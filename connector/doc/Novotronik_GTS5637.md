---
uid: Connector_help_Novotronik_GTS5637
---

# Novotronik GTS5637

The Novotronik GTS5637 is a 2:1 redundant amplifier system.

This connector can be used to monitor the status of the unit. It can also be used to set the gain of the two main RF paths or to manually switch one of the main RF paths to the backup RF path.

## About

### Version Info

| Range                | Key Features     | Based on     | System Impact     |
|----------------------|------------------|--------------|-------------------|
| 1.0.0.x \[SLC Main\] | Initial version  | \-           | \-                |

### Product Info

| Range     | Supported Firmware     |
|-----------|------------------------|
| 1.0.0.x   | 1.0                    |

### System Info

| Range     | DCF Integration     | Cassandra Compliant     | Linked Components     | Exported Components     |
|-----------|---------------------|-------------------------|-----------------------|-------------------------|
| 1.0.0.x   | No                  | Yes                     | \-                    | \-                      |

## Configuration

### Connections

#### Serial Connection

This connector uses a serial connection and requires the following input during element creation:

SERIAL CONNECTION:

- Interface connection:

  - **IP address/host**: The polling IP of the device.
  - **IP port**: The IP port of the device. Default value: *9997*.

### Web Interface

The web interface is only accessible when the client machine has network access to the product.

## How to Use

The **General** page displays the route (*Default*/*Backup*) and the gain of the two RF paths.

The **Status** page displays the different alarms provided by the device (**Temperature**, **DC Line**, etc.).
