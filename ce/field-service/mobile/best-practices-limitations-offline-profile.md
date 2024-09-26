---
title: Best practices and limitations for the offline profile
description: Learn how to use the mobile offline profile to make the best use of the Field Service mobile app when your field technicians don't have Internet access.
ms.topic: overview
ms.subservice: field-service-mobile
ms.date: 08/28/2024
author: JonBaker007
ms.author: jobaker
---

# Best practices and limitations for the offline profile

Field technicians often need to work in areas without Internet access, like remote places or underground. When an admin [sets up the Field Service mobile offline profile](set-up-offline-profile.md), technicians can continue using the mobile app when there's no Internet connection. Important data syncs to the device for viewing in the field. Changes on the device are stored locally, and then uploaded automatically when an Internet connection becomes available.

Read our blog post about [best practices for offline mode](https://cloudblogs.microsoft.com/dynamics365/administrator/2023/11/06/best-practices-for-offline-mode-in-the-field-service-mobile-app-part-1/).

Even if you think your field technicians will always have a reliable Internet connection, we strongly recommend that you set up offline capabilities to create a fast and consistent experience.

The offline profile manages offline record types, relationships, and user assignments. For a guided walkthrough, watch this brief video.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4J8no]

The Field Service mobile app follows the same architecture and security as a Power Apps mobile app. [Learn more about Power Platform security](/power-platform/admin/security/overview#the-application-and-data-on-the-device).

## Best practices for using the offline profile

Before you set up the offline profile, consider these important guidelines:

- **Use the default offline profile**. Although you can create your own mobile offline profile, we highly recommend that you use the default offline profile that's included with Field Service. The **Field Service Mobile - Offline Profile** provides an ideal starting point for offline scenarios. It has common Field Service tables preconfigured for offline use, along with recommended filters to limit the data that's downloaded. Build on it by including your custom record types. Make sure to limit the amount of data you include in the offline profile for the best sync performance.

  The default offline profile receives updates to unchanged table sync filters. You can copy the default profile and make changes to the copy, but the copy is unmanaged and doesn't receive any updates.

  If you make changes to the default offline profile and want to see the latest offline profile later, create a new trial of Field Service.

- **Don't remove default record types from the offline profile**. We purposefully added default record types to make sure that the right data is available to field technicians. Focus on adding the record types you need rather than removing ones you don't.

- **Don't use "All records" as an offline filter**. The offline profile is the gate that controls the amount of data that's downloaded to users' devices. Technically, there's no limit to the number of records the offline profile supports. Practically, however, the less data that's downloaded, the faster and more efficient syncing is. Don't use "All records" as a table filter, and avoid wide date ranges. For example, rather than downloading all customer asset records, download only the records that are related to scheduled work orders. It reduces the number of customer asset records that need to be synced without affecting the work at hand.

- **Use offline JavaScript**. Organizations often need to run workflows on mobile devices to execute business processes. However, Power Automate flows only run when the device has a network connection or on the next sync. If you need to run workflows on the device on-demand and without Internet access, use offline JavaScript instead. [Learn more about workflows and scripts for the Field Service mobile app](automate-business-processes.md).

[Learn more best practices for using mobile apps offline](/power-apps/mobile/mobile-offline-guidelines).

## Limitations of the offline profile

Keep these limitations in mind when you set up the offline profile:

- Records that are created on the device in offline mode and don't meet filter conditions aren't synced until they meet the conditions.

- Make sure that commands or capabilities that are set up for Internet connectivity call the correct APIs: `Xrm.WebApi.online`.

- Tables that support offline use are part of the default **Field Service Mobile - Offline Profile**. You can add tables to the offline profile, but some, such as Purchase Order, Agreements, RTV, and RMA, can't be used offline. If you add these tables and run the app offline, users might get errors.

- The **Field Service Mobile - Offline Profile** can have a maximum of 15 linked tables, including downstream tables. For example, if Table A has a relationship with Tables B, C, and D and Table B has a relationship with Tables F, G, and H, then Table A has six relationships: B, C, D, F, G, and H.

- Inventory validation doesn't run without network connectivity.

- Access to SharePoint documents isn't supported.

- Access to knowledge articles isn't available in offline mode.

- [Web resources are partially supported in offline mode](/power-apps/mobile/offline-capabilities#limitations). We recommend that you use the [Power Apps component framework](/powerapps/developer/component-framework/overview) to implement custom capabilities that work in both the mobile app and the browser.

## Next steps

- [Configure the mobile offline profile](set-up-offline-profile.md)
- [Offline data synchronization](offline-data-sync.md)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
