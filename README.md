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
COMPLETE FOLDER STRUCTURE
career-compass-ai-main/
├── backend/                        # FastAPI Backend
│   ├── app/                        # Main Application Logic
│   │   ├── routers/                # API Endpoints (Auth, Jobs, Users, etc.)
│   │   ├── scraper/                # Job Scraping Subsystem
│   │   │   ├── scrapers/           # Specific Scraper Engines (Google, Workday, etc.)
│   │   │   ├── utils/              # Scraper Helpers
│   │   │   └── scraper_orchestrator.py
│   │   ├── main.py                 # Backend Entry Point
│   │   ├── models.py               # Beanie ODM Models (MongoDB)
│   │   ├── schemas.py              # Pydantic Validation Schemas
│   │   ├── database.py             # DB Connection Logic
│   │   └── auth_utils.py           # JWT & Bcrypt Utilities
│   └── requirements.txt            # Python Dependencies
├── src/                            # React Frontend (Vite)
│   ├── components/                 # Reusable UI Components
│   │   ├── ui/                     # Shadcn UI Base Components
│   │   └── dashboard/              # Feature-specific Components
│   ├── pages/                      # Page-level Components
│   ├── contexts/                   # State Management (UserContext)
│   ├── lib/                        # API Client (Axios/Fetch wrapping)
│   └── layouts/                    # Navigation & Shells
├── public/                         # Static Assets
├── package.json                    # Frontend Dependencies
└── tailwind.config.js              # Styling Configuration
