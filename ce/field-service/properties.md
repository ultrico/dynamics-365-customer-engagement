---
title: Create properties and property templates
description: Learn how to use asset properties in Dynamics 365 Field Service.
ms.date: 06/10/2024
author: jshotts
ms.author: jasonshotts
ms.topic: how-to
ms.custom: bap-template
---

# Create properties and property templates

Properties record important information about customer assets. After you [define properties](#define-properties), you can [create property templates](#create-property-templates) to quickly and easily apply a set of properties to an asset or an entire category of assets. For example, the properties for a laptop can include the type of processor, the amount of RAM, the hard drive size, and the model type.

[Watch a short video about how to create and configure asset properties.](https://www.youtube.com/watch?v=dhruNqBXMgw)

## Define properties

Before you can assign values to properties, you must define them.

1. In Dynamics 365 Field Service, select the **Settings** area.
1. Under **Asset Properties**, select **Property Definitions**.

    :::image type="content" source="media/assets-properties-nav.svg" alt-text="Screenshot of a list of active properties with the New button highlighted.":::

1. Select **New**.
1. Fill in the **Property Name** field.
1. In the **Property Type** field, select the type of property: *Number*, *String* (alphanumeric), *Boolean* (true or false), or *Date/time*.
1. Select **Save & Close**.

## Create property templates

Use property templates to quickly select a group of properties and apply them to an asset or a functional location.

1. In Field Service, select the **Settings** area.
1. Under **Asset Properties**, select **Templates for Properties**.
1. Select **New**.
1. Fill in the **Template Name** field, and then select **Save**.
1. In the **Properties** section, select **New Property Template Association**.
1. To associate an existing property with the template, search for and select it.

    If the property doesn't exist yet, select **New Property Definition** to create it. Go to [Property Definitions](#define-properties). Then add the property to the template.

1. To add another property to the template, select the dropdown arrow to the right of the **Save and Close** button, and then select **Save & Create New**.

    :::image type="content" source="media/assets-properties-templates-properties-lookup-save-new.svg" alt-text="Screenshot of the Quick Create: Property Template Association dialog box with the Save & Create New button highlighted.":::

1. After you finish adding properties, select **Save and Close**.

## Associate asset categories with property templates

Associate a property template with an asset category to quickly add a set of properties to all records in that category.

1. In Field Service, select the **Settings** area.
1. Under **Properties**, select **Templates for Properties**.
1. Select a template.
1. In the **Asset Categories** section, select **New Asset Category Template Association**.

    :::image type="content" source="media/assets-properties-templates.svg" alt-text="Screenshot of the template for properties with the new asset category highlighted.":::

1. To associate an existing asset category with the template, search for and select it.

    If the category doesn't exist yet, select **New Customer Asset Category** to create it. Go to [Asset Categories](assets.md#create-and-assign-asset-categories). Then add the category to the template.

1. To add another category to the template, select the dropdown arrow to the right of the **Save and Close** button, and then select **Save & Create New**.
1. After you finish adding categories, select **Save and Close**.

## Associate assets with property templates

In addition to associating a property template with an asset category, you can associate a template with individual assets.

1. In Field Service, select the **Service** area.
1. Under **Assets**, select **Assets**.
1. Open the customer asset record, and select **Related** > **Asset Template Associations**.
1. Select **New Asset Template Association**.

    :::image type="content" source="media/asset-template-association.svg" alt-text="Screenshot of the asset template association.":::

1. To associate an existing property template with the asset, search for and select it.

    If the template doesn't exist yet, select **New Template for Properties** to create it. Go to [Templates for Properties](#create-property-templates). Then add the template to the asset.

1. To add another property template to the asset, select the dropdown arrow to the right of the **Save and Close** button, and then select **Save & Create New**.
1. After you finish adding templates, select **Save and Close**.

## Associate assets with properties

You can easily assign a set of properties to a customer asset by using a property template. However, you might want to add a property that isn't part of a template, or you might want to add more properties on top of a property template.

1. In Field Service, select the **Service** area.
1. Under **Assets**, select **Assets**.
1. Open the customer asset record, and select **Related** > **Property Asset Associations**.
1. Select **New Property Asset Association**.
1. To associate an existing property with the asset, search for and select it.

    If the property doesn't exist yet, select **New Property Definition** to create it. Go to [Property Definitions](#define-properties). Then add the property to the asset.

1. To add another property to the asset, select the dropdown arrow to the right of the **Save and Close** button, and then select **Save & Create New**.
1. After you finish adding properties, select **Save and Close**.

## Next steps

- [Add property logs](property-logs.md)
- [Build a service history for assets](service-history.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
