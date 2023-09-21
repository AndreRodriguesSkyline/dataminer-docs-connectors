---
uid: Connector_help_KOHLER-SDMO_APM403
---

# KOHLER-SDMO APM403

This connector monitors the activity of the KOHLER-SDMO APM403.

## About

This control panel is designed for low voltage industrial diesel generator sets and its remote management and supervision functions allows monitoring and even operation at anytime, anywhere.

### Version Info

| Range            | Key Features | Based on | System Impact |
|----------------------|------------------|--------------|-------------------|
| 1.0.0.x [SLC Main] | Initial version. | -           | -                |

### Product Info

| Range     | Supported Firmware     |
|-----------|------------------------|
| 1.0.0.x   | 1.2.0.1                |

### System Info

| Range     | DCF Integration     | Cassandra Compliant     | Linked Components     | Exported Components     |
|-----------|---------------------|-------------------------|-----------------------|-------------------------|
| 1.0.0.x   | No                  | Yes                     | \-                    | \-                      |

## Configuration

### Connections

#### SNMP Main Connection

This connector uses a Simple Network Management Protocol (SNMP) connection and requires the following input during element creation:

SNMP CONNECTION:

- **IP address/host**: The polling IP or URL of the destination.
- **IP port**: The IP port of the destination.
- **Bus address**: The bus address of the device.

SNMP Settings:

- **Get community string**: The community string used when reading values from the device. (default: *public*)
- **Set community string**: The community string used when setting values on the device (default: *private*).

### Initialization

No extra configurations are needed.

### Redundancy

There is no redundancy defined.

### Web Interface

The web interface is only accessible when the client machine has network access to the product.

## How to use

## General

The General Page displays information about the device. In the **Configuration** subpage it is possible to configure some general parameters.

## Generator

This page displays the information related with the device generators.

## Controller I/O

This page displays the value of the I/O parameters including the **Input** and **Output** Alarms.

## Statistics

In this page it is possible to check some statistical data about the device**.**
