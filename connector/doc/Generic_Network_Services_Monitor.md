---
uid: Connector_help_Generic_Network_Services_Monitor
---

# Generic Network Services Monitor

The **Generic Network Services Monitor** connector is used to monitor different kinds of network services.

With this connector, you can run tests on selected network protocols. The following network services are currently supported:

- **In range 1.0.0.x:** Ping, FTP, SMTP, DNS, HTTP, Web Service, Database, TCP, RTSP, RTMP, TFTP, RADIUS, SFTP, Network Share, Multiple Network Share, NTP, and SSH.
- **In range 2.0.0.x:** Ping, FTP, SMTP, DNS, HTTP, Web Service, Database, TCP, RTSP, RTMP, TFTP, SFTP, NTP, Network Share, and Multiple Network Share.

The time between two consecutive tests is configurable. For all tests, the response time can be trended.

Each test has its own page in the element. You can configure the **Interval Time**, **Port**, **Timeout Time**, **Credentials**, etc. on each of these pages.

## About

### Version Info

| **Range**            | **Description**                      | **DCF Integration** | **Cassandra Compliant** |
|----------------------|--------------------------------------|---------------------|-------------------------|
| 1.0.0.x [Obsolete]   | Initial version.                     | No                  | No                      |
| 2.0.0.x [SLC Main]   | Allows multiple devices per element. | No                  | No                      |

### Product Info

| Range     | Supported Firmware     |
|-----------|------------------------|
| 1.0.0.x   | N/A                    |
| 2.0.0.x   | N/A                    |

## Configuration

Create a new element with this connector and give it a unique name.

- In **range 1.0.0.x**, the polling IP is used as the main address for each test, and it is also possible to enter a hostname as polling IP (e.g. "google.com").
- In **range** **2.0.0.x**, no IP address is configured in the element editor, as the connector retrieves information from several devices for the same element. Instead, a new device can be added to the **General page** with the context menu option **Add new device**. (To access the context menu, right-click the table.)

## Usage

### Main View page

This page displays a summary table with an overview and results of all the tests that have been or are being executed.

### General page

This page displays the server name and IP address. On the right-hand side, tests can be enabled or disabled.

### Overview page

This page displays the monitored services in a tree chart layout.

### Ping page

The ping test is used to test the reachability of a host. The round-trip time between the request and the response is measured.

### FTP page

The FTP test can be used to check if it is possible to log on to the FTP server with the provided credentials.

In range 2.0.0.x, from version 2.0.0.9 onwards, it is possible to select the format of the primary key (*IP* or *IP/Port*) of the FTP Table. If *IP/Port* is selected, it is possible to monitor a device through different ports. These entries can be added via the right-click menu. To add a device with a specific port to the table, make sure the IP is registered in the Monitored Devices table (on the General page).

### SMTP page

The SMTP test will connect to the server and check if the correct login request is retrieved.

### DNS page

The DNS test will try to resolve a hostname to an IP address.

In range 2.0.0.x, from version 2.0.0.9 onwards, it is possible to select the format of the primary key (*IP* or *IP/Port*) of the DNS Table. If *IP/Port* is selected, it is possible to monitor a device through different ports. These entries can be added via the right-click menu. To add a device with a specific port to the table, make sure the IP is registered in the Monitored Devices table (on the General page).

### HTTP page

With this test, you can execute an HTTP request on the server. GET, POST and HEAD requests are supported

In range 2.0.0.x, from version 2.0.0.9 onwards, it is possible to select the format of the primary key (*IP* or *IP/Port*) of the HTTP Table. If *IP/Port* is selected, it is possible to monitor a device through different ports. These entries can be added via the right-click menu. To add a device with a specific port to the table, make sure the IP is registered in the Monitored Devices table (on the General page).

### Database page

With this test, a query is executed on the database. The result is investigated to determine if the server is still working fine.

In range 2.0.0.x, from version 2.0.0.9 onwards, it is possible to select the format of the primary key (*IP* or *IP/Port*) of the Database Table. If *IP/Port* is selected, it is possible to monitor a device through different ports. These entries can be added via the right-click menu. To add a device with a specific port to the table, make sure the IP is registered in the Monitored Devices table (on the General page).

### TCP page

This test will try to make a TCP connection on the specified port. No data is transferred; only the possibility to connect is tested.

In range 2.0.0.x, from version 2.0.0.9 onwards, it is possible to select the format of the primary key (*IP* or *IP/Port*) of the TCP Table. If *IP/Port* is selected, it is possible to monitor a device through different ports. These entries can be added via the right-click menu. To add a device with a specific port to the table, make sure the IP is registered in the Monitored Devices table (on the General page).

### RTSP page

This test checks if an RTSP connection can be made to the server. A "DESCRIBE" request is executed to verify if the server answers correctly.

### RTMP page

This test checks if an RTMP connection can be made to the server. The first received packet is inspected to determine if the service is still working fine.

### TFTP page

With the TFTP test, you can determine if a certain file exists on the TFTP server.

In range 2.0.0.x, from version 2.0.0.9 onwards, it is possible to select the format of the primary key (*IP* or *IP/Port*) of the TFTP Table. If *IP/Port* is selected, it is possible to monitor a device through different ports. These entries can be added via the right-click menu. To add a device with a specific port to the table, make sure the IP is registered in the Monitored Devices table (on the General page).

### NTP page

With this test, NTP port availability can be monitored. IP and port can be specified. DNS resolution can be used.

### Network Share page

This test can be used to verify if the network share is available with the provided credentials. Optionally, the use of credentials can be disabled. The total/free disk space and the number of files/folders can also be checked.

### Multiple Network Share page

This test allows you to verify the availability of multiple network shares. Optionally, the use of credentials can be disabled. The total/free disk space and the number of files/folders can also be checked.

### SFTP page

This test provides file access, file transfer, and file management over a secure SSH channel.

### Web Service page

This test will invoke a web service method with the provided input data.
To define arrays in the input table, C# syntax should be used, e.g. '*new \[\] {"1", "2", "3"}*'.
The different parts of the response object are displayed in the output table.

In range 1.0.0.x, to configure this test, open the **Select Method** subpage and fill in the location of the WSDL file that describes the web service. Then select the service and method that must be executed.
In range 2.0.0.x, the WSDL location, service and method is configured in the same row as the other settings for the web service test.

The location of the WSDL file can be a URL or local file path. In both instances, it will be saved under C:\Skyline DataMiner\Documents\GNSM\.

### RADIUS page (range 1.0.0.x only)

With this test, you can check if the radius server is working and if the provided user is able to log on.

### SSH page (range 1.0.0.x only)

With this test, SSH port availability can be monitored. DNS resolution can be used.
