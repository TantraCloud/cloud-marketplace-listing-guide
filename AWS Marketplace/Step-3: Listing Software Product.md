
<!-- AWS Marketplace/Step-3: Listing Software Product.md -->

# Step 3: Listing Your SaaS Product in AWS Marketplace

This guide walks you through creating a **SaaS product listing** in the AWS Marketplace Management Portal, based on the official AWS video:  
[Create a SaaS Product Listing in AWS Marketplace | Amazon Web Services](https://youtu.be/Qk7O7IxeBmI)

> **Note:** <img width="674" height="316" alt="image" src="https://github.com/user-attachments/assets/fb929805-e3b7-44de-b78b-171db500d0eb" />
.

---

## Prerequisites
- You are already registered as an **AWS Marketplace Seller** (Step 1).
- You have provided **Tax & Banking Information** (Step 2).
- You have an active **SaaS application** ready to integrate with AWS Marketplace.
- AWS account with appropriate IAM permissions.

---

## Step-by-Step: Create a SaaS Product Listing

### 1. Log in to AWS Marketplace Management Portal
- Go to: [https://aws.amazon.com/marketplace/management/](https://aws.amazon.com/marketplace/management/)
- Sign in with your **seller account**.

> *(<img width="1787" height="182" alt="image" src="https://github.com/user-attachments/assets/59972e04-2b48-4538-9ad3-660032ac0c51" />)*
<img width="1057" height="514" alt="image" src="https://github.com/user-attachments/assets/397039a7-2a64-49a4-b726-0cc853fa0fbf" />

---

### 2. Navigate to "Create a new offer"
- In the left sidebar, click **"Offers"**.
- Click the **"Create a new offer"** button.

> *(Screenshot placeholder: Offers dashboard)*

---

### 3. Select Product Type
- Choose **"SaaS product"**.


> *(<img width="1047" height="265" alt="image" src="https://github.com/user-attachments/assets/1e49eeee-dc21-4019-a6b4-25074098fdc4" />
)*
- Click **"Generate Product ID and Product Code"**.
<img width="1374" height="800" alt="image" src="https://github.com/user-attachments/assets/b0974fdc-038c-4328-8f18-a181943e6e8b" />

- Save **"Product ID and Product Code for reference"**.
- 
---

### 4. Fill in Basic Product Information
Complete the **"Product overview"** section:

| Field | Description |
|------|-------------|
| **Product title** | Clear, customer-facing name (max 255 chars) |
| **Short description** | 1–2 sentence summary |
| **Long description** | Detailed HTML-rich description |




> *(<img width="1391" height="966" alt="image" src="https://github.com/user-attachments/assets/515e87e7-670e-4e71-b7b7-f8dd30aa0bb7" />
)*
---
***Product logo*** | 216x216 PNG/JPG (recommended) |
***Highlight images*** | Up to 5 promotional images |

<img width="1080" height="807" alt="image" src="https://github.com/user-attachments/assets/2c905d5d-2b00-426d-982e-ae4a89ac39c5" />

---
***Support Information** | Including contact info and supporting links |


<img width="1184" height="851" alt="image" src="https://github.com/user-attachments/assets/a1c7d7c1-5e34-4351-a62c-c33acce93631" />

---
***Product categories** | Select 3 relevant categories (e.g., Developer Tools, Business Applications) 



<img width="1185" height="529" alt="image" src="https://github.com/user-attachments/assets/8ff4cca6-4af9-499a-9726-eafb3cc1efa6" />



 ***Supported countries**  Choose regions where SaaS will be available 
---

### 5. [Configure SaaS Pricing Model](https://docs.aws.amazon.com/marketplace/latest/userguide/pricing-models.html)
Choose one of the supported **SaaS pricing models**:

| Model | Description |
|-------|-----------|
| **SaaS Contract** | Fixed monthly/annual fee |
| **SaaS Contract with Dimensions** | Tiered pricing (e.g., per user, per GB) |
| **SaaS Subscription** | Recurring billing via AWS |


<img width="1416" height="946" alt="image" src="https://github.com/user-attachments/assets/2840b745-15a9-41e0-949f-c47300b6498c" />


#### Example: SaaS Contract with Dimensions
- Define **dimensions** (e.g., `Users`, `Storage`)
- Set **price per unit**
- Enable **free trial** (optional)
### 7. Upload Supporting Documents
Required:
- **Privacy Policy URL**
- **End User License Agreement (EULA)** or use AWS default
- **Support URL**

Optional:
- Product datasheet (PDF)
- Demo video link

> *(<img width="1171" height="811" alt="image" src="https://github.com/user-attachments/assets/50fe78c6-5741-4ecb-83aa-1285085e95da" />
)*

---


  | ***Set Prices*** |
  

<img width="1437" height="961" alt="image" src="https://github.com/user-attachments/assets/43e9ef7c-0e99-4af0-9bc2-37a59f9fea5e" />


| ***Specify Refund Policy*** |


<img width="788" height="394" alt="image" src="https://github.com/user-attachments/assets/4a98e122-ebf1-4697-a8e6-7af859337fa4" />


| ***Configure EULA*** |


<img width="790" height="515" alt="image" src="https://github.com/user-attachments/assets/50fcc0e8-d21a-4a32-aeff-9a1cedd1e7ac" />


| ***Configure Availability*** |


<img width="787" height="526" alt="image" src="https://github.com/user-attachments/assets/6bfd7cb2-0867-4e72-9ad3-26e159e90b47" />


| **Configure Allowlist** |


> **Note:** <img width="541" height="69" alt="image" src="https://github.com/user-attachments/assets/46787be2-0fe2-403f-8570-59538ce22fc8" />


<img width="788" height="476" alt="image" src="https://github.com/user-attachments/assets/9122e7e5-9916-4da2-8e26-e81611517686" />


---

### 8. Review and Submit for Publishing
1. Go to **"Review & Publish"** tab.
2. Verify all sections are complete.
3. Click **"Submit for review"**.

> AWS will review within **3–5 business days**.

> *(Screenshot placeholder: Review summary)*

---

## Post-Submission Steps
| Action | Description |
|------|-------------|
| Monitor status | Check "Offers" dashboard |
| Respond to AWS feedback | Via email or portal |
| Go live | Once approved, listing appears in AWS Marketplace |

---
### Next Steps: Step-4

### Set Up SaaS Integration (Technical Configuration)

#### A. Choose Fulfillment Option
- Select **"SaaS API Integration"** (recommended for automation).

#### B. Provide SaaS Application Endpoint
- Enter your **SaaS landing page URL** (customer redirect after purchase).
- Example: `https://app.your-saas.com/aws-marketplace`

#### C. Configure AWS Marketplace Metering
- Your app must call AWS Marketplace Metering Service to report usage.
- Supported dimensions: `Users`, `Hosts`, `Data`, `Bandwidth`, etc.

  ## Reference & Credit

This guide is based on the official AWS tutorial video:

> **Video:** [How to register as an AWS Marketplace seller | Amazon Web Services](https://youtu.be/w6XECzZOfXY)  
> **Channel:** Amazon Web Services  
> **Duration:** ~5 minutes  

**Thank you to AWS for the clear official guidance.**

---

<div align="center">

---

**Open Source Cloud Marketplace Documentation**  
**© 2025 Tantra Cloud**  

</div>

