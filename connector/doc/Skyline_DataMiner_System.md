---
uid: Connector_help_Skyline_DataMiner_System
---

# Skyline DataMiner System

This connector can be used to monitor a DataMiner System from another DataMiner System.

## About

This connector uses the DataMiner Web API v0 and v1 to monitor a DataMiner System.

The DataMiner Agent that is polled needs to have a valid Web API v1 license.

### Version Info

| Range                | Key Features     | Based on     | System Impact     |
|----------------------|------------------|--------------|-------------------|
| 1.0.0.x [SLC Main]   | Initial version  | -            | -                 |

### Product Info

| Range     | Supported Firmware     |
|-----------|------------------------|
| 1.0.0.x   | 7.5 and up             |

### System Info

| Range     | DCF Integration     | Cassandra Compliant     | Linked Components     | Exported Components     |
|-----------|---------------------|-------------------------|-----------------------|-------------------------|
| 1.0.0.x   | No                  | No                     | -                     | -                       |

## Installation and configuration

### Creation

#### HTTP Main connection

This connector uses an HTTP connection and requires the following input during element creation:

HTTP CONNECTION:

- **IP address/host**: The polling IP or URL of the destination DMA. The polled DMA needs to have a valid Web API v1 license.
- **IP port**: The IP port of the destination.
- **Bus address**: If the proxy server has to be bypassed, specify *bypassproxy.*

### Configuration of the HTTP Main connection

On the **General** > **Security** page, you need to configure the credentials of the DataMiner System that should be polled.

The configured user needs to have the Cube user permission to access the Monitoring UI. Prior to DataMiner 10.1.0/10.1.2, this is the permission Modules > System Configuration > Mobile Gateway > Allow access to Mobile UI. In more recent DataMiner versions, you can find this permission under General > DataMiner web apps / DataMiner Cube mobile access.

## Usage

### General

The General page displays general DataMiner Cluster information.

The general page includes a page button with access to the security settings.

### Server Performances

This page lists all DMAs (Main and Backup) in the DataMiner Cluster.

For each entry in the table, a Microsoft Platform element can be configured to poll extra information. The Microsoft Platform element needs to be a version in range 1.1.x.x .

### Elements page and Services page

On these pages, elements and services can be configured to be monitored.

Alarms of configured elements and services can be requested to be shown on the page button pages.

There are page buttons to list an overview of all elements/services in the cluster.

### Redundancy Groups

Redundancy groups can be configured to be monitored by the connector.

Monitored redundancy groups will list virtual elements and included elements.

There is an overview table with all redundancy groups on the page button page.

### Alarms

This page displays the number of alarms sorted by type: Critical, Major, Minor, Warning, Error, Notice, and Timeout.

There is also a parameter that displays the cluster overall alarm state.

### Cube Interface

This page gives access to the Cube Interface of the monitored DataMiner cluster.

Note that the client machine has to be able to access the polled DMA, as otherwise it will not be possible to open the web interface.
