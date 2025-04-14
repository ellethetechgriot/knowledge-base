---
title: Shopify User Guide
parent: External Docs
nav_order: 2
---

# Repeatify Shopify Subscription Integration Guide

> **Note:** This guide is a mock technical document for portfolio purposes. **Repeatify** is a fictional Shopify app designed to streamline subscription management for merchants.

---

## Table of Contents
1. [Overview](#overview)
2. [Prerequisites](#prerequisites)
3. [Step 1: Configure Global Settings](#step-1-configure-global-settings)
4. [Step 2: Enable Subscriptions on Products](#step-2-enable-subscriptions-on-products)
5. [Step 3: Customize Subscription Options](#step-3-customize-subscription-options)
6. [Step 4: Customer Portal Setup](#step-4-customer-portal-setup)
7. [Step 5: Email Notifications](#step-5-email-notifications)
8. [Step 6: Add Subscription Widget to Theme](#step-6-add-subscription-widget-to-theme)
9. [Step 7: Test the Subscription Flow](#step-7-test-the-subscription-flow)
10. [Managing Active Subscriptions](#managing-active-subscriptions)
11. [Analytics & Reporting](#analytics--reporting)
12. [Troubleshooting](#troubleshooting)
13. [Support](#support)

---

## Overview
Repeatify makes it easy to offer flexible subscription options on Shopify. This guide walks through the end-to-end process of setting up, customizing, and managing subscriptions with Repeatify.

---

## Prerequisites
- Shopify store (Basic plan or higher)
- Repeatify app installed via Shopify App Store
- Admin-level access
- At least one product created in Shopify

---

## Step 1: Configure Global Settings
1. From your Shopify admin, go to `Apps > Repeatify`
2. Click on `Settings`
3. Set global preferences:
   - **Default Intervals:** Weekly, Bi-weekly, Monthly
   - **Subscription Discount:** % or fixed value
   - **Shipping Behavior:** With every order, or at specified intervals
   - **Payment Processor:** Shopify Payments or third-party gateway

---

## Step 2: Enable Subscriptions on Products
1. Go to `Products > All Products`
2. Click into a product you want to offer as a subscription
3. Scroll to the **Repeatify** panel
4. Toggle **"Enable Subscriptions"** to ON

---

## Step 3: Customize Subscription Options
Within each product’s Repeatify panel:

- **Subscription Type**
  - Subscribe Only
  - One-Time & Subscription (Mixed)

- **Delivery Frequency**
  - Select intervals (e.g. every 1, 2, or 4 weeks)
  - Set a default interval

- **Discounts**
  - Apply percent or flat-rate discount for subscribers

- **Prepaid Plans (Optional)**
  - Enable options such as 3, 6, or 12-month prepaid subscriptions

Click **Save** when done.

---

## Step 4: Customer Portal Setup
1. In the Repeatify app, go to `Customer Portal`
2. Customize the following:
   - Branding (colors, logo)
   - Portal language (e.g. "Manage my plan")
   - Features enabled (e.g. skip, swap, cancel)
   - Cancellation feedback flow (optional)

Click **Save Changes**.

---

## Step 5: Email Notifications
Navigate to `Apps > Repeatify > Notifications` to manage:

| Email Type               | Trigger                          |
|--------------------------|----------------------------------|
| Subscription Confirmed   | New subscription is placed       |
| Upcoming Order Reminder  | X days before renewal            |
| Payment Failed           | Transaction failure              |
| Cancellation Confirmation| User cancels via portal          |

Customize content using the visual editor or HTML.

---

## Step 6: Add Subscription Widget to Theme
1. Go to `Online Store > Themes`
2. Click `Actions > Edit Code`
3. In the `Sections` folder, open `product-template.liquid`
4. Locate the Add-to-Cart block
5. Insert the Repeatify widget snippet:

```liquid
<!--
  Render tag removed for Jekyll compatibility – was used for mock widget:
  {% render 'repeatify-widget', product: product %}
-->
```

6. Save your changes.

---

## Step 7: Test the Subscription Flow
1. Visit the storefront as a customer
2. Add a subscription product to the cart
3. Proceed through checkout
4. Confirm subscription appears in the **Repeatify Dashboard**
5. Access the **Customer Portal** to verify post-purchase controls

---

## Managing Active Subscriptions
- Navigate to `Apps > Repeatify > Subscriptions`
- Search and filter subscriptions by status, email, or product
- Available actions:
  - **Skip Order**
  - **Swap Product**
  - **Update Shipping Info**
  - **Change Payment Method**
  - **Cancel Subscription**

---

## Analytics & Reporting
Find insights under `Apps > Repeatify > Analytics`:

- Active Subscribers
- Monthly Recurring Revenue (MRR)
- Churn Rate
- Lifetime Value (LTV)
- Upcoming Orders

Export all reports in `.csv` format.

---

## Troubleshooting

| Issue                          | Recommended Action                                       |
|-------------------------------|----------------------------------------------------------|
| Widget not displaying         | Verify Liquid snippet is inserted properly              |
| Subscription not applying     | Check that product-level settings are enabled            |
| Payment errors                | Review payment processor and retry transaction           |
| Portal inaccessible           | Confirm portal is enabled in settings                    |

---

## Support
- Email: support@repeatify.app
- Documentation: [Coming Soon]
- Community Forum: [Coming Soon]

---

## License
This documentation is provided for educational and portfolio purposes only. Repeatify is a fictional brand created as part of a mock technical writing sample.


