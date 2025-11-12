# Setting Up Your Software as a Service (SaaS) Product for Google Cloud

bookmark_border  

This page describes the steps to set up your **Google Cloud environment** and add your **product's details** to **Cloud Marketplace**.

---

## 🏗️ Setting Up Your Google Cloud Environment

You must set up your **Google Cloud environment** so that you can distribute your SaaS product.

---

### 🧩 Creating Your Workspace

We recommend that you **create a new project** in the [Google Cloud Console](https://console.cloud.google.com/) primarily for your Cloud Marketplace products.

For the project ID, use the format:

PARTNER_NAME-public


For information about creating projects, see [Creating and managing projects](https://cloud.google.com/resource-manager/docs/creating-managing-projects).

If you already have a project for your current Cloud Marketplace products, you can **re-use that project** and start creating your product in **Producer Portal**.

---

### 🔐 Granting Required IAM Roles

After you create your project, grant the following **Identity and Access Management (IAM)** roles **at the project level**:

| **Service Account** | **Required Roles** |
|----------------------|--------------------|
| `cloud-commerce-marketplace-onboarding@twosync-src.google.com` | Project Editor and Service Management Administrator |
| `cloud-commerce-producer@system.gserviceaccount.com` | Config Editor (`roles/servicemanagement.configEditor`) |

For steps to grant access to your project, see [Granting, changing, and revoking access to resources](https://cloud.google.com/iam/docs/granting-changing-revoking-access).

Grant **one** of the following options to the service account `cloud-commerce-procurement@system.gserviceaccount.com`:

1. **Service Management Administrator** role, **or**  
2. Both of these roles:
   - **Service Consumer** (`roles/servicemanagement.serviceConsumer`)
   - **Service Controller** (`roles/servicemanagement.serviceController`)

> ⚠️ This second option requires using the **Google Cloud CLI**, as these roles aren't visible in the UI.  
> For steps to grant access at the service level, see [Granting and revoking access to the API](https://cloud.google.com/iam/docs/granting-changing-revoking-access#api).

---

## 📝 Submitting Your Product Information

Before you begin setting up and integrating your product, complete the **Cloud Marketplace Project Info Form**.  
You only need to complete this form **once**.

After you have completed the form, your **Partner Engineer** will:

- Give you access to **Producer Portal**
- Enable the following APIs:
  - **Cloud Commerce Partner Procurement API**
  - **Service Control API**

These APIs are used to integrate your product with **Cloud Marketplace**.

---

## 🧭 Creating Your Product in the Producer Portal

You use **Producer Portal** to add your product information, including marketing info, pricing, and integration details.

Your **Partner Engineer** enables **Producer Portal** after you have completed the **Cloud Marketplace Project Info Form**.

To publish your product to Cloud Marketplace, you must submit the following details:

| **Section** | **Description** |
|--------------|----------------|
| **Product Details** | Listing information and marketing info about your product |
| **Pricing** | Pricing model that determines how customers will pay |
| **Technical Integration** | Technical integration details for the SaaS product you are offering |

> ⏳ Some reviews might take up to **two weeks** for approval.  
> We recommend starting early and reviewing the requirements carefully.

> 💡 You can submit **Product Details** and **Pricing** in any order.  
> You must **submit Technical Integration** only **after** your Pricing submission is approved.

At this stage, you only need to **create the entry** for your product in **Producer Portal**.  
You can add marketing information later.

---

### 🔗 Direct Link to Producer Portal

[https://console.cloud.google.com/producer-portal?project=YOUR_PROJECT_ID](https://console.cloud.google.com/producer-portal?project=YOUR_PROJECT_ID)

> **Note:**  
> If you don’t see the link or can’t access the URL:
> - Verify that you’ve selected the correct project.  
> - If the issue persists, contact the **Partner Support Desk** and include the word “Marketplace” in your description.  
> See [Request assistance with Cloud Marketplace](https://cloud.google.com/marketplace/docs/partners/contact).

---

### 🧱 To Create Your Product

1. Click **Add product**.  
2. Under **Solution type**, select **SaaS**.  
3. Under **Product name**, enter your product name and check the **Product ID**.  
   - By default, the **Solution ID** is used in the URL for your listing.  
   - You can customize the URL later when adding product details.  
4. ⚠️ **Caution:** The **solution ID** and **solution type** cannot be changed after creation.  
   You can still edit the product name before submission.  
5. Click **Create**. It may take a few seconds to complete.

---

## 🎨 Adding Product Details

The **product details** include your product listing on Cloud Marketplace, marketing information, and links to documentation.

You use **Producer Portal** to add these details.

---

### 🔗 Access Producer Portal

[https://console.cloud.google.com/producer-portal?project=YOUR_PROJECT_ID](https://console.cloud.google.com/producer-portal?project=YOUR_PROJECT_ID)

> **Note:**  
> If you can’t access the link:  
> - Verify that the correct project is selected.  
> - If you still can’t access it, contact the **Partner Support Desk** and mention “Marketplace”.  
> [Request assistance with Cloud Marketplace](https://cloud.google.com/marketplace/docs/partners/contact)

---

### 🧾 To Add Product Details

1. In the list of products, click the **solution ID** you created.  
2. On the **Overview page**, go to the **Product details** section and click **Edit**.  
3. Complete the **Product info** tab:  
   - Add **Category IDs** to make your product discoverable under certain categories.  
   - You can select **up to two Category IDs**.  
4. ⚙️ **Note:** If your product connects to **Google Distributed Cloud**, add the following text to your product info:  
   > “We recommend that you only purchase this product for a duration equal to or less than the shortest subscription length of your Google Distributed Cloud-connected devices.”
5. Complete the **Documentation** tab:  
   - Add tutorials, documentation, and optional additional license agreements.  
6. Complete the **Product metadata** tab:  
   - Add search metadata, keywords, and optionally customize your product’s detail page URL.

> 🧩 Cloud Marketplace may require additional approvals for certain product categories.  
> If you need to list your product in a category not shown in Producer Portal, use the **special category request form**.

When ready, click **Submit**.  
It takes approximately **2–5 days** for the **Partner Engineering team** to review and approve your product details.  
You can edit details anytime and submit for review later.

---

## 🪙 Reference & Credit

This guide is based on the official **Google Cloud Marketplace** documentation.

**Reference:**  
Google Cloud Marketplace Official Setup Guide  
Duration: ~7 minutes  

Thank you to **Google Cloud Platform (GCP)** for the official guidance.

---

<p align="center">
  <strong>Open Source Cloud Marketplace Documentation</strong><br>
   2025 Tantra Cloud
</p>
