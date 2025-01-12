## Requirements

This article covers the installation of Pentaho Data Catalog. For every release, a release package containing all necessary Data Catalog software and dependencies for installation is made available.

!!! note "Note"

    To access the appropriate release package, Hitachi Vantara provides specific credentials along with a URL download link. These credentials grant you access to download the required package for your server.

Pentaho Data Catalog requires specific external components and applications to operate optimally. This article provides a list of those components and applications along with details of their use and the versions Data Catalog supports.

## Environment considerations
To ensure proper software development and deployment practices, it is a best practice to have two separate environments:

- Development or Staging
- Production

## System requirements
This section outlines the software, hardware, and access requirements you should have before you install Data Catalog.

??? Tip "Checklist for infrastructure requests"

    Perform the following tasks as needed to prepare your environment for Data Catalog:

    - Request a Virtual Machine (VM) on Azure or AWS or on-premises.
    - Request IDs with remote access permissions to the VM on your cloud or on-premises.
    - Request necessary access to systems, applications, and data sources.
    - Request VDI or VPN access for Data Catalog data engineers to enable remote access to the VM.
    - Request a database user account (service account) or logins for connecting to the data sources.
    - Make sure the database user account has read-only permissions for the database objects, including system catalog tables.
    - Make sure that your system owner or Database Administrator (DBA) has copied or extracted any required data or files.
    - Obtain an SSL certificate from a certificate authority. If required by your organization's security policy, raise an infrastructure support request for an SSL certificate. The certificate authority will give you a key file and a certificate file.

# Hardware requirements

Your server and network must meet the following requirements: