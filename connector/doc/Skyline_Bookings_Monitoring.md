---
uid: Connector_help_Skyline_Bookings_Monitoring
---

# Skyline Bookings Monitoring

The **Skyline Bookings Monitoring** is a virtual connector that allows **SRM Solution** to report the status of bookings to produce alarm and trend data over the booking data.

## About

### Version Info

| Range                | Key Features     | Based on     | System Impact     |
|----------------------|------------------|--------------|-------------------|
| 1.0.0.x [SLC Main] | - Booking Table to Monitor booking<br>- Clear all Nominal Bookings Button<br>- Clear all Bookings Button<br>- Configurable Retention Time<br>- Configurable Past Lookup Time | - | - |

### Product Info

| Range     | Supported Firmware                                                                                       |
|-----------|----------------------------------------------------------------------------------------------------------|
| 1.0.0.x   | Connector meant to be installed with Skyline Booking Manager Connector (2.0.2.29) in SRM 1.2.14 or above |

### System Info

| Range     | DCF Integration     | Cassandra Compliant     | Linked Components     | Exported Components     |
|-----------|---------------------|-------------------------|-----------------------|-------------------------|
| 1.0.0.x   | No                  | Yes                     | -                     | -                       |

## Configuration

### Connections

#### Virtual connection

This connector uses a virtual connection and does not require any input during element creation.

### Initialization

No extra configuration is needed.

### Redundancy

There is no redundancy defined.

## How to use

This connector is part of the **SRM Solution**.

To use this connector properly a user must access the **Skyline Booking Manager** and configure:

- **Bookings Monitoring Element** with the name of the created Skyline Bookings Monitoring Element Name.

- **Bookings Monitoring Mode:** with one of the following states:

  - **None**: No Bookings will be reported
  - **Non-Nominal**: All Failed, Quarantined or Interrupted bookings will be reported to the configured element.
  - **All Bookings**: Report all Configured Bookings.

## General

In this page the user will find the Bookings table which features all bookings that are under monitoring.

The Connector will only monitor bookings that are running, in a non-nominal state and past bookings.

There are 2 buttons to allow a user to **clear all bookings** or to **clear all nominal bookings**, while keeping bookings with non-nominal states.

There is an extra **Refresh** button that will refresh the Bookings Table based on the configuration.

## Configuration

Two parameters are available on this page to set the:

**Retention Time:** Time over which a booking is kept on the Table even after the booking as already finished.

**Past Lookup Time:** Time over which the element actively looks for bookings which have not ended.

## Notes

This connector is part of the SRM Solution and should not be installed on standalone integrations.

Skyline Bookings Monitoring is meant to work on a 1 to 1 mapping to a Skyline Booking Manager.

**Always install this Protocol via SRM Solution package.**
