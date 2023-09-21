---
uid: Connector_help_Sky_UK_Info_On_EWL_-_Pin_Due_Workflow
---

# Sky UK Info On EWL - Pin Due Workflow

This connector can be used to create an enhanced service containing elements using the connectors [Sky UK SSR](xref:Connector_help_Sky_UK_SSR) and [Sky UK VICC](xref:Connector_help_Sky_UK_VICC).

With this connector, alarms can be generated according to predefined rules.

## About

### Version Info

| Range                | Key Features     | Based on     | System Impact     |
|----------------------|------------------|--------------|-------------------|
| 1.0.0.x \[SLC Main\] | Initial version. | \-           | \-                |

### System Info

| Range     | DCF Integration     | Cassandra Compliant     | Linked Components     | Exported Components     |
|-----------|---------------------|-------------------------|-----------------------|-------------------------|
| 1.0.0.x   | No                  | Yes                     | \-                    | \-                      |

## Configuration

To use this connector, create a service that uses it as its service definition. Then configure the following child elements/parameters:

- [Sky UK VICC](xref:Connector_help_Sky_UK_VICC)

  - **Channel From User**
  - **Data Update Trigger**

- [Sky UK SSR](xref:Connector_help_Sky_UK_SSR)

  - **Start Date Time (Current Events)**
  - **Duration (Current Events)**
  - **Parental Rating (Current Events)**

## How to Use

A service created using this connector will have the data pages detailed below.

### Alarms

This page displays the **Early Warning List Table**, with an entry for each current and future event with their PIN due status. The table displays the Cause, Alarm State, Channel, Alarm Time and Target UI.

### Device Data

Because multiple services are evaluated, no single parameters with logical states are displayed. The SSR identifier is required for lookups when the VICC triggers. The value is displayed for validation purposes. It also shows the value of the **Channel Bus** and the **Service Status**. When the latter is *Off-Air*, this workflow will not trigger any alarms. If it is *NA* or *On-Air*, the workflow will run as expected.

### Subscriptions Active

This page contains a table with parameters contained within the service.
