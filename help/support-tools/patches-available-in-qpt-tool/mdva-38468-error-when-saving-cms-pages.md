---
title: "MDVA-38468: Receive an error message when saving CMS page"
labels: QPT patches,Quality Patches Tool,QPT,Support Tools,QPT 1.0.26,Magento Commerce Cloud,Magento Commerce,CMS,error message,2.3.2,2.3.3,2.3.2-p2,2.3.4,2.3.3-p1,2.3.5,2.3.4-p2,2.3.5-p1,2.3.5-p2,Adobe Commerce,on-premises,cloud infrastructure
description: "The MDVA-38468 Adobe Commerce patch fixes the issue where users get the error message: *Item with the same ID \"PAGE_ID\" already exists,* when saving a CMS page. This patch is available when the [Quality Patches Tool (QPT)](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching.html#mqp) 1.0.26 is installed. The patch ID is MDVA-38468. Please note that the issue was fixed in Adobe Commerce 2.3.6."
---

# MDVA-38468: Receive an error message when saving CMS page

The MDVA-38468 Adobe Commerce patch fixes the issue where users get the error message: *Item with the same ID "PAGE_ID" already exists,* when saving a CMS page. This patch is available when the [Quality Patches Tool (QPT)](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching.html#mqp) 1.0.26 is installed. The patch ID is MDVA-38468. Please note that the issue was fixed in Adobe Commerce 2.3.6.

## Affected products and versions

**The patch is created for Adobe Commerce version:**
Adobe Commerce on cloud infrastructure 2.3.2-p2

**Compatible with Adobe Commerce versions:**
Adobe Commerce on-premises and Adobe Commerce on cloud infrastructure 2.3.2-2.3.5-p2

>[!NOTE]
>
>The patch might become applicable to other versions with new Quality Patches Tool releases. To check if the patch is compatible with your Adobe Commerce version, update the `magento/quality-patches` package to the latest version and check the compatibility on the [QPT landing page](https://devdocs.magento.com/quality-patches/tool.html#patch-grid). Use the patch ID as a search keyword to locate the patch.

## Issue

When trying to save a CMS page, you receive the following error message: *Item with the same ID "PAGE_ID" already exists.*

<u>Steps to reproduce</u>:

1. Create a new Website + Store + Storeview.
1. Create one more Website + Store + Storeview.
1. Go to **Content** > **Hierarchy** > Add any existing CMS page to hierarchy tree.
1. Go to **Content** > **Pages** > **Add New Page**:
   * Add any title.
   * In Page in Websites section assign to both created Storeviews.
   * In Hierarchy section assign to any category.
   * **Save and Continue Edit**.

<u>Expected results</u>:

The page is saved without any error.

<u>Actual results</u>:

The page is saved, but you get the following error message: *Item (Magento\VersionsCms\Model\Hierarchy\Node) with the same ID "PAGE_ID" already exists.*

## Apply the patch

To apply individual patches, use the following links depending on your deployment method:

* Adobe Commerce or Magento Open Source on-premises: [Software Update Guide > Apply Patches](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching/mqp.html) in our developer documentation.
* Adobe Commerce on cloud infrastructure: [Upgrades and Patches > Apply Patches](https://devdocs.magento.com/cloud/project/project-patch.html) in our developer documentation.

## Related reading

To learn more about Quality Patches Tool, refer to:

* [Quality Patches Tool released: a new tool to self-serve quality patches](https://support.magento.com/hc/en-us/articles/360047139492) in our support knowledge base.
* [Check if patch is available for your Adobe Commerce issue using Quality Patches Tool](https://support.magento.com/hc/en-us/articles/360047125252) in our support knowledge base.

For info about other patches available in QPT tool, refer to the [Patches available in QPT tool](https://support.magento.com/hc/en-us/sections/360010506631-Patches-available-in-QPT-tool-) section.