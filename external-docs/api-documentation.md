---
title: API Documentation
parent: External Docs
nav_order: 1
---

# Repeatify Subscriptions API

## Overview

The **Repeatify Subscriptions API** enables developers to programmatically manage subscription products, customer subscriptions, and subscription workflows on Shopify stores. This RESTful API provides endpoints to create, retrieve, update, and delete subscription-related resources.

---

## Authentication

All API requests require authentication using an API key. Include your API key in the request header:

```http
Authorization: Bearer YOUR_API_KEY
```

To obtain an API key, go to `Settings → API Access` in your Repeatify dashboard.

---

## Base URL

```
https://api.repeatify.io/v1
```

---

## Rate Limits

The API supports up to **100 requests per minute per API key**. If the limit is exceeded, a `429 Too Many Requests` response is returned.

---

## Endpoints

### Subscriptions

#### List Subscriptions

```
GET /subscriptions
```

Retrieves a list of subscriptions with optional filtering.

**Query Parameters:**

| Parameter    | Type     | Description                                      |
|-------------|----------|--------------------------------------------------|
| customer_id | string   | Filter by customer ID                           |
| status      | string   | Filter by status (`active`, `paused`, `cancelled`) |
| product_id  | string   | Filter by product ID                            |
| limit       | integer  | Number of results per page (default: 50, max: 100) |
| page        | integer  | Page number for pagination (default: 1)         |

**Example Request:**

```
GET https://api.repeatify.io/v1/subscriptions?status=active&limit=25
```

**Example Response:**

```json
{
  "subscriptions": [
    {
      "id": "sub_12345",
      "customer_id": "cust_789",
      "product_id": "prod_456",
      "variant_id": "var_123",
      "status": "active",
      "billing_interval": "monthly",
      "next_billing_date": "2025-05-10T00:00:00Z",
      "created_at": "2025-01-15T09:23:47Z",
      "updated_at": "2025-04-01T14:32:10Z"
    }
  ],
  "meta": {
    "total": 157,
    "page": 1,
    "limit": 25
  }
}
```

#### Get Subscription

```
GET /subscriptions/{subscription_id}
```

Retrieves a specific subscription by ID.

**Example Request:**

```
GET https://api.repeatify.io/v1/subscriptions/sub_12345
```

**Example Response:**

```json
{
  "id": "sub_12345",
  "customer_id": "cust_789",
  "product_id": "prod_456",
  "variant_id": "var_123",
  "status": "active",
  "billing_interval": "monthly",
  "next_billing_date": "2025-05-10T00:00:00Z",
  "shipping_address": {
    "name": "Jane Smith",
    "address1": "123 Main St",
    "city": "Portland",
    "state": "OR",
    "zip": "97201",
    "country": "US"
  },
  "line_items": [
    {
      "product_id": "prod_456",
      "variant_id": "var_123",
      "quantity": 1,
      "price": 29.99
    }
  ],
  "created_at": "2025-01-15T09:23:47Z",
  "updated_at": "2025-04-01T14:32:10Z"
}
```

#### Create Subscription

```
POST /subscriptions
```

Creates a new subscription.

**Request Body:**

```json
{
  "customer_id": "cust_789",
  "product_id": "prod_456",
  "variant_id": "var_123",
  "billing_interval": "monthly",
  "quantity": 1,
  "shipping_address": {
    "name": "Jane Smith",
    "address1": "123 Main St",
    "city": "Portland",
    "state": "OR",
    "zip": "97201",
    "country": "US"
  },
  "payment_method_id": "pm_345"
}
```

**Example Response:**

```json
{
  "id": "sub_12345",
  "customer_id": "cust_789",
  "product_id": "prod_456",
  "variant_id": "var_123",
  "status": "active",
  "billing_interval": "monthly",
  "next_billing_date": "2025-05-10T00:00:00Z",
  "created_at": "2025-04-10T09:23:47Z",
  "updated_at": "2025-04-10T09:23:47Z"
}
```

---

## Error Codes

| Code | Description                                      |
|------|--------------------------------------------------|
| 400  | Bad Request – Check your request parameters      |
| 401  | Unauthorized – Invalid API key                   |
| 404  | Not Found – Resource does not exist              |
| 422  | Unprocessable Entity – Request validation failed |
| 429  | Too Many Requests – Rate limit exceeded          |
| 500  | Internal Server Error – Unexpected error         |

---

## Webhooks

Configure webhooks to receive real-time notifications about subscription events. Webhooks can be managed from your Repeatify dashboard under `Settings → Webhooks`.

**Available Events:**

- `subscription.created`
- `subscription.updated`
- `subscription.cancelled`
- `payment.succeeded`
- `payment.failed`

---

## Additional Resources

- [API Changelog](/changelog)
- [Webhook Integration Guide](/webhook-guide)
- [Sample Applications](https://github.com/repeatify/api-examples)

For support, contact: `api-support@repeatify.io` or visit the [Developer Forum](https://community.repeatify.io/developers)

---

