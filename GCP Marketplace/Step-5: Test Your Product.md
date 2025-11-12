# Step-5: Test Your SaaS Product Listing in Google Cloud Marketplace

This section explains how to test usage reporting for **SaaS products listed in Google Cloud Marketplace**.  
Testing ensures that your usage metering and reporting integration works correctly before your product goes live.

---

## 🧭 Before You Begin

Before testing:
- Your product’s **pricing plan must be approved** by Google.
- You must have a **Test Billing Account** configured in your partner project.
- Make sure that:
  - You have turned on **Customer Incremental Insights reports**.
  - You are receiving **usage reports**.
  - Your SaaS **fulfillment and usage reporting APIs** are fully implemented.

📘 Reference: [Test usage reporting for SaaS products | Google Cloud Marketplace](https://cloud.google.com/marketplace/docs/partners/integrated-saas/test-usage-reporting)

---

## 🧪 Step-by-Step: Run a Test to Generate Usage

### Step 1: Switch to Your Test Billing Account
1. In the **Producer Portal**, switch to a Google Cloud project associated with your **Test Billing Account**.
2. From your product’s **Google Cloud Marketplace listing page**, purchase the product using the Test Billing Account.

> 🔹 A Test Billing Account provides 100% discounted usage and allows you to test safely.

---

### Step 2: Send Initial Usage Data
1. Send an initial usage report for a single recognizable metric.
   - It should be more than **US$0.01** but less than one hour of normal usage.
   - Example: if you bill per GiB per hour, report 1 GiB for one hour.

📘 Reference: [Sending usage reports](https://cloud.google.com/marketplace/docs/partners/integrated-saas/usage-reporting)

---

### Step 3: Continue Reporting for 6 Hours
- Send at least **one usage report per hour** for a minimum of **six hours**.  
- Even if you send more frequent reports, the testing period must last at least six hours.

---

### Step 4: Log Usage for Verification
For each report, log usage details in a file (e.g., Google Sheets or CSV) with this format:

Time (UTC) | operationID | startTime | endTime | consumerId | metricName | metricValue

yaml
Copy code

Send this log to your **Google Cloud Marketplace Partner Engineering** contact for validation.

---

### Step 5: Verify Usage Data
After your testing period:
1. Wait for your **Customer Incremental Insights report**.
2. Compare your usage reports with Google’s expected data:
   - `charges`
   - `sku_id`
   - `sku_description`
   - `usage`
   - `unit`
   - `currency`
   - `external_account_id`

Google will verify that your reporting aligns with their ingestion and billing systems.

---

## 🧹 Clean Up After Testing

After verification:
- Stop sending usage reports for the **test entitlements**.
- Cancel all test entitlements created during testing.
- Remove any **Google team members** added to your billing account for validation.

📘 Reference: [Clean up after testing | Google Cloud Marketplace](https://cloud.google.com/marketplace/docs/partners/integrated-saas/test-usage-reporting#cleanup)

---

## 📚 Related Official References

- [Test usage reporting for SaaS products](https://cloud.google.com/marketplace/docs/partners/integrated-saas/test-usage-reporting)  
- [Preview your product in Producer Portal](https://cloud.google.com/marketplace/docs/partners/integrated-saas/preview)  
- [Submit your SaaS product after integration](https://cloud.google.com/marketplace/docs/partners/integrated-saas/submitting)  
- [Usage Reporting API overview](https://cloud.google.com/marketplace/docs/partners/integrated-saas/usage-reporting)

---

✅ **Next Step:** Once testing is complete and verified, proceed to  
**Step-6: Submit Your SaaS Product for Final Review & Publishing** in the Google Cloud Marketplace.

