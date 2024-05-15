---
uid: Connector_help_Generic_HTTP_Credential_Manager
---

# Generic HTTP Credential Manager

This connector can be used to manage sets of credentials for HTTP connectors.

## About

With this connector, you can store and use credentials for other HTTP connectors that have been equipped to use the Generic HTTP Credential Manager.

### Version Info

| Range     | Key Features     | Based on     | System Impact     |
|-----------|------------------|--------------|-------------------|
| 1.0.0.x   | Initial version  | -            | -                 |

### System Info

| Range     | DCF Integration     | Cassandra Compliant     | Linked Components     | Exported Components     |
|-----------|---------------------|-------------------------|-----------------------|-------------------------|
| 1.0.0.x   | No                  | Yes                     | -                     | -                       |

## Configuration

### Connections

#### Virtual Connection

This connector uses a virtual connection and does not require any input during element creation.

## How to use

The connector displays only one page, the General page, which contains the **Credentials** table. In this table, you can view and edit the **Friendly Name**, **Username**, and **Password** for each set of credentials.

The page also contains a page button, **Add Credential**, which opens up a pop-up page that allows you to add a new set of credentials. To do so, fill in the **Friendly Name**, **Username** and **Password**, and click the **Add New Credential** button to add it to the table.
