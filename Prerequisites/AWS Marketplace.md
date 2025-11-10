# ✅ AWS Marketplace SaaS Listing Prerequisites

Before you can publish your **model package** or **algorithm** in AWS Marketplace, ensure you have the following:

---

## 1. AWS Account
- An active **AWS Account**.
- Supported AWS Regions in AWS Marketplace:

### 🌍 Supported Regions
**North America**
- US East (Ohio)
- US East (N. Virginia)
- US West (N. California)
- US West (Oregon)
- AWS GovCloud (US-East)
- AWS GovCloud (US-West)
- AWS Secret
- Canada (Central)
- Canada West (Calgary)
- Mexico (Central)

**Africa**
- Africa (Cape Town)

**South America**
- South America (São Paulo)

**EMEA**
- Europe (Frankfurt)
- Europe (Ireland)
- Europe (London)
- Europe (Milan)
- Europe (Paris)
- Europe (Spain)
- Europe (Stockholm)
- Europe (Zurich)

**APAC**
- Asia Pacific (Hong Kong)
- Asia Pacific (Hyderabad)
- Asia Pacific (Jakarta)
- Asia Pacific (Malaysia)
- Asia Pacific (Melbourne)
- Asia Pacific (Mumbai)
- Asia Pacific (New Zealand)
- Asia Pacific (Osaka)
- Asia Pacific (Seoul)
- Asia Pacific (Singapore)
- Asia Pacific (Sydney)
- Asia Pacific (Taipei)
- Asia Pacific (Thailand)
- Asia Pacific (Tokyo)

**Middle East**
- Middle East (Bahrain)
- Israel (Tel Aviv)
- Middle East (UAE)

---

## 2. Register as an AWS Marketplace Seller
- Create a **Seller Account** in the [AWS Marketplace Management Portal (AMMP)](https://docs.aws.amazon.com/marketplace/latest/userguide/saas-getting-started.html).
- Provide:
  - Company details
  - Tax information
  - Banking details for payouts  
  *(Approvals can take a few days depending on your region.)*

---

## 3. Access AWS Marketplace Management Portal
- Use the portal to:
  - Register as a seller
  - Create and manage product listings
  - Configure pricing and integration settings

---

## 4. Plan Your SaaS Product
- Define **pricing model**:
  - SaaS Subscription (Pay-as-you-go)
  - SaaS Contract
  - SaaS Contract with Consumption
- Decide on **usage dimensions** (e.g., API calls, storage, users).
- Prepare **customer onboarding workflow** and **billing integration strategy**.

---

## 5. Technical Integration
- Integrate with AWS Marketplace APIs:
  - **Metering Service** for usage-based billing
  - **Entitlement Service** for subscription validation
- Set up **SNS topics** and **SQS queues** for subscription notifications.
- Test integration thoroughly before going live.

---

## 6. Collect Required Assets

- Product logo URL – A publicly accessible Amazon S3 URL that contains a clear image of the logo for the product that you're providing.
- End User License Agreement (EULA) URL – Your product must have a EULA that's available as a PDF file. You must provide a link to an Amazon S3 bucket where customers can review the EULA on your product's AWS Marketplace page.
- Product registration URL – This is the URL where buyers are redirected after successfully subscribing to your product in AWS Marketplace.
- Metadata about your product – You provide the metadata in the product creation wizard of the AWS Marketplace Management Portal.
- Support information for your product – This information includes email addresses and URLs for your product's support channels.

---

- 
## Reference & Credit

This guide is based on the official AWS tutorial video:

> ** Reference** [AWS Official Guide](https://docs.aws.amazon.com/marketplace/latest/userguide/saas-getting-started.html)
> **Channel:** Amazon Web Services  
> **Duration:** ~5 minutes  

**Thank you to AWS for the clear official guidance.**

---

<div align="center">

---

**Open Source Cloud Marketplace Documentation**  
**© 2025 Tantra Cloud**  

</div>
