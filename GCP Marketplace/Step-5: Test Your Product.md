# Step-X: Test Your SaaS Product Listing in Google Cloud Marketplace

This section covers how to test usage reporting for SaaS products offered through Google Cloud Marketplace. :contentReference[oaicite:1]{index=1}

---

## Before you begin

- To test usage reporting, your product’s pricing plan must be approved by Google. :contentReference[oaicite:2]{index=2}  
- Make sure you are using a **Test Billing Account**, which has 100% discounted usage. :contentReference[oaicite:3]{index=3}  
- Verify that you’ve turned on Customer incremental insights reports:  
  - Set up to receive reports.  
  - Turn on Customer incremental insights reports. :contentReference[oaicite:4]{index=4}  

---

## Run a test to generate usage

1. In the Producer Portal, switch to a Google Cloud project associated with your **Test Billing Account**. :contentReference[oaicite:5]{index=5}  
2. From your product’s Google Cloud Marketplace listing page, use your Test Billing Account to purchase the product. :contentReference[oaicite:6]{index=6}  
3. Send an initial usage report for a single, recognizable metric. This should equal more than US $0.01, and be less than the amount of usage you expect in one hour of usage. For example, if you bill per GiB per hour, send a usage report equivalent to one GiB per hour. This simplifies verification when comparing with the Customer incremental insights report. :contentReference[oaicite:7]{index=7}  
4. Continue to send at least one usage report per hour for at least six hours. If you send more than one per hour, the minimum length of the test remains six hours. :contentReference[oaicite:8]{index=8}  
5. For the duration of the testing period, create logs that contain usage information you are reporting, e.g., in Google Sheets or CSV, with the following format:  
Time (UTC) | operationID | startTime | endTime | consumerId | metricName | metricValue

yaml
Copy code
Provide these logs (in Google Sheets or CSV) to your Google Cloud Marketplace partner engineering team. :contentReference[oaicite:9]{index=9}  
6. After receiving the Customer incremental insights report for the time period you tested, Google will compare your reported values with expected values in the fields: `charges`, `sku_id`, `sku_description`, `usage`, `unit`, `currency`, `external_account_id`. :contentReference[oaicite:10]{index=10}  

---

## Clean up after testing

Once Google receives and verifies your usage from the testing period:  
- Stop sending usage reports for the entitlements you used for testing. :contentReference[oaicite:11]{index=11}  
- Cancel all entitlements you created for testing. :contentReference[oaicite:12]{index=12}  
- Remove any Google team members you added to your Cloud Billing account during testing. :contentReference[oaicite:13]{index=13}  

---

## Related topics

- Preview your product in Producer Portal to see how it appears to Marketplace users. :contentReference[oaicite:14]{index=14}  
- Preview your product’s pricing plans. :contentReference[oaicite:15]{index=15}  
- Submit your SaaS product after integration. :contentReference[oaicite:16]{index=16}  

---

**✅ After completion:**  
If all testing passes as per the above steps, your SaaS product’s usage reporting integration is validated and you are ready to move forward to the final submission/publishing step.
