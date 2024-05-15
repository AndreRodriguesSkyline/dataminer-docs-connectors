---
uid: Connector_help_Astro_U124_Edge_FM
---

# Astro U124 Edge FM

With this connector, you can gather and view information from the device **Astro U124 Edge FM**, as well as configure the device.

## About

This connector uses HTTP to monitor the **Astro U124 Edge FM** device. The connector also has an SNMP interface to receive traps from the device and poll certain network information.

### Version Info

| Range | Description | DCF Integration | Cassandra Compliant |
|------------------|-----------------|---------------------|-------------------------|
| 1.0.0.x          | Initial version | No                  | Yes                     |

### Product Info

| Range | Supported Firmware Version |
|------------------|-----------------------------|
| 1.0.0.x          | 4668, 6000, 6200, 6400      |

## Installation and configuration

### Creation

This connector uses two interfaces: an HTTP interface to retrieve the data and an SNMP interface to collect the traps.

Depending on the setup, the **HTTP** configuration differs: this connector can communicate directly with the **U124**, but it can also be configured to send the requests to the **Astro U100 Controller**, which will then serve as a proxy.

In either case, the **SNMP** interface collects the traps emitted by the device, so the SNMP IP address must be the IP address of the **U124** (not the controller).

#### Serial Connection for Communication with U100C as proxy

- **IP address/host**: The IP address of the Astro U100 Controller.
- **IP port**: The port of the destination, e.g. *80*.
- **Bus address**: The IP address of the U116. In addition, "*ByPassProxy*" must be filled in to bypass any possible proxy that could block the HTTP communication. The two fields must be separated by a semicolon, e.g. *ByPassProxy;10.11.12.13.*

#### Serial Connection for Direct Communication:

- **IP address/host**: The IP address of the U124.
- **IP port**: The port of the destination, e.g. *80*.
- **Bus address**: This field can be used to bypass the proxy. To do so, fill in the value *ByPassProxy*.

#### SNMP connection

SNMP Connection:

- **IP Address/host**: The polling IP of the U124, e.g. *10.11.12.13*.

SNMP Settings:

- **Port number**: The port of the connected device, by default *161*.
- **Get community string**: The community string in order to read from the device. The default value is *public*.
- **Set community string**: The community string in order to set to the device. The default value is *private*.

## Usage

### General

This page displays general information about the device.

The credentials of the device must be filled in via the **Login** page button.

Some important parameters are available at the end of the first column:

- **Controller Name**: This parameter shows the name of the **Astro Virtual Controller** element that manages this device. If no such element is used, the parameter will show the exception value *No Virtual Controller Found*.

- **Communication Type**:

- *Direct Communication*: The element sends the requests directly to the Astro module.
  - *U100C Proxy*: The element sends the requests to the Astro U100 Controller, which will forward them to the Astro module. The controller acts as a proxy.

- **Communication Method**: This parameter is only available in *Direct Communication* mode.

- *Login*: The element logs in to the device before every request (read and write requests).
  - *Anonymous*: The element only logs in to the device for write requests. The device does not log in for read requests.

### Status

This page displays the status of the device, e.g. **Temperature**, **Power Supply**, **CPU Load**, etc.

### Main

On this page, you can access the main configuration of the device, e.g. **DNS**, **Time Source**, **Interfaces**, etc.

### Test Gen

On this page, you can configure the test gen parameters, e.g. **Data Rate**, **Packet ID**, etc.

### IP Channel

On this page, you can configure the IP channels, using the **IP RX Channel Settings** table.

### RF

On this page, you can configure the RF channels

Several page buttons are available with more RF configuration options and statistics.

### Time Zone

On this page, you can configure the time zone settings.

### In Out Status

This page contains a summary of the links between inputs and outputs.

### Update/Config

On this page, you can upload/download configuration files to/from the device, and perform a software update.

#### Configuration Files (Download/Upload)

The following table provides more information on how to upload/download configuration files to/from the device:

- To **download** a file, click *Download*. The following pop-up window will be displayed:

  ![Download.PNG](~/connector/images/Download.PNG)

  Enter the name of the file then click on `OK'. The file will be saved at this location:

  `C:\Skyline DataMiner\Documents\<protocol name>\<element name>\<file name>`

- To **upload** a file, click *Upload*. The following pop-up window will be displayed:

  ![Upload.PNG](~/connector/images/Upload.PNG)

  **Module Name** lists all the Astro elements of the same type in the system.

  **Upload File Name** lists all the files available in Documents folder of the selected module.

  The file to be uploaded is located at: `C:\Skyline DataMiner\Documents\<protocol name>\<element name>\<file name>`

#### Software Update

The connector allows you to upload a firmware archive from the local disk of the DMA:

![SoftwareUpdate.PNG](~/connector/images/Astro_U124_Edge_FM_SoftwareUpdate.PNG)

The **Firmware File** parameter is used to select which file to upload. The drop-down list contains all the files present in the following directory of the DMA: *C:\Skyline DataMiner\Documents\\Protocol Name\>*.

Once the file is selected, click the button **Update and Reboot** to start the upgrade. To follow the update progress, click the **Update Progress** page button. However, traps must be configured for this to be possible.

### Licensing

This page shows the available licenses for this Astro device.

### System Log

This page contains a table listing all the log entries. You can download the log files by clicking the **Download** buttons. To access the log settings, click the **System Log Config** page button.

### Alarm Severities

On this page, you can set the severity for each alarm type.

### Active Alarms

This page displays a table with the current alarms on the device.

### Network

This page displays network parameters.

Note that these parameters are retrieved via SNMP. The polling can be enabled/disabled using the **Network Data Polling** toggle button.

### Web Interface Page

This page displays the web interface of the device. Note that the client machine has to be able to access the device, as otherwise it will not be possible to open the web interface.
