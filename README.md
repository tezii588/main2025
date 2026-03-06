ARCHITECTURE BREAKDOWN
Pattern: Modular Monolith with a decoupled Frontend.
Backend Architecture: Layered approach:
Router Layer: Handles HTTP requests and status codes.
Schema Layer: Pydantic models for request/response serialization.
Model Layer: Beanie ODM for database persistence.
Service Layer (Scraper): Independent background orchestrator for data ingestion.
Frontend Architecture: Component-based React with Tailwind CSS and Shadcn UI. State is managed via UserContext and React Query.
Type: NoSQL (MongoDB).
ORM: Beanie (Async ODM for Pydantic).
Key Collections:
users: Core identity, roles, and GDPR timestamps.
profiles: Detailed student/professional metadata.
jobs: Stores both internal and external (scraped) job postings.
applications: Links users to jobs with status (screening, interview, etc.).
scraped_jobs: Raw data store for unprocessed job leads.

# Taiton – Class Fitting Manufacturing CMS & Product Platform

🔗 Website: https://demo.taiton.in/  
🗓️ Developed: 2025  
📍 Industry: Class Fitting Manufacturing  

---

## Project Overview

Taiton is a custom-built Laravel-based CMS and product management platform developed for a **class fitting manufacturing company**.  
The system provides a **highly flexible, admin-controlled page builder**, product catalog management, SEO optimization, and user access control, allowing non-technical users to manage both content and products without code changes.

The project was fully developed and handed over to the client as a complete solution.

---

## Core Objective

- Build a flexible CMS with custom page designs
- Enable product and catalog management similar to an e-commerce structure
- Implement role-based access and permissions
- Provide SEO control for every page
- Support bulk catalog downloads and secure user interactions

---

## Key Features

### Custom CMS & Page Builder
- Fully dynamic pages with custom layouts
- Admin-controlled design components per page
- Flexible block-based page composition
- Articles and content page management
- SEO configuration for each page

### Product & Catalog Management
- Product listing structured by:
  - Categories
  - Sub-categories
  - Items
  - Variants
- Manufacturing-focused product display
- Bulk catalog download functionality

### User & Security Features
- Role-based user and permission control
- OTP-based email verification
- Secure contact form handling

### Admin Panel (FilamentPHP)
- Centralized CMS and product management
- User role and permission configuration
- Content, product, and SEO management
- Secure administrative controls

### Frontend
- Custom UI designs per page
- Responsive layouts using Tailwind CSS
- Dynamic interactions using Livewire

---

## Tech Stack

- Backend: Laravel (PHP)
- Database: MySQL
- Frontend: Livewire, Tailwind CSS
- Admin Panel: FilamentPHP
- Architecture: MVC with role-based access control

---

## My Role & Responsibilities

- Designed and developed the complete website independently
- Built a custom CMS with flexible page layout management
- Implemented product catalog and variant structure
- Integrated SEO management for all pages
- Implemented OTP-based email verification
- Developed bulk catalog download functionality
- Built role-based user access control
- Delivered and handed over the complete solution to the client

---

## Disclaimer

This project was developed for a client and handed over as a complete solution.  
Ongoing maintenance is managed by the client.
