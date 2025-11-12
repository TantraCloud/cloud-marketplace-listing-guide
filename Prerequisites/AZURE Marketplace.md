# 🧾 Azure Marketplace Prerequisites


This section outlines the key **listing requirements** and **best practices** for publishing your **Software as a Service (SaaS)** application on **Microsoft Azure Marketplace**.  

---

# 🧾 Listing Options for SaaS Offers in Microsoft Marketplace

When preparing to **publish a new SaaS offer**, you need to decide which **listing option** best fits your business model.  
The **listing option** determines what additional information you must provide when creating your offer in **Partner Center**.

You’ll define your listing option on the **Offer setup** page as explained in  
[How to create a SaaS offer in Microsoft Marketplace](https://learn.microsoft.com/en-us/azure/marketplace/partner-center-portal/saas-offer-setup).

---

## 📋 SaaS Offer Listing Options

| **Listing Option** | **Transaction Process** | **Can It Be Changed After Publishing?** |
|---------------------|--------------------------|------------------------------------------|
| **Contact me** | The customer contacts you directly from the information in your listing. <br><br> 🧑‍💼 *Publishers are responsible for all aspects of the transaction including order, fulfillment, billing, invoicing, and payment.* | ✅ Yes |
| **Free trial** | The customer is redirected to your target URL via **Microsoft Entra ID**. <br><br> 🧑‍💼 *Publishers handle all transaction processes directly.* | ✅ Yes |
| **Get it now (Free)** | The customer is redirected to your target URL via **Microsoft Entra ID**. <br><br> 🧑‍💼 *Publishers handle all transaction processes directly.* | ✅ Yes |
| **Sell through Microsoft** | Offers sold through Microsoft are **transactable offers**, meaning Microsoft facilitates the exchange of money for your software license. <br><br> 💳 Microsoft bills customers using your chosen pricing model and manages the transaction on your behalf. <br> ☁️ Azure infrastructure usage fees are billed directly to you, the partner — include these costs in your pricing. | ❌ No |

---

## 💡 Notes
- For **Contact me**, **Free trial**, and **Get it now (Free)** offers, publishers must support **all aspects of the software license transaction**, including:
  - Order processing  
  - Fulfillment  
  - Metering  
  - Billing and invoicing  
  - Payment and collection  

- For **Sell through Microsoft**, refer to the section **[SaaS billing](https://learn.microsoft.com/en-us/azure/marketplace/partner-center-portal/saas-billing)** for more details.

---


## 🏷️ Offer Title

- Must consist only of **lowercase letters**, **alphanumeric characters**, **dashes**, or **underscores**.  
- The **title cannot be modified** after the offer is published.  
- The title should **accurately describe your solution offering**.  
- Ensure it **matches your online promotion** and marketing materials.  
- Include **key search terms** to help users discover your app easily.

---

## ⚙️ Technical Information: Configuration

- For SaaS applications, decide whether you want to:
  - Only **list your app**, or  
  - Allow customers to **purchase directly** through **Microsoft Marketplace**.  
- Choose the text for your offer’s **acquisition button** — options include:
  - **Free**
  - **Free Trial**
  - **Contact Me**
- In the pop-up configuration, select one applicable product if your app uses specific Microsoft technologies such as:
  - **Cortana Intelligence**
  - **Power BI Solution Templates**
  - **Power Apps**

---

## 🛒 Online Store Details

### Offer Summary
- This appears on your app’s **search results page**.  
- Maximum **100 characters** allowed.  
- Keep it concise and value-driven.

### Industries
- Choose up to **two industries** that best represent where your app is applicable or has the strongest fit.  
- Avoid selecting unrelated industries.

---

## 🧩 Offer Description

- Supports **simple HTML** tags such as `<p>`, `<em>`, `<ul>`, `<li>`, `<ol>`, and header tags.  
- Maximum **3,000 characters**.  
- Should include **2–3 paragraphs** that clearly explain:
  - Your solution offering  
  - The target audience and industry  
  - The **value proposition** — why it’s beneficial and unique  
- Use **clear, easy-to-understand language** with minimal technical jargon.  
- Each paragraph should start with a short, **summary-style heading**.  
- Use **bullet points** where appropriate to highlight **key benefits**.  
- Maintain **proper spacing** and formatting — think of a **brochure-style** presentation:
  - Visually appealing
  - Simple yet comprehensive
  - Easy to skim and understand at a glance

---

## 🎨 Marketing Artifacts

- **Logos** must display correctly and meet the following requirements:
  - Small: 48 x 48 px (optional)  
  - Medium: 90 x 90 px (optional)  
  - Large: Between 216 x 216 and 350 x 350 px (**required**)  
- Include up to **5 screenshots** in `.PNG` format, with a **resolution of 1280 x 720 pixels**.  
- Ensure your visuals are clean, brand-aligned, and representative of your product interface or functionality.

---

## 🧭 Categories and Industries

- Categories must **accurately reflect your app’s capabilities**.  
- Choose at least one category from the list of available options.  
- Avoid selecting irrelevant categories.  
- Ideally, select **up to three categories** that best describe your solution.  
- If applicable, ensure you also choose an **optimal industry alignment**.

---

## 📇 Lead Management

- Choose where your **customer leads** will be stored.  
- Integrate your CRM system following Microsoft’s official guide:  
  👉 [Get Customer Leads to Connect Your CRM System](https://learn.microsoft.com/en-us/azure/marketplace/partner-center-portal/commercial-marketplace-get-customer-leads)

---

## ☎️ Contacts: Solution Support and Help

You must provide both **engineering** and **support contact information**:

### Engineering Contact
- **Name:** Engineering contact person for your app (receives technical communications).  
- **Email:** Valid email for engineering queries.  
- **Phone:** Phone number in **ISO format**.

### Support Contact
- **Name:** Support contact person for customer issues.  
- **Email:** Valid email for support inquiries.  
- **Phone:** Phone number in **ISO format**.  
- **Support URL:** Public URL of your support page.  

Additional requirements:
- All **support methods** (email, phone, URL) must be listed.  
- If your app offers **paid support**, make it **free during the trial period**.

---

## ⚖️ Legal Requirements

- **Privacy Policy URL:**  
  - Must be a public, accessible link to your product’s **privacy policy**.  
- **Terms of Use:**  
  - Customers must **accept** your app’s terms before trying or purchasing your app.  
- Both the **privacy policy** and **terms of use** should be hosted on a **public website** for transparency.

---

## 🪙 Reference & Credit

This guide is based on the official **Microsoft Azure Marketplace** documentation.

**Reference:**  
Azure Marketplace Official Publishing Guide  
Duration: ~7 minutes  

Thank you to **Microsoft Azure** for the clear and detailed official guidance.

---

<p align="center">
  <strong>Open Source Cloud Marketplace Documentation</strong><br>
   2025 Tantra Cloud
</p>
