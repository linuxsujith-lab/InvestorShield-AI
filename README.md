# InvestorShield-AI
<div align="center">

<img width="1774" height="887" alt="image" src="https://github.com/user-attachments/assets/c7696397-2c76-416a-9f93-401e0cc1fc02" />



<br />

# InvestorShield AI

### Real-time detection of synthetic media and phishing attacks in securities markets

*Multi-modal AI verification for investors, brokers, and regulators — built for SEBI's Securities Market TechSprint 2026*

<br />

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)
[![Build Status](https://img.shields.io/github/actions/workflow/status/your-org/investorshield-ai/ci.yml?branch=main&style=for-the-badge&label=Build)](../../actions)
[![Version](https://img.shields.io/badge/version-0.1.0--alpha-blue?style=for-the-badge)](../../releases)
[![Android](https://img.shields.io/badge/Android-API%2026%2B-3DDC84?style=for-the-badge&logo=android&logoColor=white)](.)
[![Kotlin](https://img.shields.io/badge/Kotlin-1.9-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)](.)
[![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-UI-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white)](.)
[![FastAPI](https://img.shields.io/badge/FastAPI-Backend-009688?style=for-the-badge&logo=fastapi&logoColor=white)](.)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](.)
[![Firebase](https://img.shields.io/badge/Firebase-Backend%20Services-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)](.)
[![AI](https://img.shields.io/badge/AI-Multi--Modal%20Detection-8A2BE2?style=for-the-badge)](.)

[![Stars](https://img.shields.io/github/stars/your-org/investorshield-ai?style=flat-square)](../../stargazers)
[![Forks](https://img.shields.io/github/forks/your-org/investorshield-ai?style=flat-square)](../../network/members)
[![Issues](https://img.shields.io/github/issues/your-org/investorshield-ai?style=flat-square)](../../issues)

<br />

[Overview](#project-overview) · [Features](#features) · [Architecture](#system-architecture) · [Installation](#installation) · [Contributing](#contributing)

</div>

<br />

> **Disclaimer** — InvestorShield AI is an independent research and engineering project submitted to SEBI's Securities Market TechSprint 2026 (Problem Statement 1). It is not affiliated with, endorsed by, or officially adopted by SEBI, NSE, BSE, or any regulatory body unless explicitly stated in a signed partnership agreement.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Screenshots](#screenshots)
- [System Architecture](#system-architecture)
- [Project Structure](#project-structure)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Configuration](#configuration)
- [Firebase Setup](#firebase-setup)
- [AI Configuration](#ai-configuration)
- [Application Flow](#application-flow)
- [Security](#security)
- [Performance](#performance)
- [Testing](#testing)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [Roadmap](#roadmap)
- [Changelog](#changelog)
- [License](#license)
- [Acknowledgements](#acknowledgements)

---

## Project Overview

### What is InvestorShield AI?

InvestorShield AI is a multi-modal detection platform that identifies AI-generated fraud targeting retail and institutional investors — deepfake video, cloned-voice audio, phishing text/email, fraudulent URLs, and fabricated documents — and fuses the results into a single explainable risk score, cross-verified against SEBI's public registered-intermediary registry.

### Why It Exists

Synthetic media generation has outpaced the verification tooling available to retail investors. A fabricated executive video or a cloned voice call can now be produced with only a few seconds of source material, and existing detection tooling is split across disconnected categories: enterprise network-security platforms protect institutional perimeters, KYC vendors verify identity only at account-opening, and generic deepfake detectors carry no financial-market context. InvestorShield AI exists to close the specific gap between these categories — content verification for the investor, at the moment they encounter it, in a securities-market context.

### The Problem It Solves

| Problem | Current State | InvestorShield AI's Approach |
|---|---|---|
| Deepfake executive videos driving fraudulent stock tips | Detected reactively, after distribution and losses | Cross-channel monitoring designed for point-of-distribution detection |
| Cloned-voice fraud calls | No investor-facing verification tooling exists | Acoustic/spectral biometric analysis on submitted audio |
| Phishing impersonating brokers, SEBI, or exchanges | Caught only after a complaint is filed | Real-time URL/domain reputation and NLP authority-language analysis |
| Unregistered intermediary impersonation | No investor-accessible real-time check | Direct cross-verification against SEBI's public registry |
| Fragmented, single-modality detection tools | Vendors solve one modality at a time | Ensemble fusion across video, audio, text, and URL signals into one score |

### Target Users

- **Retail and institutional investors** verifying suspicious content before acting on it
- **Brokers and registered intermediaries** verifying content authenticity prior to distribution
- **Regulatory and surveillance teams** requiring auditable, explainable fraud-detection tooling

### Key Innovations

- Real-time cross-verification against SEBI's public registered-intermediary database
- Multi-modal ensemble fusion (video, audio, image, text, URL) into a single composite, explainable risk score
- Human-in-the-loop escalation workflow for medium/high-risk classifications
- Architecture designed to operate within India's IT Rules Amendment 2026 takedown-speed requirements
- Multilingual detection coverage oriented toward Tier-2/3 Indian investor bases

---

## Features

<table>
<tr><th>Category</th><th>Capability</th><th>Status</th></tr>
<tr><td rowspan="6">AI Detection</td><td>AI Analysis Orchestration</td><td>✅ Stable</td></tr>
<tr><td>Composite Risk Scoring</td><td>✅ Stable</td></tr>
<tr><td>Image Forensics Analysis</td><td>✅ Stable</td></tr>
<tr><td>Video / Deepfake Analysis</td><td>🚧 In Progress</td></tr>
<tr><td>Audio / Voice-Clone Analysis</td><td>🚧 In Progress</td></tr>
<tr><td>Document Analysis (OCR + NLP)</td><td>✅ Stable</td></tr>
<tr><td rowspan="3">Threat Surfaces</td><td>URL / Domain Reputation Analysis</td><td>✅ Stable</td></tr>
<tr><td>Email Header & Body Analysis</td><td>✅ Stable</td></tr>
<tr><td>QR Code Payload Analysis</td><td>🧭 Planned</td></tr>
<tr><td rowspan="2">Detection Output</td><td>Threat Detection & Classification</td><td>✅ Stable</td></tr>
<tr><td>Explainable Evidence Timeline</td><td>✅ Stable</td></tr>
<tr><td rowspan="2">Investor Tooling</td><td>Investor Awareness Modules</td><td>✅ Stable</td></tr>
<tr><td>Reports History & Favorites</td><td>✅ Stable</td></tr>
<tr><td rowspan="1">Market Context</td><td>News & Sentiment Feed</td><td>✅ Stable</td></tr>
<tr><td rowspan="4">Platform</td><td>Authentication (Email + OAuth)</td><td>✅ Stable</td></tr>
<tr><td>Cloud Sync (Firestore)</td><td>✅ Stable</td></tr>
<tr><td>Push Notifications</td><td>✅ Stable</td></tr>
<tr><td>Offline Cache</td><td>🚧 In Progress</td></tr>
<tr><td rowspan="4">Enterprise</td><td>Role-Based Access Control</td><td>🧭 Planned</td></tr>
<tr><td>Admin Dashboard</td><td>🧭 Planned</td></tr>
<tr><td>Configurable Settings</td><td>✅ Stable</td></tr>
<tr><td>Accessibility (WCAG AA)</td><td>🚧 In Progress</td></tr>
<tr><td>UI</td><td>Dark Mode Ready</td><td>🧭 Planned</td></tr>
</table>

---

## Screenshots

<details>
<summary><strong>Expand to view application screenshots</strong></summary>

<br />

| | |
|---|---|
| **Landing** <br /> `/assets/screenshots/landing.png` | **Login** <br /> `/assets/screenshots/login.png` |
| **Dashboard** <br /> `/assets/screenshots/dashboard.png` | **New Scan** <br /> `/assets/screenshots/scan.png` |
| **Analysis Report** <br /> `/assets/screenshots/analysis.png` | **Reports History** <br /> `/assets/screenshots/reports.png` |
| **News & Sentiment** <br /> `/assets/screenshots/news.png` | **Profile** <br /> `/assets/screenshots/profile.png` |
| **Settings** <br /> `/assets/screenshots/settings.png` | **Admin Dashboard** <br /> `/assets/screenshots/admin.png` |

*Screenshot assets are placeholders — replace the referenced files under `/assets/screenshots/` with actual application captures.*

</details>

---

## System Architecture

```mermaid
flowchart TD
    A[Client Applications<br/>Android · Web] --> B[API Gateway<br/>FastAPI]
    B --> C[Authentication Service<br/>Firebase Auth]
    B --> D[Analysis Orchestrator]
    D --> E[AI Service Layer<br/>Provider Abstraction + Circuit Breaker]
    E --> F[Vision Models<br/>Image / Video Forensics]
    E --> G[Audio Models<br/>Voice Biometrics]
    E --> H[NLP Models<br/>Phishing / Authority-Language]
    E --> I[URL Reputation Engine]
    D --> J[SEBI Registry Cross-Verification]
    D --> K[Risk Fusion Engine]
    K --> L[(PostgreSQL<br/>Structured Records)]
    K --> M[(Firestore<br/>Realtime Sync)]
    K --> N[Firebase Cloud Storage<br/>Uploaded Artifacts]
    K --> O[Notification Service<br/>FCM]
    K --> P[Reports Service]
    P --> A
```

<details>
<summary><strong>AI Detection Pipeline</strong></summary>

```mermaid
flowchart LR
    A[Input Ingested<br/>Video / Audio / Image / URL / Text] --> B{Modality Router}
    B --> C[Visual Forensics Model]
    B --> D[Voice Biometric Model]
    B --> E[NLP Phishing Model]
    B --> F[URL / Domain Reputation]
    C --> G[Confidence Scores]
    D --> G
    E --> G
    F --> G
    G --> H[SEBI Registry Cross-Check]
    H --> I[Ensemble Risk Fusion]
    I --> J{Risk Threshold}
    J -->|Low| K[Auto-Clear]
    J -->|Medium / High| L[Human Review Queue]
    L --> M[Analyst Verdict]
    K --> N[Explainable Report Generated]
    M --> N
```

</details>

<details>
<summary><strong>Authentication Flow</strong></summary>

```mermaid
sequenceDiagram
    participant U as User
    participant App as Client App
    participant FB as Firebase Auth
    participant API as FastAPI Backend
    participant DB as PostgreSQL

    U->>App: Enter credentials / OAuth
    App->>FB: signIn(credentials)
    FB-->>App: ID Token
    App->>API: Request + Bearer Token
    API->>FB: Verify ID Token
    FB-->>API: Token Valid + UID
    API->>DB: Fetch / Create user profile
    DB-->>API: User profile
    API-->>App: Authenticated session
```

</details>

<details>
<summary><strong>User Journey</strong></summary>

```mermaid
journey
    title Investor Verification Journey
    section Discover Suspicious Content
      Receives message or video: 3
      Opens InvestorShield AI: 5
    section Submit for Analysis
      Uploads media or link: 5
      Views live analysis progress: 4
    section Review Result
      Reads composite risk score: 5
      Reviews explainable evidence: 5
    section Take Action
      Reports to authorities: 4
      Shares verified result: 4
```

</details>

<details>
<summary><strong>Backend Architecture</strong></summary>

```mermaid
flowchart TB
    subgraph API Layer
        A1[FastAPI Routers]
        A2[Request Validation - Pydantic]
        A3[Rate Limiting Middleware]
    end
    subgraph Service Layer
        B1[Analysis Orchestrator]
        B2[Registry Verification Service]
        B3[Report Generation Service]
        B4[Notification Service]
    end
    subgraph Data Layer
        C1[(PostgreSQL)]
        C2[(Redis Cache)]
        C3[(Firestore)]
        C4[Firebase Storage]
    end
    A1 --> A2 --> A3 --> B1
    B1 --> B2
    B1 --> B3
    B3 --> B4
    B1 --> C1
    B1 --> C2
    B3 --> C3
    B1 --> C4
```

</details>

<details>
<summary><strong>Deployment Architecture</strong></summary>

```mermaid
flowchart LR
    A[GitHub Actions CI/CD] --> B[Container Registry]
    B --> C[Kubernetes Cluster]
    C --> D[FastAPI Pods]
    C --> E[Redis Cluster]
    D --> F[(Managed PostgreSQL)]
    D --> G[Firebase Project]
    C --> H[Ingress + TLS Termination]
    H --> I[CDN / Edge]
    I --> J[Android Client]
    I --> K[Web Client]
```

</details>

<details>
<summary><strong>Database Relationships</strong></summary>

```mermaid
erDiagram
    USERS ||--o{ SCANS : submits
    USERS ||--o{ REPORTS : owns
    SCANS ||--|| REPORTS : generates
    REPORTS ||--o{ EVIDENCE_ITEMS : contains
    USERS ||--o{ USER_PROGRESS : tracks
    LEARNING_MODULES ||--o{ LESSONS : contains
    USER_PROGRESS }o--|| LEARNING_MODULES : references
    REPORTS {
        uuid id PK
        uuid scan_id FK
        uuid user_id FK
        int risk_score
        string risk_label
        string primary_threat_classification
        timestamp created_at
    }
    SCANS {
        uuid id PK
        uuid user_id FK
        string input_type
        string status
        timestamp created_at
    }
    USERS {
        uuid id PK
        string email
        string role
        int total_scans
        int risk_protection_score
    }
```

</details>

---

## Project Structure

```
investorshield-ai/
├── android/                       # Android client (Kotlin + Jetpack Compose)
│   ├── app/src/main/java/...      # Application source
│   │   ├── ui/                    # Composable screens and reusable components
│   │   ├── data/                  # Repositories, local cache, Firestore models
│   │   ├── domain/                # Use cases, business logic
│   │   └── di/                    # Dependency injection modules
│   └── build.gradle.kts
│
├── backend/                       # FastAPI service
│   ├── app/
│   │   ├── api/                   # Route definitions, versioned
│   │   ├── core/                  # Config, security, middleware
│   │   ├── services/              # Analysis orchestration, registry checks
│   │   ├── ai_providers/          # AI provider abstraction + circuit breaker
│   │   ├── models/                # SQLAlchemy / Pydantic models
│   │   └── db/                    # Migrations, session management
│   ├── tests/                     # Unit and integration tests
│   └── requirements.txt
│
├── web/                            # Next.js 14 marketing / dashboard frontend
│   ├── app/                        # App Router pages
│   ├── components/                 # Shared UI components
│   └── lib/                        # API clients, utilities
│
├── firebase/                       # Firestore rules, indexes, Cloud Functions
│   ├── firestore.rules
│   ├── firestore.indexes.json
│   └── functions/
│
├── infra/                          # Docker, Kubernetes manifests, CI/CD configs
│   ├── docker/
│   ├── k8s/
│   └── .github/workflows/
│
├── assets/                         # Banners, screenshots, diagrams
├── docs/                           # Extended technical documentation
├── .env.example                    # Environment variable template
└── README.md
```

---

## Tech Stack

### Languages & Frameworks

| Layer | Technology |
|---|---|
| Mobile Client | Kotlin, Jetpack Compose |
| Web Client | Next.js 14, TypeScript, Tailwind CSS |
| Backend API | Python 3.11, FastAPI |
| Async Task Handling | Celery / background workers |

### Data & Infrastructure

| Component | Technology |
|---|---|
| Primary Database | PostgreSQL |
| Caching Layer | Redis |
| Realtime Sync / Client DB | Firebase Firestore |
| Object Storage | Firebase Cloud Storage |
| Authentication | Firebase Authentication |
| Push Notifications | Firebase Cloud Messaging |

### AI & Detection

| Component | Technology |
|---|---|
| Primary LLM Provider | Claude API (provider-abstracted) |
| Provider Resilience | Circuit breaker pattern across AI providers |
| Vision / Deepfake Analysis | Computer vision model ensemble |
| Audio / Voice Biometrics | Acoustic/spectral analysis models |
| Document Intelligence | OCR + NLP pipeline |

### DevOps & Testing

| Component | Technology |
|---|---|
| Containerization | Docker |
| Orchestration | Kubernetes |
| CI/CD | GitHub Actions |
| Testing | Pytest, JUnit, Compose UI Testing, Locust (load) |

---

## Installation

### Requirements

- Python 3.11+
- Node.js 20+
- JDK 17+ (Android builds)
- Docker & Docker Compose
- A Firebase project with Firestore, Authentication, and Storage enabled

### Clone

```bash
git clone https://github.com/your-org/investorshield-ai.git
cd investorshield-ai
```

### Backend Setup

```bash
cd backend
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
cp ../.env.example .env
uvicorn app.main:app --reload
```

### Web Setup

```bash
cd web
npm install
cp ../.env.example .env.local
npm run dev
```

### Android Setup

```bash
cd android
# Place your google-services.json under android/app/
./gradlew assembleDebug     # Debug build
./gradlew assembleRelease   # Release build
```

---

## Configuration

Create a `.env` file at the project root based on the template below. **Never commit real secrets to version control.**

```bash
# ---------- Application ----------
APP_ENV=development
APP_PORT=8000

# ---------- Database ----------
DATABASE_URL=postgresql://user:password@localhost:5432/investorshield
REDIS_URL=redis://localhost:6379/0

# ---------- Firebase ----------
FIREBASE_PROJECT_ID=
FIREBASE_PRIVATE_KEY=
FIREBASE_CLIENT_EMAIL=
FIREBASE_STORAGE_BUCKET=

# ---------- Authentication ----------
JWT_SECRET=
JWT_EXPIRY_MINUTES=60

# ---------- AI Providers ----------
ANTHROPIC_API_KEY=
OPENAI_API_KEY=
GEMINI_API_KEY=
OLLAMA_URL=

# ---------- External Data ----------
NEWS_API_KEY=
SEBI_REGISTRY_API_URL=
```

---

## Firebase Setup

<details>
<summary><strong>Expand for full Firebase configuration guide</strong></summary>

**Authentication**
Enable Email/Password and Google providers in the Firebase Console under `Authentication → Sign-in method`.

**Firestore**
Provision a Firestore database in Native mode. Deploy the included security rules and indexes:

```bash
firebase deploy --only firestore:rules,firestore:indexes
```

**Storage**
Enable Firebase Storage and configure the bucket referenced in `.env` as `FIREBASE_STORAGE_BUCKET`. Uploaded scan artifacts are stored under `/uploads/{uid}/{scanId}/`.

**Notifications**
Configure Firebase Cloud Messaging and register the server key for backend-triggered push notifications on scan completion and threat alerts.

**Rules**
Firestore rules restrict read/write access on `/users/{uid}`, `/scans`, `/reports`, and `/userProgress` to the owning authenticated user. `/news` and `/learningModules` are public-read, admin-write only. See `firebase/firestore.rules`.

**Indexes**
Composite indexes are required for filtered/sorted queries (e.g., reports filtered by `riskLabel` and ordered by `createdAt`). See `firebase/firestore.indexes.json`.

</details>

---

## AI Configuration

The AI service layer uses a **provider abstraction with circuit breaker pattern**, allowing providers to be swapped or load-balanced without changes to calling code.

```bash
ANTHROPIC_API_KEY=your-key-here
OPENAI_API_KEY=your-key-here
GEMINI_API_KEY=your-key-here
OLLAMA_URL=http://localhost:11434
NEWS_API_KEY=your-key-here
JWT_SECRET=your-secret-here
```

Provider selection, timeout thresholds, and failover behavior are configured in `backend/app/ai_providers/config.py`. When a provider's error rate crosses the configured threshold, the circuit breaker opens and traffic is routed to the next configured provider automatically.

---

## Application Flow

```mermaid
flowchart TD
    A[User Opens App] --> B{Authenticated?}
    B -->|No| C[Login / Register]
    B -->|Yes| D[Home Dashboard]
    D --> E[Initiate New Scan]
    E --> F[Select Input Modality]
    F --> G[Upload to Storage]
    G --> H[Backend Analysis Triggered]
    H --> I[Realtime Progress via Firestore]
    I --> J[Risk Report Generated]
    J --> K[View Report + Evidence Timeline]
    K --> L{Risk Level}
    L -->|Low| M[Archived to Reports History]
    L -->|Medium/High| N[Flagged for Review + Notification Sent]
```

---

## Security

| Domain | Implementation |
|---|---|
| Application Security | OWASP ASVS-aligned controls across API and client layers |
| Authentication | Firebase Authentication with JWT-based session validation on the backend |
| Authorization | Per-resource ownership checks enforced at both Firestore rules and API layer |
| Encryption | TLS in transit; encryption at rest for PostgreSQL and Firebase Storage |
| Input Validation | Strict Pydantic schema validation on all API inputs |
| Prompt Injection Defense | Structured input sanitization and role-separation on all LLM-facing calls |
| Secrets Management | Environment-based secrets, never committed; recommend a managed secrets store in production |
| Logging & Audit | Structured, PII-redacted logging with full audit trail on report generation and review actions |
| Secure Storage | Uploaded artifacts scoped per-user with signed, time-limited access URLs |

---

## Performance

- **Caching** — Redis-backed caching for registry lookups and frequently accessed reference data
- **Lazy Loading** — Paginated Firestore queries for reports and news feeds using cursor-based `startAfter`
- **Background Processing** — Long-running AI analysis executed asynchronously with real-time client updates via Firestore listeners
- **Offline Support** — Local caching of non-sensitive UI state on the Android client (in progress)
- **Optimization** — Connection pooling on PostgreSQL, response compression, and CDN-fronted static assets on the web client

---

## Testing

| Type | Tooling | Scope |
|---|---|---|
| Unit Tests | Pytest, JUnit | Business logic, service layer, utility functions |
| Integration Tests | Pytest + test containers | API endpoints, database interactions, AI provider abstraction |
| UI Tests | Jetpack Compose Testing, Playwright | Android screens, web application flows |
| Performance Tests | Locust | API throughput, concurrent analysis load |
| Security Tests | OWASP ZAP, manual review | Input validation, auth boundary testing |

```bash
# Backend
pytest --cov=app tests/

# Android
./gradlew test connectedAndroidTest

# Web
npm run test
```

---

## Deployment

```mermaid
flowchart LR
    A[Push to main] --> B[GitHub Actions: Lint + Test]
    B --> C[Build Docker Images]
    C --> D[Push to Container Registry]
    D --> E[Deploy to Kubernetes]
    E --> F[Run DB Migrations]
    F --> G[Health Check]
    G --> H[Production Traffic Cutover]
```

- **Docker** — Multi-stage builds for backend and web services; see `infra/docker/`
- **GitHub Actions** — CI pipeline runs linting, unit tests, and integration tests on every pull request; CD pipeline builds and deploys on merge to `main`
- **Android Release** — Signed release builds via `./gradlew bundleRelease`, published through the Play Console pipeline
- **Firebase** — Firestore rules, indexes, and Cloud Functions deployed via `firebase deploy`
- **Backend / Production** — Kubernetes manifests under `infra/k8s/`, with horizontal pod autoscaling configured on the analysis orchestrator service

---

## Contributing

Contributions are welcome. Please review the guidelines below before opening a pull request.

**Branch Strategy**
- `main` — production-ready, protected branch
- `develop` — integration branch for upcoming release
- `feature/<short-description>` — new features
- `fix/<short-description>` — bug fixes

**Commit Convention**
This project follows [Conventional Commits](https://www.conventionalcommits.org/):

```
feat(scan): add QR code payload extraction
fix(auth): resolve token refresh race condition
docs(readme): update Firebase setup instructions
```

**Code Review**
All pull requests require at least one approving review and a passing CI pipeline before merge.

**Issue Templates**
Use the provided bug report and feature request templates under `.github/ISSUE_TEMPLATE/`.

**Pull Requests**
Keep pull requests scoped to a single concern. Include a clear description of the change, testing performed, and any relevant screenshots for UI changes.

---

## Roadmap

**Completed**
- [x] Core authentication and user profile system
- [x] Document and image analysis pipeline
- [x] URL and email phishing analysis
- [x] Explainable risk report generation
- [x] Investor awareness learning modules

**In Progress**
- [ ] Video deepfake detection pipeline
- [ ] Audio voice-clone biometric analysis
- [ ] Offline caching for the Android client
- [ ] Accessibility audit (WCAG AA)

**Future**
- [ ] Real-time SEBI registry cross-verification API integration
- [ ] Admin dashboard with role-based access control
- [ ] Multilingual detection coverage (Hindi, Tamil, Telugu, Marathi, Bengali)
- [ ] Broker/intermediary verification API (public beta)
- [ ] Regulator surveillance dashboard

---

## Changelog

All notable changes to this project are documented below. This project adheres to [Semantic Versioning](https://semver.org/).

### [0.1.0-alpha] — Unreleased
- Initial project scaffolding across Android, backend, and web clients
- Core authentication and Firestore data model established
- Document, URL, and email analysis pipelines implemented
- Investor awareness module framework added

---

## License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- The open-source maintainers and communities behind FastAPI, Jetpack Compose, Next.js, and Firebase, whose tooling underpins this project
- Public research and advisories referenced during threat-landscape analysis
- All contributors who submit issues, pull requests, and feedback to this repository

This project is developed independently for submission to SEBI's Securities Market TechSprint 2026 and does not imply endorsement, authorship, or official adoption by SEBI or any affiliated regulatory body.

<div align="center">

<br />

**Built with precision for a safer securities market.**

</div>
