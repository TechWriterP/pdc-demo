The advantage of using software in a hyperscale environment is that the architecture can scale as needed to meet increased usage by provisioning additional resources on demand. Hyperscale environments also offer full high availability, intelligent load balancing, and support for orchestration.

You can use Pentaho Data Catalog in a hyperscaler environment by launching an instance of Data Catalog in the Amazon Web Services (AWS) Marketplace or the Microsoft Azure Marketplace.

Launching a Data Catalog instance in a hyperscaler
To launch an instance of Data Catalog in a hyperscaler, see the following procedures for the marketplace you want to use:

## Launching a Data Catalog AMI in AWS

You can launch a new Data Catalog Amazon Machine Image (AMI) from the AWS Marketplace. To use the Data Catalog AMI, you must create a customized security group and select or create an SSH key pair during the launch configuration.

### Launch the Data Catalog AMI instance

Perform the following steps to launch an instance of the Data Catalog AMI from the AWS console:

**Procedure**

1. From the AWS **Console Home** page, click **EC2**.
   
   The **EC2 Dashboard** opens with a **Launch instance** card.
    
    !!! note
        You can also launch a Data Catalog AMI from the Amazon Marketplace.

2. On the **Launch instance** card, click **Launch instance**.

    The **Launch an instance** page opens.

3. Add a name for the instance.
4. In the **Application and OS images (Amazon Machine Image)** card, enter Pentaho Data Catalog in the search field.
5. On the Pentaho Data Catalog result, click **Select**.
6. Review the product overview, details, and pricing, and click Continue to accept the terms.
7. On the **Instance type** card, choose an instance type from the list.

    For a Production environment, it is a best practice to use a **2xlarge** or larger instance type.

8. On the **Key pair (login)** card, select an existing key pair to connect securely, or create a new key pair.

    If you create a new private key, the file downloads automatically to your local computer.

    !!! Note
        Make sure to store the private key file in a secure location, because you need it to connect to the instance using SSH.

9. On the **Network settings** card, make the following selections:
    
    - Under Firewall (security groups), select an existing security group or create a new one.

    !!! Note
        Any existing security group you select must support SSH and HTTPS traffic.

    - Select the Allow SSH traffic from checkbox and choose My IP from the list.

    !!! Note
        Use the username pentaho and port 22 for SSH access.

    - Select the **Allow HTTPS traffic** from the internet checkbox.

10. On the **Configure storage** card, specify at least **512 GiB** for a Production instance.
11. Click **Launch instance**.

    The instance launches, and you are subscribed to the Marketplace AMI. When the process is complete, a success message includes a link to the instance, with the unique instance ID.

12. Record the instance’s IP address or URL.

    It is needed for the [Set up an administrator account for the AWS instance](https://docs.hitachivantara.com/r/G9GP7z6L5RyH4VQoyvktoA/Y90Wv4xatSfn8vacjbkNfA) procedure.

13. Click the instance link.

    The **Instances** page opens.

14. Select the checkbox next to the Data Catalog instance and click **Launch instances**.

!!! Abstract "Next Steps"
    When the instance is running, you can connect to it using HTTPS in the browser on port 443. You might need to create a new rule or edit an existing rule to allow traffic on port 443 from your desired IP addresses or IP ranges.

### Set up an administrator account for the AWS instance

You must set up an administrator account to manage your Data Catalog instance in the AWS Marketplace.

!!! abstract "Before you begin"
    Before you begin this procedure, you must have an IP address or URL for accessing the Data Catalog instance and an environment that meets the following conditions:

    - an active Data Catalog instance in the AWS Marketplace.
    - traffic allowed on port 443 from your desired IP addresses or IP ranges.

Perform the following steps to set up the account:

**Procedure**

1. In a browser, navigate to the Data Catalog IP address or URL resulting from the Launch the Data Catalog AMI instance procedure.
    You must use HTTPS to access the instance. You might see a NET::ERR_CERT_AUTHORITY_INVALID error message, due to Data Catalog's self-signed certificate.

2. Ignore the error and proceed.
    You can add your own certificates to Data Catalog later.
    You are redirected to the Data Catalog admin account registration page.

3. On the Create Admin Account page, provide details for the Data Catalog admin user and click Create Account.
You are logged in to the admin account and see the Data Catalog home page.

!!! Abstract "Next Steps"
    You can begin using Data Catalog or create accounts for other users in your organization.

## Launching a Data Catalog VMI in Azure

You can launch a new Data Catalog Virtual Machine Image (VMI) from the Microsoft Azure Marketplace. To use the Data Catalog VMI, you must create a customized network security group and select or create an SSH key pair during the launch configuration.

### Launch the Data Catalog VMI instance

### Set up an administrator account for the Azure instance