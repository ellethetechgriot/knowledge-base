---
title: Zendesk Knowledge Article
parent: External Docs
nav_order: 3
---


# Troubleshooting Subscription Payment Issues

> **Last updated**: April 8, 2025  
> **App Reference**: Repeatify (Mock Subscription App for Shopify)

## Overview

This guide helps merchants troubleshoot common subscription payment issues on Shopify using **Repeatify**, a fictional app for recurring orders. Learn how to identify failed payments, resolve customer billing issues, and prevent future disruptions.

---

## Identifying Payment Issues

In your Shopify admin, navigate to:

``Apps → Repeatify → Subscriptions → Payment Issues``

Here, you’ll find flagged subscriptions with:

- **Failed Payment** – Payment method was declined
- **Card Expiring Soon** – Card will expire before the next charge
- **Invalid Payment Method** – Card is no longer valid

![Payment Issues Dashboard Screenshot](/hc/article_attachments/payment-issues-dashboard.png)

---

## Common Payment Failure Reasons

| Error Code         | Description                        | Likely Cause                           |
|--------------------|------------------------------------|----------------------------------------|
| `insufficient_funds` | Not enough funds available         | Low balance on customer’s card         |
| `expired_card`       | Card has expired                   | Customer hasn’t updated card info      |
| `invalid_cvc`        | Incorrect CVC                      | Typo in security code                  |
| `card_declined`      | Card declined by issuing bank      | Various bank-specific reasons          |
| `processing_error`   | Generic payment processor error    | Temporary issue with processor         |

---

## Resolving Failed Payments

### For Merchants

1. **Send Payment Update Request**  
   - Go to: `Subscriptions → Payment Issues`  
   - Select affected customers  
   - Click **Send Payment Update Email**  
   - Customers receive a secure link to update billing info

2. **Manually Update Payment Method**  
   - Open a specific subscription  
   - Click **Edit Payment Method**  
   - Enter new card info provided via phone or chat (if applicable)

3. **Retry a Failed Charge**  
   - From the Payment Issues list, select subscriptions  
   - Click **Retry Charge**  
   - Repeatify will reattempt payment processing immediately

---

### For Customers

When a customer reaches out:

1. Ask them to click the **"Update Payment Method"** link in their email  
2. They’ll be taken to a secure portal to enter new billing info  
3. Once saved, Repeatify will retry the charge automatically

---

## Preventing Future Payment Failures

### 1. Enable Smart Dunning

Smart Dunning retries failed payments automatically using optimized timing:

- Go to: `Settings → Billing`
- Enable **Smart Dunning**
- Recommended retry schedule: 1, 3, and 5 days after failure

### 2. Set Up Pre-Renewal Notifications

Send customers a heads-up before renewal:

- Navigate to: `Settings → Communications`
- Enable **Pre-renewal Notifications**
- Set reminder: 3–5 days before subscription renewal

### 3. Enable Card Expiry Reminders

Automatically notify customers before their card expires:

- Go to: `Settings → Communications`
- Enable **Card Expiration Reminders**
- Recommended: Send 14 days before expiration

---

## Related Articles

- [Setting Up Smart Dunning](../billing/smart-dunning-setup.md)
- [Customizing Communication Templates](../communications/email-template-guide.md)
- [Understanding Subscription Metrics](../analytics/subscription-kpis.md)

---

## Still Need Help?

This is a mock help document, but in a real-world environment you could offer:

- **Email**: support@repeatify.app  
- **Live Chat**: Available in-app during business hours  
- **Phone Support**: 1-800-REPEAT-1 (Mon–Fri, 9am–5pm EST)
