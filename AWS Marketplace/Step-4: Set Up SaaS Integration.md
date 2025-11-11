
This guide provides a hands-on lab to enable **SaaS Quick Launch** for your AWS Marketplace SaaS product. Quick Launch simplifies buyer onboarding by automating resource deployment (e.g., IAM roles, Lambda functions) using AWS CloudFormation and securely sharing secrets via AWS Secrets Manager. No more manual copy-pasting!

Based on the official AWS Marketplace documentation and lab exercises.

> **Note:** <img width="3028" height="2490" alt="image" src="https://github.com/user-attachments/assets/7568f5d5-fb59-4493-a919-95e5c8e38ef9" />


**In this task, as the seller, you configure the Quick Launch experience for our selected product.**

Launch the AWS CloudFormation stack to automatically deploy AWS services that demonstrates a landing page for buyers to register or log into your SaaS application after subscribing. You can learn more about this template and its function in the Integrate your SaaS lab .

[**Launch stack**](https://us-east-1.console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/quickcreate?templateURL=https://marketplace-sa-resources.s3.amazonaws.com/sellerworkshop/saas/landing-page-demo.yaml&stackName=saas-lab-demo-landing-page)
[**View template**](https://marketplace-sa-resources.s3.amazonaws.com/sellerworkshop/saas/landing-page-demo.yaml)

**To launch the stack**
- Check the checkbox next to I acknowledge that AWS CloudFormation might create IAM resources and select Create stack.
- Wait 5-10 minutes for the stack to complete.

- <img width="1454" height="104" alt="image" src="https://github.com/user-attachments/assets/1b0d655e-72c8-4efc-88ea-9f68343e9c60" />


When the stack status shows CREATE_COMPLETE, select the Outputs tab for the stack. Copy the value for the SaaSFulfillmentUrl. It looks similar to the following: https://example123.cloudfront.net.

<img width="1449" height="442" alt="image" src="https://github.com/user-attachments/assets/f546d971-f5a4-4c10-bf90-bda571a43cf5" />


[**SaaSFulfillmentUrl**](https://aws.amazon.com/marketplace/management/products/saas)

- Open the SaaS products page  and select the product you wish to enable Quick Launch for. Select View details.
- Select the Fulfillment options tab and choose Activate and configure from the Quick Launch section. This opens a request form.
- Paste the SaaSFulfillmentUrl value copied from the stack outputs in the Sign-in/registration URL field.
- Select Add template and complete the form.

**Title** - Quick Launch product configuration template

**Description** - optional - CloudFormation template description goes here.

**CloudFormation stack name** - quicklaunch-demo-stack

**CloudFormation template URL** - https://mp-saas-integrations.s3.amazonaws.com/cfn-mp-ql-aws-mpsa-quicklaunch-test-project/templates/ql-cross-account-role-sample.template.yaml

<img width="1438" height="240" alt="image" src="https://github.com/user-attachments/assets/ce5131af-1b1a-46e9-9336-1a2843570646" />


**Add Manual configuration instructions.**  
Instructions - Manual configuration instructions go here.

**Add a URL to Launch details.**  
Buyers use this URL to launch the software they configure in your Quick Launch experience.  
**Launch URL** - https://example.com

<img width="1467" height="185" alt="image" src="https://github.com/user-attachments/assets/9eb37fea-0156-4627-9caf-534f0b320e84" />


- Select Submit. Wait 1 to 3 minutes for the request to complete.
- In the Change request summary section, select your product title under Entities to return to your product overview page in the seller portal.
- Select the Fulfillment options tab for your product and select Update Quick Launch visibility.
- In the Allowlisted accounts for Quick Launch section, add your test buyer AWS account ID to the comma separated list.
- Select Submit and wait 1 to 3 minutes for the request to complete.


