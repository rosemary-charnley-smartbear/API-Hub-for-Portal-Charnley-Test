# 🚀 Getting Started with the Portal APIs (v. 0.5.0-beta)

Welcome to the **Portal APIs**! This guide will help you get up and running quickly with our β-version API.

---

## 1. Authentication

To interact with these APIs, your first step is to obtain and configure proper authentication. Refer to the **Getting Started → Authentication** section in the SwaggerHub documentation for details on:

- Token generation (e.g., API key or OAuth)
- Required headers for API requests
- Permission scopes and access controls

*(Link to the Authentication section in your documentation or API portal)*

---

## 2. API Endpoints Overview

This API provides full lifecycle management of Portals, Products, Content, Sections, Publishing, Access Requests, and more.

### Key Capabilities

- **Portals**
  - `GET /portals` — List all portals  
  - `POST /portals` — Create a new portal  
  - `GET /portals/{portalId}` — Retrieve portal details  
  - `PATCH /portals/{portalId}` — Update a portal  
  - `DELETE /portals/{portalId}` — Remove a portal  
  :contentReference[oaicite:0]{index=0}

- **Products**
  - `GET /products` — List all products  
  - `POST /products` — Create a product  
  - `GET /products/{productId}` — Retrieve product details  
  - `PATCH /products/{productId}` — Update a product  
  - `DELETE /products/{productId}` — Delete a product  
  :contentReference[oaicite:1]{index=1}

- **Access Requests**
  - `GET /accessRequests` — Fetch pending access requests  
  - `PATCH /accessRequests/{requestId}` — Approve or deny access  
  :contentReference[oaicite:2]{index=2}

- **Content Management**
  - `GET /documents/{documentId}` — Retrieve the content and metadata of a document  
  - `PATCH /documents/{documentId}` — Update document contents  
  :contentReference[oaicite:3]{index=3}

- **Publishing**
  - `PUT /publish` — Publish content changes  
  - `GET` various endpoints for fetching publishing history, published pages/products, and unpublished changes  
  :contentReference[oaicite:4]{index=4}

- **Sections & Table of Contents (ToC)**
  - `GET /sections` — List sections  
  - `GET /sections/{sectionId}` — Retrieve a specific section  
  - ToC operations: `GET`, `POST`, `PATCH`, `DELETE` on `/tableOfContents`  
  :contentReference[oaicite:5]{index=5}

- **Attachments**
  - `GET /attachments` — List all attachments  
  - `POST /attachments/branding` — Upload branding images  
  - `POST /attachments/documentation` — Upload attachment for documentation  
  - `GET /attachments/{attachmentId}/metadata` & `/content` — Retrieve metadata or binary data  
  :contentReference[oaicite:6]{index=6}

- **OpenAPI Definitions**
  - `GET /openapi.json` or `GET /openapi.yaml` — Retrieve the API schema  
  :contentReference[oaicite:7]{index=7}

---

## 3. Quick Start: Sample Request

```bash
curl -X GET "https://api.yourdomain.com/portals" \
     -H "Authorization: Bearer YOUR_TOKEN" \
     -H "Accept: application/json"
{
  "portals": [
    {
      "id": "abc123",
      "name": "Example Portal",
      "description": "Your user-friendly Portal"
      // ... other portal details
    }
  ]
}

---

Let me know if you’d like walkthroughs for specific sections—like publishing content, uploading assets, or automating portal creation!
::contentReference[oaicite:10]{index=10}
