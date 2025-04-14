---
title: Internal SOP
parent: Internal Docs
nav_order: 2
---

# Standard Operating Procedure: Handling Subscription Cancellation Requests

**Document ID:** SOP-CUST-103  
**Version:** 2.1  
**Last Updated:** April 5, 2025  
**Department:** Customer Success  
**Owner:** Customer Retention Team  

---

## Purpose

This document outlines the standard procedure for handling subscription cancellation requests to ensure a consistent customer experience, maximize retention opportunities, and maintain accurate data for analytics.

---

## Scope

This SOP applies to all Customer Success Representatives and Support Specialists who handle subscription cancellation requests via email, chat, phone, or the customer dashboard.

---

## Prerequisites

- Access to Repeatify Admin Dashboard  
- Access to Shopify Admin  
- Familiarity with the Retention Offer Matrix  
- Completion of Subscription Management Training  

---

## Procedure

### 1. Receiving Cancellation Requests

#### 1.1 Self-Service Cancellations

When a customer cancels through the customer portal:

- An automated notification is sent to the Customer Success team  
- The customer receives an automated cancellation confirmation email  
- The subscription status updates to `Cancelled` in the dashboard  

#### 1.2 Agent-Assisted Cancellations

When a customer requests cancellation via support channels:

1. Log the request in Zendesk and apply the tag: `subscription_cancellation`  
2. Verify customer identity using at least two of the following:  
   - Order number  
   - Email address  
   - Phone number  
   - Last four digits of the payment method  

---

### 2. Understand Cancellation Reason

Determine the reason for cancellation by:

1. Reviewing any reason provided in the customer portal  
2. If not available, ask:  
   _“To help us improve our service, may I ask why you're cancelling your subscription today?”_  
3. Categorize the reason using one of the following tags:  
   - `too_expensive`  
   - `product_issue`  
   - `shipping_issue`  
   - `found_alternative`  
   - `no_longer_needed`  
   - `financial_reasons`  
   - `other` (include specific reason in the notes)  

---

### 3. Retention Attempts

Follow the appropriate retention path based on the customer's reason.

#### 3.1 Price-Related Concerns

- Offer a one-time 20% discount on their next order  
- If declined, suggest reducing order frequency (e.g., bimonthly)  
- If still declined, offer to pause the subscription for 30 days  

#### 3.2 Product Issues

- Offer to replace or resend the product at no cost  
- Recommend an alternative product that may suit their needs better  
- Offer a 30% discount to try a different product  

#### 3.3 Shipping Issues

- Offer free expedited shipping on the next order  
- Adjust the shipping schedule if needed  
- Provide a $10 one-time shipping credit  

#### 3.4 No Longer Needed / Found Alternative

- Offer to pause the subscription for 60–90 days  
- Offer to skip the next shipment  
- As a last resort, offer a win-back discount code for future use  

---

### 4. Processing the Cancellation

If retention is unsuccessful:

1. Go to **Subscriptions → Customer Details** in the Repeatify dashboard  
2. Search for the customer via email or subscription ID  
3. Select **Actions → Cancel Subscription**  
4. Add cancellation reason in the notes  
5. Choose the appropriate reason code from the dropdown  
6. Check “Send cancellation email” unless the customer opts out  
7. Click **Confirm Cancellation**  

---

### 5. Post-Cancellation Actions

After completing the cancellation:

1. Update the Zendesk ticket with:  
   - Cancellation confirmation  
   - Reason code used  
   - Retention offers made  
   - Final resolution  

2. If a retention offer was accepted:  
   - Record which offer was accepted  
   - Set a 30-day follow-up task to check the subscription status  

3. For all cancellations:  
   - Add the customer to the “Cancelled Subscribers” segment in the marketing platform  
   - Trigger automated win-back campaigns at 30, 60, and 90 days  

---

### 6. Special Scenarios

#### 6.1 Subscription Less Than 30 Days Old

- Offer a full refund if the product is unopened  
- For opened products, follow the standard return policy  
- Flag the case for review by the Customer Experience Manager  

#### 6.2 High-Value Customer (LTV > $500)

- Escalate to a Senior Customer Success Representative  
- Authorize up to 40% discount if needed to retain  
- Schedule a personalized follow-up call within 5 business days  

#### 6.3 Technical Difficulties

- Create an urgent ticket for the Technical Support team  
- Reassure the customer their request will be honored  
- Follow up within 24 hours to confirm cancellation  

---

## Metrics and Reporting

Track the following KPIs for all cancellations:

- Cancellation reason  
- Retention offers made  
- Retention success rate  
- Agent handling the request  
- Customer lifetime value (LTV)  
- Subscription duration prior to cancellation  

Reports must be generated weekly and shared with the Customer Success Manager and Product team.

---

## Related Documents

- [Retention Offer Matrix](internal-docs/retention-matrix-v3.pdf)  
- [Subscription Analytics Guide](internal-docs/subscription-analytics.pdf)  
- [Customer Communication Templates](internal-docs/communication-templates.pdf)  
- [Return Policy](policies/returns-and-refunds.pdf)  

---

## Revision History

| Version | Date       | Author       | Changes                                 |
|---------|------------|--------------|------------------------------------------|
| 1.0     | 2024-06-15 | J. Martinez  | Initial document                         |
| 1.5     | 2024-09-03 | L. Williams  | Added high-value customer section        |
| 2.0     | 2025-01-20 | M. Johnson   | Updated retention offers                 |
| 2.1     | 2025-04-05 | K. Smith     | Added special scenarios section          |

---

## Training and Compliance

All Customer Success team members must:

- Complete SOP training before handling cancellations  
- Score 90% or higher on the SOP quiz  
- Acknowledge all SOP updates within 5 business days  

---

## Questions and Support

For support or clarification:

- **Team Lead:** [retention-lead@repeatify.com](mailto:retention-lead@repeatify.com)  
- **Process Owner:** [customer.experience@repeatify.com](mailto:customer.experience@repeatify.com)  

