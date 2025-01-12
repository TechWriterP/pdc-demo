# Installing Data Catalog

!!! tip
    It is a best practice before installing Data Catalog to save a copy of your conf/.env file to save any environment customizations you have made in case the file is overwritten during the installation process. During installation, Data Catalog checks for a PDC_DATA_ENCRYPTION_KEY environment variable in the conf/.env file. If the variable exists, the conf/.env file is retained. However, if the variable does not exist, Data Catalog generates a new .env file containing a PDC_DATA_ENCRYPTION_KEY environment variable. If needed, you can add any custom environment variable settings back in to the new .env file from your saved file.

Perform the following steps to install Data Catalog:

!!! abstract "Before you begin"
    Lorem ipsum

**Procedure**

1. Verify that you have root privileges or have the necessary permissions to run Docker.
2. Open a terminal window on your dedicated Data Catalog deployment server.
3. Save the Data Catalog release package in the Data Catalog server.
4. Open a terminal window on your dedicated Data Catalog deployment server and extract the files from the release package to the /opt directory using the following command:
    ```py
    tar -xvf [name of release package].tar.gz -C /opt
    ```
   The command creates a pentaho directory and extracts the contents of the deployment into a pdc-docker-deployment subdirectory.
5. Load the required installation images that are packaged in the vendor directory into Docker using the following command:
    ``` linenums="1"
    cd /opt/pentaho/pdc-docker-deployment
    ./pdc.sh load-images
    ```
    You may get a message to set the ```GLOBAL_SERVER_HOST_NAME``` variable:
    ```
    GLOBAL_SERVER_HOST_NAME env is not set, please select an environment variable value from the list or type your own:
    1.	IP address
    2.	Hostname
    3.	Hostname.localhost.localdomain
    4.	Other 
    #?    1
    ```
6. (Optional) If you get the GLOBAL_SERVER_HOST_NAME env is not set message, enter the number for the option that you want to set as the variable and press Enter.
    If you select 1, the script sets the GLOBAL_SERVER_HOST_NAME variable to the IP address in the conf/.env file.
7. Edit the conf/.env file to add email domains and keycloak SMTP configuration:
    ```
    sudo vi conf/.env
    ```
    a. Add new email allowed domains into the .env file. By default, Data Catalog includes users that use hv.com emails. You can add your own domain to this list:
    ```
    EMAIL_DOMAINS='["hv.com", "hitachivantara.com", "pdccatalog.com", "example.com", "yahoo.com"]'
    ```
    b. Add configuration for Keycloak SMTP. In the example value below, SMTP configuration is set to use hv.com emails, but you can change these to point to your company’s SMTP server configuration:
    ```
    KEYCLOAK_SMTP='{"replyToDisplayName" : "pdccatalog@hv.com","starttls" : "true","auth" : "true","envelopeFrom" : "pdccatalog@hv.com", "ssl" : "true","password" : "fwjx mpvb hcdb yofp","port" : "465","host" : "smtp.hv.com","replyTo" : "pdccatalog@hv.com","from" : "pdccatalog@hv.com","fromDisplayName" : "pdccatalog@hv.com","user" : "pdccatalog@hv.com"}'
    ```
   c. Save the file.

    !!! note 
        The email and SMTP settings are complete. If you want to update email or SMTP settings after installation, this will need to be done using IAM APIs.

8. Start all the Docker containers using the following command:
    ```
    sh pdc.sh up
    ```
    The installation script uses the packaged Docker images for the Data Catalog release and the Data Storage Optimizer release, if installed, to create and run Docker containers on your dedicated server.

!!! success "Result"
    The installation is ready for use after all the Docker containers have successfully started.