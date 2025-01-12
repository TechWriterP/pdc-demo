# Pentaho Data Catalog overview

Pentaho Data Catalog rapidly ingests, profiles, and meticulously curates structured and unstructured data through a combination of automation and machine learning. This process involves data fingerprinting and the application of metadata rules to provide contextualization aligned with the business's terminology as documented in the business glossary.

### AI-driven discovery

Data Catalog uses unique data fingerprinting to automate discovery and classification of structured, semi-structured, and unstructured data.

### User interface

Data Catalog's interactive user interface provides a customized user experience for the business role of every user, promoting rich content authoring and resource knowledge.

### Data Canvas

Data Catalog gives users access to the file and field-level metadata available for the entire catalog of data assets. In addition, for the assets that each user has authorization to view, the Data Catalog displays a rich view of data-based details such as minimum, maximum, and most frequent values. Data Catalog users can add their own information to the catalog in the form of descriptions and custom metadata designed for their organization.
Use the Data Canvas to explore and investigate your data. Here, you can find detailed insights into resource metadata to help you understand and clarify practical applications.

![Data Canvas](/img/prod-overview/data-canvas.png)

### Galaxy view

In Data Catalog, you can use the Galaxy view feature to quickly view the structure of your data and its details. Galaxy view is especially useful when you want to view information that is not easily visualized using the navigation tree in the Data Canvas.

![Galaxy View](/img/prod-overview/galaxy-view.png)

In business glossary, you can use the Galaxy view feature to visualize and explore business terms and their relationships and to understand how terms are interconnected. You can also quickly identify related terms, synonyms, and hierarchies within specific domains or categories, enhancing their understanding of the glossary's structure.

### Business glossary

Data Catalog lets you build or import a taxonomy of business terms in a ​glossary and organized into domains and categories and establish relationships between terms. Data Catalog distributes these terms to similar data across the cluster, producing a powerful index for business language searches. It lets business users find the right data quickly to understand the meaning and quality of the data at a glance.
Access control
User profiles, roles, and access restrictions combine to deny or grant metadata access to users.

### User roles

Assigning roles to Data Catalog users lets administrators exercise role-based functional and access control for those users, such as who can assign a business term to data and who can update a business rule. In addition, you can use roles to establish access control over Data Catalog resources at the data source level. Roles also incorporate a set of predefined access levels that define which features of the catalog are available to different users.

### Architecture

The following diagram provides an overview of Data Catalog's architectural components across the distributed application.

![Diagram of PDC Architecture](/img/prod-overview/pdc-architecture.png)

### Pentaho Data Storage Optimizer

If you wish, you can install Pentaho Data Storage Optimizer to use with Data Catalog.

Data Storage Optimizer is an intelligent data storage tiering solution that reduces operating costs and gives you seamless access to Hadoop data with S3 compatible object storage like Hitachi Content Platform.

For more information on Pentaho Data Storage Optimizer, see *Pentaho Data Storage Optimizer* document.

To install Data Storage Optimizer, see the *Install* chapter of the *Pentaho Data Storage Optimizer* document.

You can either install Data Storage Optimizer when you install Data Catalog, or if you already have Data Catalog 10.0.1 installed, you can enable Data Storage Optimizer.