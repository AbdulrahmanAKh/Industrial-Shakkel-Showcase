# Shakkel Industrial & Packaging E-Commerce Platform

[![Production Store](https://img.shields.io/badge/Production%20Store-shakkel.store-00c853?style=for-the-badge&logo=googlechrome&logoColor=white)](https://shakkel.store/)
[![License: Commercial / Proprietary](https://img.shields.io/badge/License-Proprietary%20%2F%20NDA-red?style=for-the-badge)](https://shakkel.store/)
[![Framework](https://img.shields.io/badge/Frontend-React%2018%20%7C%20TypeScript%20%7C%20Vite-blue?style=for-the-badge&logo=react)](https://shakkel.store/)
[![Backend](https://img.shields.io/badge/Cloud%20Backend-Supabase%20%7C%20PostgreSQL-3ECF8E?style=for-the-badge&logo=supabase)](https://shakkel.store/)
[![Styling](https://img.shields.io/badge/Styling-Tailwind%20CSS-38B2AC?style=for-the-badge&logo=tailwind-css)](https://shakkel.store/)

Live Production Web Store: [https://shakkel.store/](https://shakkel.store/)  
Client: Shakkel Industrial Trading & Packaging Solutions (Saudi Arabia)  
Role: Full-Stack Software Engineer & Solutions Architect  

---

## Commercial Project and Confidentiality Notice (NDA)

> [!IMPORTANT]
> Proprietary Source Code Notice:  
> This repository serves as a Case Study and Architectural Showcase for the production platform built for Shakkel. In adherence to client confidentiality agreements and commercial non-disclosure agreements (NDA), proprietary business logic, custom payment gateway configurations, and underlying cloud infrastructure keys are not publicly published.
>
> You can experience and test the live, fully deployed e-commerce platform directly at:  
> [https://shakkel.store/](https://shakkel.store/)

---

## Project Overview

Shakkel is an enterprise B2B and B2C digital commerce platform engineered specifically for the Saudi packaging, manufacturing, and industrial supplies sector. The platform bridges the gap between industrial manufacturers, corporate buyers, and retail customers with automated quotation generation, custom order workflows, and real-time inventory management.

### Key Objectives Achieved
- **B2B Bulk Request Engine:** Replaced manual phone/email quoting with an automated dynamic quote generator allowing industrial clients to request tailored specifications and bulk pricing.
- **Sub-Second Performance:** Engineered on top of modern Vite and React 18 SPA architecture with optimized tree-shaking, lazy-loaded routes, and instant caching.
- **Enterprise-Grade Security:** Comprehensive Row Level Security (RLS) enforcement at the PostgreSQL database layer, preventing privilege escalation and securing quotation data.
- **Bilingual and Localized Experience:** Full native Arabic (RTL) and English support adhering to Saudi industrial standards, commercial compliance, and VAT regulations.

---

## Architectural Highlights and Key Modules

```
┌────────────────────────────────────────────────────────────────────────┐
│                        Shakkel Client Layer                            │
│           (React 18 | TypeScript | Tailwind CSS | Shadcn UI)           │
└───────────────────▲────────────────────────────────▲───────────────────┘
                    │                                │
            REST / GraphQL                   WebSocket Streams
                    │                       (Realtime Channel)
┌───────────────────▼────────────────────────────────▼───────────────────┐
│                        Supabase Cloud Infrastructure                   │
│   ┌──────────────────────────┐      ┌──────────────────────────────┐   │
│   │ PostgreSQL Database      │      │ Event Realtime Engine        │   │
│   │ - Strict RLS Policies    │      │ - Instant Ticket Sync        │   │
│   │ - Custom Stored RPCs     │      │ - Live Admin Quote Badges    │   │
│   └──────────────────────────┘      └──────────────────────────────┘   │
│   ┌──────────────────────────┐      ┌──────────────────────────────┐   │
│   │ Edge Functions           │      │ Auth & RBAC Security         │   │
│   │ - Transactional Resend   │      │ - Admin / Client Isolation   │   │
│   │ - WhatsApp Notification  │      │ - Encrypted Sessions         │   │
│   └──────────────────────────┘      └──────────────────────────────┘   │
└────────────────────────────────────────────────────────────────────────┘
```

### 1. Dynamic Quotation and Pricing Engine
- Interactive RFQ (Request for Quotation) pipeline with customizable item matrices.
- Automated tax and discount computing with instant status feedback for commercial buyers.
- Integrated RPC procedures (`create_quote_with_items`) ensuring ACID transaction integrity.

### 2. Real-Time Admin Operations Hub
- Live administrative cockpit for monitoring customer quotation requests, orders, and inquiries.
- WebSocket-powered Supabase Realtime channels eliminating polling delay and providing instant push notifications upon quote submission.
- Executive KPI analytics dashboard tracking conversion rates, quote closure velocity, and popular product lines.

### 3. Role-Based Access Control (RBAC) and Data Protection
- Decoupled `user_roles` architecture from basic public profiles.
- Strict `SECURITY DEFINER` procedures preventing unauthorized privilege elevation.
- Granular PostgreSQL Row Level Security (RLS) ensuring commercial buyers only access their own quotes and order documents.

### 4. Optimized UX for Industrial Buyers
- Advanced multi-filter catalog indexing products by industrial dimensions, materials, and pack quantities.
- Real-time stock status indicators with protective inventory masking.
- Fluid mobile-responsive drawer menus, modal calculators, and friction-free inquiry forms.

---

## Technology Stack

| Layer | Technologies and Tools |
| :--- | :--- |
| **Frontend Framework** | React 18, TypeScript, Vite |
| **Styling and UI System** | Tailwind CSS, Radix UI, Shadcn UI, Lucide Icons |
| **Data Fetching and State** | TanStack React Query v5, Supabase JS Client |
| **Backend and Database** | PostgreSQL, Supabase Cloud, Database Triggers & Functions (RPC) |
| **Realtime Communications** | Supabase Realtime WebSockets |
| **Analytics and Data Viz** | Recharts (Responsive Area, Bar, and Donut KPI Charts) |
| **Deployment and Domain** | Cloudflare SSL / Custom Domain at [shakkel.store](https://shakkel.store/) |

---

## Core Features Implemented

- Interactive Product Catalog: High-performance multi-category browsing with bilingual search.
- Digital RFQ Workflow: Multi-step quote request builder with specifications attachment.
- Live Administrative Panel: Management portal for approving, amending, and issuing quotation PDFs.
- Real-time Ticket and Inquiries System: Integrated customer messaging channel with unread badge synchronizer.
- Automated Notifications: Webhook integration for customer email and WhatsApp status updates.
- Saudi Market Compliance: VAT calculation, invoice formatting, and localized Arabic typography.

---

## Live Application Links

- Production Storefront: [https://shakkel.store/](https://shakkel.store/)
- Contact / Inquiries: [aboodkhatib90@gmail.com](mailto:aboodkhatib90@gmail.com)
- GitHub Profile: [@AbdulrahmanAKh](https://github.com/AbdulrahmanAKh)
- Portfolio: [https://abdulrahmanakh.github.io/Alkhatib-Portfolio/](https://abdulrahmanakh.github.io/Alkhatib-Portfolio/)

---

<p align="center">
  <b>Developed & Engineered by Abdulrahman Alkhatib</b><br>
  <i>Computer Science Graduate | Software & AI Engineer</i>
</p>
