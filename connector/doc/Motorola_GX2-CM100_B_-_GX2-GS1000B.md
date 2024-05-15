---
uid: Connector_help_Motorola_GX2-CM100_B_-_GX2-GS1000B
---

# Motorola GX2-CM100 B - GX2-GS1000B

The **Motorola GX2-CM100 B - GX2-GS1000B** connector is an SNMP-based connector used to monitor and configure the **Motorola GX2-GS1000B**.

## About

This connector provides a monitoring interface for the **Motorola GX2-GS1000B** module.

### Version Info

| Range                | Key Features     | Based on     | System Impact     |
|----------------------|------------------|--------------|-------------------|
| 2.0.1.x [SLC Main]   | Initial version  | -            | -                 |

### Product Info

| Range     | Supported Firmware     |
|-----------|------------------------|
| 2.0.1.x   | D                      |

### System Info

| Range     | DCF Integration     | Cassandra Compliant     | Linked Components     | Exported Components     |
|-----------|---------------------|-------------------------|-----------------------|-------------------------|
| 2.0.1.x   | No                  | Yes                     | -                     | -                       |

## Installation and configuration

### Creation

This connector is used by DVE child elements that are **automatically created** by the parent connector [Motorola GX2-CM100 B](xref:Connector_help_Motorola_GX2-CM100_B), from version 2.0.1.1 onwards.

## Usage

### General

This page displays general information about the card, including the **Unit Name**, **Module Type**, **Firmware** and **Hardware Version**, **IP Address** and **Physical Address**.

### DWDM Transmitter

This page displays the parameters **Offset Monitor**, **Offset Control**, **Optical Power**, **Laser Temperature**, **Laser BIAS**, **TEC Current**, **Temperature**, **12V Current**, **Fan 1 Speed**, **Fan 2 Speed**, **RF Input**, **Optical Power Output**, **Laser Mode**, **Attenuator**, **Laser Secondary Mode**, **Video Offset** and **Factory Default**.

### Alarms

This page contains all **Status** parameters.

### Factory

This page displays **CRC Parameters**, **Flash Banks** and **Flash Counters**.

### Web Interface

This page displays the webpage of the device. Note that the client machine has to be able to access the device, as otherwise it will not be possible to open the web interface.
