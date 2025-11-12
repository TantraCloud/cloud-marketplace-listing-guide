# Step-5: Test Your SaaS Product Listing in Azure Marketplace

Once your SaaS offer is configured and published to the **Preview (Private Plan)** stage, you need to **test the complete end-to-end flow** — from purchase → subscription activation → landing page → provisioning → deprovisioning.

Testing ensures your offer meets Microsoft’s SaaS technical validation and works seamlessly for customers.

---

## 🧭 Objective

To verify that:
- Your SaaS offer can be discovered and purchased from the **Azure Marketplace**
- The **SaaS fulfillment API integration** (via your landing page and webhook) works correctly
- Subscription lifecycle events (Activate, Suspend, Revoke, Unsubscribe) are handled properly
- Customers see correct pricing, terms, and redirection

---

## 🧩 Prerequisites

Before you begin testing:
- Your SaaS offer status in **Partner Center** must be **“Preview”**
- You must have:
  - A valid **Microsoft Entra (Azure AD)** account
  - Access to the **Azure Marketplace Preview URL** (shared after offer submission)
  - Your **Landing Page URL** configured in SaaS Technical Configuration
  - **SaaS Fulfillment API** endpoints implemented and reachable (create, activate, delete)
  - Your application deployed and available for provisioning

---

## 🧪 Step-by-Step Testing Process

### 🟢 Step 1: Access the Private Preview Offer
1. Sign in to [Azure Marketplace Preview Portal](https://portal.azure.com/#blade/Microsoft_Azure_Marketplace/GalleryFeaturedMenuItemBlade)
2. Use the **private offer link** generated in Partner Center (Offer → Preview)
3. You should see your SaaS offer with proper:
   - Name, logo, description
   - Plans and pricing
   - Publisher name

---

### 🟢 Step 2: Purchase the Offer
1. Click **“Set up + subscribe”**
2. Choose the subscription (your own tenant for testing)
3. Select the plan and agree to terms
4. Click **“Subscribe”**

🧭 The flow should:
- Redirect to your **Landing Page**
- Include a `subscriptionId` and `token` in query parameters

**Example URL:**
https://your-landingpage.com/landing?token=abc123&subscriptionId=xxxx

yaml
Copy code

---

### 🟢 Step 3: Handle the Token & Activate the Subscription
Your **Landing Page** should:
1. Validate the token using the **Resolve API**
   - `GET https://marketplaceapi.microsoft.com/api/saas/subscriptions/resolve`
2. Display a user-friendly confirmation message like:
   > “We’ve verified your Azure Marketplace subscription! Click below to complete activation.”

3. When user confirms → call the **Activate API**
   - `POST https://marketplaceapi.microsoft.com/api/saas/subscriptions/{id}/activate`
4. Mark the subscription as *Active* in your system.

✅ **Expected result:**  
The subscription status in Partner Center changes from **PendingFulfillmentStart → Subscribed**

---

### 🟢 Step 4: Verify Events from Microsoft
Check that you receive webhook calls (if configured) for:
- `ChangePlan`
- `ChangeQuantity`
- `Suspend`
- `Reinstate`
- `Unsubscribe`

Make sure your API endpoint returns **HTTP 200 OK** and updates your backend accordingly.

---

### 🟢 Step 5: Test Suspend and Unsubscribe
1. Go to **Partner Center → Test Drive → Manage Subscriptions**
2. Trigger **Suspend** — your app should restrict access
3. Trigger **Unsubscribe** — your app should deprovision the user and clean up data

✅ **Expected result:**  
All lifecycle states (`Subscribed`, `Suspended`, `Unsubscribed`) are correctly handled.

---

## 🧾 Verification Checklist

| Test Area | Expected Result | Status |
|------------|----------------|--------|
| Offer appears in Preview Marketplace | Offer visible with correct metadata | ☐ |
| Landing page loads | Redirected with subscription token | ☐ |
| Resolve API works | Token resolves successfully | ☐ |
| Activation API works | Subscription moves to “Subscribed” | ☐ |
| Suspend event | App access blocked | ☐ |
| Unsubscribe event | App deprovisioned | ☐ |
| Billing Plan Change | Plan updates reflected | ☐ |

---

## 🪙 Post-Testing Actions

After successful validation:
1. Return to **Partner Center → Offer Overview**
2. Change status from **Preview → Go Live**
3. Microsoft team performs a final validation (can take 1-3 business days)
4. Once approved, your offer is **live in Azure Marketplace**

---

## 🧠 Tips & Best Practices

- Always test using a **separate tenant** (not your dev account)
- Store and log all API payloads for debugging
- Include descriptive error messages on your landing page
- Re-run activation test after every code change
- Maintain an internal “SaaS Test Plan” document for reproducibility

---

## 📚 References

- [Azure Marketplace SaaS Fulfillment APIs](https://learn.microsoft.com/en-us/azure/marketplace/partner-center-portal/pc-saas-fulfillment-api-v2)
- [Partner Center Offer Publishing Guide](https://learn.microsoft.com/en-us/azure/marketplace/create-new-saas-offer)
- [Microsoft SaaS Accelerator (Open Source)](https://github.com/Azure/Commercial-Marketplace-SaaS-Accelerator)

---

**✅ You’re done!**  
If all the above steps pass, your SaaS listing is fully functional and ready for public customers.

> 💬 *Need help?*  
> Ask in the [Discussions tab](../../discussions) — the community can guide you.
