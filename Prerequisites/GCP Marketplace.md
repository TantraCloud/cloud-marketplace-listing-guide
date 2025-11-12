# ✅ GCP Marketplace SaaS Listing Prerequisites

# Requirements for Your Product

## Organization Requirements

- Your organization must join and maintain good standing in **Partner Advantage**.
- Your organization must be incorporated in one of the supported regions.  
- Your organization must have a Cloud Marketplace vendor account and payment profile in good standing.

---

## Supported Regions and Currency

| **Region**        | **Currency** |
|--------------------|--------------|
| Belgium            | EUR          |
| Canada             | CAD          |
| Canada             | USD          |
| Finland            | EUR          |
| France             | EUR          |
| Germany            | EUR          |
| Hong Kong          | HKD          |
| India              | USD          |
| Ireland            | EUR          |
| Israel             | ILS          |
| Italy              | EUR          |
| Japan              | JPY          |
| Luxembourg         | EUR          |
| Netherlands        | EUR          |
| Norway             | NOK          |
| Poland             | PLN          |
| Romania            | EUR          |
| Saudi Arabia       | USD          |
| Spain              | EUR          |
| Sweden             | SEK          |
| Switzerland        | CHF          |
| United Kingdom     | GBP          |
| United States      | USD          |

---

## Product Requirements

Your product must be **production-ready** (not alpha or beta) to be publicly listed and sold through Cloud Marketplace.

Your product must be **enterprise-ready**, including:
- A professional online presence  
- A defined sales motion  
- Customer support  
- Adherence to strong security best practices

Your product must not include known vulnerabilities, viruses, spyware, Trojan horses, or other malicious code of any kind.

You must verify to Google Cloud through an approval process during onboarding that you host your software product primarily on **Google Cloud**.  
The following patterns are common approved use cases:

---

### Pattern 1: Entire Product on Google Cloud

Your entire product, and all of its supporting components, run entirely on Google Cloud.  
The following architecture diagram provides an example of this pattern:

![Pattern 1](https://github.com/user-attachments/assets/ff253d87-2323-4fb9-9941-fd3b0c4286fd)

---

### Pattern 2: Compute or Data Plane on Google Cloud

Your product's compute or data plane runs on Google Cloud, but smaller control planes or support infrastructure (such as logging or AI inference) run on-premises or on another cloud.  
Your Google Cloud-hosted compute or data plane must be the resource whose consumption increases the fastest when your users increase their consumption.  
The following architecture diagram provides an example of this pattern:

![Pattern 2](https://github.com/user-attachments/assets/cf251c6f-4745-4393-aaa4-bb4f00ee21f4)

---

### Pattern 3: Data Replication or Backup on Google Cloud

Your storage, backup, replication, or data recovery (DR) product must replicate all data to Google Cloud, while the product's control plane can run on-premises or on other clouds.  
The following architecture diagram provides an example of this pattern:

![Pattern 3](https://github.com/user-attachments/assets/66cce651-4f84-4222-9286-c27b6221a3b3)

---

### Pattern 4: Migration Tooling to Google Cloud

Your product is migration tooling that has Google Cloud as its only destination for migration, but can run on-premises or on another cloud as a migration source.  
The following architecture diagram provides an example of this pattern:

![Pattern 4](https://github.com/user-attachments/assets/6096b1f2-4b9a-4422-a787-64eff126e1d6)

---

### Pattern 5: Monitoring or Security Agents Sending Data to Google Cloud

Your product's compute or data plane runs on Google Cloud.  
Your product's monitoring or security agents can run on-premises or on another cloud, but they must send data to a Google Cloud-hosted environment for storage and analysis.  
The following architecture diagram provides an example of this pattern:

![Pattern 5](https://github.com/user-attachments/assets/c6714cac-f3d6-4b4e-9eea-7d4906a68ee8)

---

### Pattern 6: Dataset Hosted on Google Cloud

Your product is a dataset hosted on and delivered through Google Cloud.  
The following architecture diagram provides an example of this pattern:

![Pattern 6](https://github.com/user-attachments/assets/ba729509-26e6-401a-b553-5e4e139af5f7)

---

### Pattern 7: VM or Kubernetes Product on Google Distributed Cloud

Your product is a virtual machine (VM) or Kubernetes product that's deployed to and runs on devices connected to Google Distributed Cloud.  
Your product might connect to the internet to integrate with other Google Cloud-hosted apps or services.  
The following architecture diagram provides an example of this pattern:

![Pattern 7](https://github.com/user-attachments/assets/5f2f9016-fa14-471d-8199-34c0d3d88852)

---

## Additional Product Conditions

- Your products on Cloud Marketplace must have the same capabilities and features as any versions offered outside Cloud Marketplace.  
- Your data products must **not contain any “personally identifiable sensitive information”** as defined in the *Protecting Americans' Data from Foreign Adversaries Act of 2024.*

---

## Reference & Credit

This guide is based on the official Google Cloud documentation.

**Reference:**  
Google Cloud Marketplace [Official Guide](https://cloud.google.com/marketplace/docs/partners/)  
Duration: ~5 minutes  

Thank you to **Google Cloud Platform (GCP)** for the clear official guidance.

---

**Open Source Cloud Marketplace Documentation**  
© 2025 Tantra Cloud
