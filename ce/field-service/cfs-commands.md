---
title: Send commands in Connected Field Service
description: Send commands to IoT devices with Field Service to remotely control them.
ms.date: 09/04/2024
ms.topic: how-to
ms.subservice: connected-field-service
ms.custom: bap-template
ms.author: vhorvath
author: vhorvathms
---

# Send commands in Connected Field Service

Dynamics 365 Field Services enables seamless bi-directional communication with your IoT devices. It empowers your organization to not only gather data from IoT devices but also send commands and receive real-time updates. This symmetrical flow of information enhances control, monitoring, and decision-making capabilities within the IoT infrastructure.

Commands are programed instructions sent from the Field Service application to IoT devices. They direct devices to perform specific actions, retrieve data, or modify their existing configurations. Commands consist of IoT definition properties that provide a standardized framework for understanding and interacting with device data. These properties represent the attributes or characteristics of IoT devices that can be monitored or controlled. For example, the IoT definition properties for a thermostat might include temperature and humidity.

> [!TIP]
> Commands for an IoT device are usually documented in the device manual or API documentation. These resources provide detailed information on the available commands, their syntax, and how to interact with the device programmatically.

## Create IoT definition properties

Before configuring an IoT command in Field Service, you first need to create IoT definition properties. IoT definition properties help construct the message string for your IoT command.

1. In Field Service, change to the **Settings** area.
1. Under **IoT**, select **IoT Property Definitions** and select **New**.
1. Enter a **Name** and choose the **Type** of data for the property.
1. Add information in the **Additional Properties** section. Select **Show string** to verify the constructed string.
1. Select **Save**.

:::image type="content" source="media/ioT-property-definition.png" alt-text="Screenshot of a filled out IoT property definition record.":::

## Configure IoT commands

1. In Field Service, change to the **Settings** area.
1. Under **IoT**, select **Command Definitions** and select **New**.
1. In the **Name** field, enter the command definition. For example: Reset Thermostat.
1. Select **Save**.
1. In the **Command Parameters** section, select the vertical ellipsis &vellip; and choose **Add Existing IoT Property**.
1. Select a IoT property definition record and select **Add**.
1. Select **Save**.

:::image type="content" source="media/IoT-command-definition.png" alt-text="Screenshot of an IoT command definition record.":::

## Send a command on an active IoT alert

1. In Field Service, open the **Service** area.
1. Under **Assets**, select **IoT Alerts** and open an existing IoT alert record.
1. On the Iot alert record, select **Send Command**.
1. Choose a command definition in the **Command** field and select **Send Command**.

:::image type="content" source="media/IoT-alert-send-command.png" alt-text="Screenshot of an IoT alert with the send command dialog option.":::

## Example thermostat simulator commands

If you use the [IoT deployment template for Azure IoT Hub](installation-setup-iothub.md), you can choose to install a thermostat simulator. The following table lists commands that you can send to the thermostat simulator.

|       Command  |     Command Message String   |
|---|---|
|     Reset Thermostat  |   {"CommandName":"Reset Thermostat","Parameters":{}}  |
|     Notification  |   {"CommandName":"Notification","Parameters”: {"Message":"Technician has been dispatched"}}  |
|     Set Values (Update IoT property definitions Temperature and Humidity)    |      {"CommandName":"Set Values","Parameters”: {"Reading":{"Temperature":"70","Humidity":"60"}}}    |

## Next steps

- [Create IoT alerts and convert IoT alerts into work orders](cfs-iot-alerts.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
