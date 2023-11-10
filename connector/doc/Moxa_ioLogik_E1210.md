---
uid: Connector_help_Moxa_ioLogik_E1210
---

# Moxa ioLogik E1210

This connector allows you to monitor a configured Moxa ioLogik E1210 device via SNMP. It displays basic information about the device, as well as the status of the existing DI channels. For each DI channel, some settings can also be configured.

## About

### Version Info

| **Range** | **Key Features**                | **Based on** | **System Impact**              |
|-----------|---------------------------------|--------------|--------------------------------|
| 1.0.0.x   | Monitoring of DI channels       | \-           | \-                             |
| 1.0.1.x   | Improved DI channel display key | 1.0.0.x      | Display keys have been updated |

### Product Info

| Range     | Supported Firmware     |
|-----------|------------------------|
| 1.0.0.x   | v3.0                   |
| 1.0.1.x   | v3.0                   |

### System Info

| Range     | DCF Integration     | Cassandra Compliant     | Linked Components     | Exported Components     |
|-----------|---------------------|-------------------------|-----------------------|-------------------------|
| 1.0.0.x   | No                  | Yes                     | \-                    | \-                      |
| 1.0.1.x   | No                  | Yes                     | \-                    | \-                      |

## Configuration

### Connections

#### SNMP Main Connection

This connector uses a Simple Network Management Protocol (SNMP) connection and requires the following input during element creation:

SNMP CONNECTION:

- **IP address/host**: The polling IP of the device, e.g. *10.11.12.13.*

SNMP Settings:

- **Port number**: The port of the connected device, by default *161.*
- **Get community string**: The community string in order to read from the device. The default value is *public*.
- **Set community string**: The community string in order to set to the device. The default value is *private.*

### Web Interface

The web interface is only accessible when the client machine has network access to the product.

## How to use

### General Page

This page displays **system information**: the total number of channels, server model, system uptime and firmware version.

### I/O Status Page

On this page, you can find the **DI channel monitor table**. This table allows you to monitor all available DI channels, as well as set specific parameters for each channel such as mode, filter, trigger and counter.
This table also allows you to configure a custom name for each channel. Greyed out entries in this table are disabled and cannot be set.
