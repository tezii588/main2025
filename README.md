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

