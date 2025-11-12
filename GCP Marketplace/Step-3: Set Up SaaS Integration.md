# 🔗 Integrate Your App with Google Cloud Marketplace


This section provides an overview of the steps required to **integrate your app with Google Cloud Marketplace**.  
At a high level, integration involves connecting your app’s **backend** and **frontend** with Google Cloud APIs and services.

---

## ⚙️ Backend Integration

You must integrate your app's **backend** with the following **Google APIs and services**:

### 1. 📨 Integrate with Pub/Sub

Receive notifications from Cloud Marketplace — for example, when a user signs up for your product.

- Your **Partner Engineer** creates a **Pub/Sub topic** that you must subscribe to for receiving notifications.
- For detailed steps, refer to the [Pub/Sub Subscriber Guide](https://cloud.google.com/pubsub/docs/subscriber).

---

### 2. 💼 Integrate with the Partner Procurement API

Use the **Partner Procurement API** to:

- Create accounts for customers  
- Link those accounts with their Cloud Marketplace purchase  
- Update linked accounts when users **change or cancel their subscription plans**

> **API Reference:**  
> [Partner Procurement API Documentation](https://cloud.google.com/marketplace/docs/partners/saas/enabling-procurement)

---

### 3. 📊 Integrate with Service Control (for Usage-Based Pricing)

If you've chosen a **usage-based pricing model**, integrate with **Service Control** to **report usage information**.

> **Guide:** [Service Control Overview](https://cloud.google.com/service-infrastructure/docs/service-control/reference/rest)

---

### 📘 Learn More

For detailed information on integrating your app's backend with Cloud Marketplace, see:  
👉 [Configure your app's backend](https://cloud.google.com/marketplace/docs/partners/saas/configure-backend)

For a complete example with sample code, visit:  
👉 [Codelab: Integrating a SaaS product with Cloud Marketplace](https://codelabs.developers.google.com/cloud-marketplace-saas-integration)

---

## 🖥️ Frontend Integration

In your app’s **frontend**, you must set up the following integrations:

### 1. 🧾 Provide a Sign-Up Page

Create a **sign-up page** for new customers who buy your product through Cloud Marketplace.

When users visit this page, **Google sends a JSON Web Token (JWT)** containing the user’s **account ID**.  
Use this ID to:
- Link the user's account in your app with their Google Account  
- Manage **Identity and Access Management (IAM)**

> **Note:**  
> A single user might have multiple Google Cloud account IDs, or multiple users might share one account ID, depending on how their organization manages Google Cloud.

<img width="1012" height="152" alt="image" src="https://github.com/user-attachments/assets/8dc0a704-1f69-4ea5-8119-68b5310f4927" />

---

### 2. 🔐 Provide a Login Page

Offer a **login page** for existing customers to access your product.

---

### 3. 🔁 Optional: Integrate Single Sign-On (SSO)

You can optionally integrate **Google SSO** so that customers can sign in with their Google Accounts.

When using SSO:
- Google sends a **JWT** containing user details.
- Your app must **verify the JWT** for authentication.

> **Guide:** [Integrating your app's frontend](https://cloud.google.com/marketplace/docs/partners/saas/integrate-frontend)

---

## 🚀 Before You Begin

Verify that your **Partner Engineer** has enabled access to the **Cloud Commerce Partner Procurement API**.

Once access is granted, you do **not** need to manually enable the API in the **Google Cloud Console**.

> **Reference:** [Partner Procurement API Setup](https://cloud.google.com/marketplace/docs/partners/saas/enabling-procurement)

---

## 🧰 Integrate with Google APIs

You can integrate your app with Google APIs using **client libraries**, which provide programmatic access to Google Cloud services.

Client libraries are available for most popular platforms, including **Java**, **Python**, and **.NET**.

### 📦 Installing Client Libraries

Install the client libraries for your platform from the  
👉 [Google API Client Libraries page](https://developers.google.com/api-client-library).

---

### ✅ With Client Libraries, You Can:

- Connect to your **Pub/Sub** subscription and handle incoming messages.  
- Connect to the **Service Control API** (if using usage-based pricing) to report usage data to Google.  
- Create linked customer accounts and update them via the **Partner Procurement API**.

---

### 🧩 Building a New Client Library for Partner Procurement API

The **Partner Procurement API** is **restricted**, so you must **build your own client library** using the API discovery document.

To do this:

1. Install the **Google client libraries** for your platform.
2. Build the new library using the API discovery document located at:

[https://cloudcommerceprocurement.googleapis.com/$discovery/rest?version=v1](https://cloudcommerceprocurement.googleapis.com/$discovery/rest?version=v1)


3. For example, in **Python**, use the `build()` method to create a client library.

> 🧠 **Example Code:**  
> For sample code that builds a client library, see the [Codelab samples on GitHub](https://github.com/googlecodelabs/).

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
