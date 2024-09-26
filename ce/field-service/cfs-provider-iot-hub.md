---
title: Create an IoT Provider for Azure IoT Hub
description: Learn how to create an IoT Provider record and specify the associated actions in Dynamics 365 Field Service.
ms.date: 09/04/2024
ms.author: vhorvath
author: vhorvathms
ms.subservice: connected-field-service
ms.topic: how-to
ms.custom: bap-template
ms.search.app: 
  - D365CE
  - D365FS
--- 

# Create an IoT Provider for Azure IoT Hub

An Internet of Things (IoT) provider record specifies the provider type and the associated actions.

1. In Dynamics 365 Field Service, change to the **Settings** area. Under **IoT**, select **Providers**.

1. Select **New** and select **New IoT Provider** in the **IoT Provider** field.

1. Enter a **Name** and choose **Azure IoT Suite**.

   :::image type="content" source="media/iot-hub-provider.png" alt-text="Screenshot of IoT Provider record with details filled in.":::

1. Under Action names, enter the following entities:

   - Register device: *msdyn_IoTHubRegisterDevice*
   - Pull device data: *msdyn_IoTHubPullDeviceData*
   - Get time series device readings: *msdyn_IoTHubQueryDeviceReadings*

1. **Save** the record.

## Next steps

- [Installation and setup - Connected Field Service for Azure IoT Hub](installation-setup-iothub.md)
- [Extensible IoT data sources for Connected Field Service](cfs-custom-iot-provider.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
