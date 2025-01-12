# What is new in Pentaho Data Catalog

### Key features
The key features in this release are:

### Data delivery
A business user is able to find data and with a few clicks be able to configure a data pipeline that delivers the data to its desired destination.

### Application catalog
Catalog your applications, their governance requirements, ownership, their relationship
with data assets, reference data and other elements in the data catalog

### Governance policies
Document regulatory or corporate regulations, policies, standards in the catalog, building a source of record and an intuitive interface to find policies and the data to which they apply.

### Data lineage
Build data lineage for data movement executed by Pentaho ETL. Compatible with open lineage, this capability gives us a quick ROI for customers interested in lineage for Pentaho Data Integration.

### Galaxy view
This release enhances the visual representation of assets (such as data assets, business terms, policies/standards/rules, reference data, and applications) to easily grasp the dependencies, understand potential impact, and collaborate with all the stakeholders to make the right business decision.

### Trust score
Support for bringing data quality scores from the Pentaho Data Quality product, verification of lineage, and assessing sensitivity to build a trust score.

### License support
This release introduces a license solution for the Data Catalog and Pentaho Data Optimizer products. You can configure the number of data sources and Expert users (Steward, Admin, Developer) you can add, and the size of data scanned from file systems.

In addition, there are numerous improvements including extensive rules support, additional support for data sources and technologies, and continued emphasis on ease of use and performance improvements.

### Product roles & licensing
Your Data Catalog software license determines the following entitlements:

- additional features that you can use (Pentaho Data Optimizer and Pentaho Data Mastering)
- the number of data sources you can add
- the amount of data you can scan
- the number of Expert user roles that you can assign to users. The Expert user roles are:
    - Business Steward
    - Data Steward
    - Admin
    - Data Developer

To calculate the total number of users for licensing, use the following table for mapping from product role to licensing role. A named user with multiple product roles maps into a single user for licensing consideration. For example, if a user is given the role of data source administrator and data source access manager, that is considered a single licensed Data Steward. If two distinct users are given these two roles, then that is considered two licensed Data Stewards.

| Product Roles                       | Licensing Considerations |
|-------------------------------------|--------------------------|
| Owner                               | Admin User               |
| Reader                              | Business User            |
| User Access Administrator           | Admin User               |
| Data Source Administrator           | Data Steward             |
| Data Source Access Manager          | Data Steward             |
| Data Quality Administrator          | Data Steward             |
| Data Quality Operator               | Data Steward             |
| Data Quality Rule Approver          | Data Steward             |
| Data Profiler                       | Data Steward             |
| Data Sample Viewer                  | Business User            |
| Data Tagger                         | Data Steward             |
| Data Tag Viewer                     | Data Steward             |
| Business Glossary Administrator     | Data Steward             |
| Business Glossary Mapper            | Data Steward             |
| Data Identification Methods Manager | Data Steward             |
| Data Source Steward                 | Data Steward             |