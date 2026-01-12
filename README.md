# 🛡️ ThreatPredict: AI-Driven Cybersecurity Threat Prediction Platform

<div align="center">

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE.txt)
[![Security Policy](https://img.shields.io/badge/Security-Policy-important.svg)](SECURITY.md)
[![Open Source](https://img.shields.io/badge/Open%20Source-Yes-brightgreen.svg)](https://github.com/pratikabhang/AI-DRIVEN-CYBERSECURITY-THREAT-PREDICTION-PLATFORM)
[![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Enabled-red.svg)](#)
[![AI Powered](https://img.shields.io/badge/AI-Powered-purple.svg)](#)
[![MERN Stack](https://img.shields.io/badge/Stack-MERN-success.svg)](#tech-stack)
[![Supabase](https://img.shields.io/badge/Backend-Supabase-darkgreen.svg)](#architecture)
[![API](https://img.shields.io/badge/API-REST-orange.svg)](#edge-functions)

</div>

---

## 📋 Table of Contents

- [🎯 Overview](#-overview)
- [🚀 Key Features](#-key-features)
- [🏗️ Architecture](#-architecture)
- [🛠️ Tech Stack](#-tech-stack)
- [📁 Project Structure](#-project-structure)
- [🗄️ Database Schema](#-database-schema)
- [⚡ Edge Functions](#-edge-functions)
- [🏁 Getting Started](#-getting-started)
- [🔐 Security](#-security)
- [📊 Project Resources](#-project-resources)
- [👥 Team](#-team-members)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## 🎯 Overview

**ThreatPredict** is a comprehensive, enterprise-grade cybersecurity monitoring and threat intelligence platform that combines real-time attack visualization, AI-powered threat prediction, and multi-modal security scanning to provide security teams with actionable insights and rapid incident response capabilities.

### 🌐 Live Deployment

**Access the platform:** [ai-threatpredict.vercel.app](https://ai-threatpredict.vercel.app/)

**⚠️ Important Notice:** This is an **enterprise cybersecurity platform**. The login/signin functionality is exclusively available to registered organizations and companies with active subscriptions. Public user registration is not available.

### Why ThreatPredict?

- **Proactive Defense**: AI-driven predictions help identify threats before they materialize
- **Unified Dashboard**: Single pane of glass for all security operations
- **Real-time Monitoring**: Live attack feeds with geographic visualization
- **Automated Response**: Auto-blocking capabilities for critical threats
- **Comprehensive Scanning**: Website, API, QR code, and static file analysis

---

## 🚀 Key Features

### 🛡️ Real-time Threat Monitoring
- **Live Attack Map**: Interactive 2D/3D visualization of global cyber attacks
- **Attack Globe**: Three.js powered 3D globe showing attack origins and targets
- **Threat Feed**: Real-time stream of security incidents with severity classification
- **Analytics Dashboard**: Comprehensive metrics, charts, and trend analysis
- **Blocked Attacks View**: Monitor and manage blocked threats

### 🔍 Multi-Modal Security Scanners
| Scanner | Description | Capabilities |
|---------|-------------|--------------|
| **Website Scanner** | Web application security assessment | XSS, SQLi, CSRF, misconfigurations |
| **API Scanner** | REST API endpoint security audit | Authentication, authorization, injection |
| **QR Scanner** | QR code malware detection | Malicious URLs, phishing attempts |
| **Static Scanner** | File-based security analysis | Malware signatures, suspicious patterns |

### 🤖 AI-Powered Intelligence
- **ThreatDoctor Chat**: Interactive AI assistant for security guidance with conversation persistence
- **Threat Predictions**: ML-driven analysis anticipating potential breaches
- **Auto-generated Recommendations**: Context-aware security suggestions
- **Markdown Rendering**: Rich text responses with syntax-highlighted code blocks

### 👥 Enterprise Management
- **Role-Based Access Control**: Admin, Analyst, Viewer roles
- **User Management**: Complete user lifecycle management
- **Audit Logging**: Comprehensive activity tracking
- **Export History**: Track and manage data exports

---

## 🏗️ Architecture

### System Architecture Diagram

![Architecture](https://github.com/pratikabhang/AI-DRIVEN-CYBERSECURITY-THREAT-PREDICTION-PLATFORM/raw/main/documents/architecture_1.png)

**Multi-tier modular architecture** with AI intelligence layer for real-time threat detection and prediction.

### Architecture Components

```

┌─────────────────────────────────────────────────────────────────────────────────┐
│                              CLIENT LAYER (React SPA)                           │
├─────────────────────────────────────────────────────────────────────────────────┤
│  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐ ┌─────────────┐               │
│  │  Dashboard  │ │  Scanners   │ │  Monitoring │ │  AI Tools   │               │
│  │  ─────────  │ │  ─────────  │ │  ─────────  │ │  ─────────  │               │
│  │ • Stats     │ │ • Website   │ │ • Live Map  │ │ • Threat    │               │
│  │ • Charts    │ │ • API       │ │ • 3D Globe  │ │   Doctor    │               │
│  │ • Alerts    │ │ • QR Code   │ │ • Analytics │ │ • Predict   │               │
│  │ • Actions   │ │ • Static    │ │ • Feed      │ │   ions      │               │
│  └─────────────┘ └─────────────┘ └─────────────┘ └─────────────┘               │
│                                                                                 │
│  ┌──────────────────────────────────────────────────────────────────────────┐  │
│  │                        SHARED COMPONENTS                                  │  │
│  │  AppLayout • ProtectedRoute • Charts • Cards • Tables • Forms            │  │
│  └──────────────────────────────────────────────────────────────────────────┘  │
├─────────────────────────────────────────────────────────────────────────────────┤
│                              STATE MANAGEMENT                                   │
│  ┌──────────────┐  ┌───────────────┐  ┌─────────────────┐                      │
│  │ TanStack     │  │ React Hooks   │  │ Real-time       │                      │
│  │ Query        │  │ (Auth, Stats) │  │ Subscriptions   │                      │
│  └──────────────┘  └───────────────┘  └─────────────────┘                      │
└─────────────────────────────────────────────────────────────────────────────────┘
                                        │
                                        ▼
┌─────────────────────────────────────────────────────────────────────────────────┐
│                            SUPABASE BACKEND                                     │
├─────────────────────────────────────────────────────────────────────────────────┤
│  ┌─────────────────────────────────────────────────────────────────────────┐   │
│  │                         EDGE FUNCTIONS (Deno)                            │   │
│  │  ┌──────────────┐ ┌──────────────┐ ┌──────────────┐ ┌──────────────┐    │   │
│  │  │ scan-website │ │ scan-api     │ │ analyze-qr   │ │ scan-static  │    │   │
│  │  └──────────────┘ └──────────────┘ └──────────────┘ └──────────────┘    │   │
│  │  ┌──────────────┐ ┌──────────────┐ ┌──────────────┐ ┌──────────────┐    │   │
│  │  │threat-doctor │ │ live-threat  │ │ block-entity │ │ export-cloud │    │   │
│  │  │    -chat     │ │   -stream    │ │              │ │              │    │   │
│  │  └──────────────┘ └──────────────┘ └──────────────┘ └──────────────┘    │   │
│  └─────────────────────────────────────────────────────────────────────────┘   │
│                                                                                 │
│  ┌─────────────────────────────────────────────────────────────────────────┐   │
│  │                         POSTGRESQL DATABASE                              │   │
│  │  ┌────────────┐ ┌────────────┐ ┌────────────┐ ┌────────────┐            │   │
│  │  │live_attacks│ │ incidents  │ │ profiles   │ │ user_roles │            │   │
│  │  └────────────┘ └────────────┘ └────────────┘ └────────────┘            │   │
│  │  ┌────────────┐ ┌────────────┐ ┌────────────┐ ┌────────────┐            │   │
│  │  │blocked_*│ │scan_results│ │audit_logs  │ │threat_doc* │            │   │
│  │  └────────────┘ └────────────┘ └────────────┘ └────────────┘            │   │
│  └─────────────────────────────────────────────────────────────────────────┘   │
│                                                                                 │
│  ┌─────────────────────────────────────────────────────────────────────────┐   │
│  │                         AUTHENTICATION (RLS)                             │   │
│  │  • JWT-based authentication    • Row Level Security policies             │   │
│  │  • Role-based access control   • Secure session management               │   │
│  └─────────────────────────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────────────────────────┘
                                        │
                                        ▼
┌─────────────────────────────────────────────────────────────────────────────────┐
│                           EXTERNAL INTEGRATIONS                                 │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐                          │
│  │ Lovable AI   │  │ Gemini API   │  │ Threat Intel │                          │
│  │ Gateway      │  │ (Summaries)  │  │ Feeds        │                          │
│  └──────────────┘  └──────────────┘  └──────────────┘                          │
└─────────────────────────────────────────────────────────────────────────────────┘

```

### Data Flow
```

User Request → React Router → Page Component → Custom Hook → Supabase Client
                                                    │
                    ┌───────────────────────────────┼───────────────────────────────┐
                    │                               │                               │
                    ▼                               ▼                               ▼
            Edge Function                   Database Query                  Real-time
            (scan-*, chat)                  (SELECT/INSERT)                 Subscription
                    │                               │                               │
                    └───────────────────────────────┼───────────────────────────────┘
                                                    │
                                                    ▼
                                            Response/Update
                                                    │
                                                    ▼
                                         UI State Update → Re-render

```

---

## 🛠️ Tech Stack

### Frontend
| Technology | Purpose |
|------------|---------|
| **React 18** | UI component library |
| **TypeScript** | Type-safe development |
| **Vite** | Build tool and dev server |
| **Tailwind CSS** | Utility-first styling |
| **shadcn/ui** | Pre-built UI components |
| **TanStack Query** | Server state management |
| **React Router v6** | Client-side routing |
| **Framer Motion** | Animation library |

### Visualization
| Technology | Purpose |
|------------|---------|
| **Three.js** | 3D globe rendering |
| **@react-three/fiber** | React renderer for Three.js |
| **@react-three/drei** | Three.js helpers |
| **Recharts** | Chart components |
| **react-globe.gl** | Globe visualization |

### Backend (Supabase)
| Technology | Purpose |
|------------|---------|
| **PostgreSQL** | Primary database |
| **Edge Functions (Deno)** | Serverless API endpoints |
| **Row Level Security** | Data access control |
| **Real-time** | Live data subscriptions |
| **Auth** | User authentication |

### AI/ML Integration
| Service | Purpose |
|---------|---------|
| **Lovable AI Gateway** | ThreatDoctor chat assistant |
| **Gemini API** | Threat intelligence summaries |

---

## 📁 Project Structure

```

threat-predict/
├── public/                    # Static assets
│   ├── favicon.svg
│   └── robots.txt
├── src/
│   ├── components/           # React components
│   │   ├── ai/              # AI-related components
│   │   │   └── MarkdownMessage.tsx
│   │   ├── dashboard/       # Dashboard widgets
│   │   │   ├── RiskGauge.tsx
│   │   │   ├── StatCard.tsx
│   │   │   ├── ThreatChart.tsx
│   │   │   └── ThreatFeed.tsx
│   │   ├── layout/          # Layout components
│   │   │   └── AppLayout.tsx
│   │   └── ui/              # shadcn/ui components
│   ├── hooks/               # Custom React hooks
│   │   ├── useAuth.ts       # Authentication hook
│   │   ├── useLiveThreatData.ts
│   │   ├── useSecurityStats.ts
│   │   └── useThreatDoctorChat.ts
│   ├── integrations/        # Third-party integrations
│   │   └── supabase/
│   │       ├── client.ts    # Supabase client
│   │       └── types.ts     # Generated types
│   ├── lib/                 # Utility functions
│   │   └── utils.ts
│   ├── pages/               # Page components
│   │   ├── ai/             # AI features
│   │   │   ├── Predictions.tsx
│   │   │   └── ThreatDoctor.tsx
│   │   ├── monitor/        # Monitoring views
│   │   │   ├── Analytics.tsx
│   │   │   ├── BlockedAttacks.tsx
│   │   │   ├── GlobeView.tsx
│   │   │   ├── LiveMap.tsx
│   │   │   └── ThreatFeed.tsx
│   │   ├── scanner/        # Security scanners
│   │   │   ├── APIScanner.tsx
│   │   │   ├── QRScanner.tsx
│   │   │   ├── StaticScanner.tsx
│   │   │   └── WebsiteScanner.tsx
│   │   ├── users/          # User management
│   │   │   └── Roles.tsx
│   │   ├── Auth.tsx
│   │   ├── Dashboard.tsx
│   │   ├── Incidents.tsx
│   │   ├── Landing.tsx
│   │   ├── Settings.tsx
│   │   └── Users.tsx
│   ├── App.tsx              # Main app component
│   ├── index.css            # Global styles
│   └── main.tsx             # Entry point
├── supabase/
│   ├── functions/           # Edge functions
│   │   ├── analyze-qr/
│   │   ├── block-entity/
│   │   ├── export-to-cloud/
│   │   ├── live-threat-stream/
│   │   ├── monitor-control/
│   │   ├── multi-agent-analysis/
│   │   ├── scan-api/
│   │   ├── scan-static/
│   │   ├── scan-website/
│   │   └── threat-doctor-chat/
│   └── config.toml          # Supabase config
├── .env                      # Environment variables
├── tailwind.config.ts       # Tailwind configuration
└── vite.config.ts           # Vite configuration

```

---

## 🗄️ Database Schema

### Core Tables
| Table | Description |
|-------|-------------|
| `live_attacks` | Real-time attack data with geolocation |
| `blocked_attacks` | History of blocked attacks |
| `blocked_entities` | Blocked IPs/domains |
| `incidents` | Security incident records |
| `scan_results` | Scanner output storage |
| `threats` | Threat intelligence data |

### User Management
| Table | Description |
|-------|-------------|
| `profiles` | User profile information |
| `user_roles` | Role assignments (admin/analyst/viewer) |
| `audit_logs` | User activity audit trail |

### AI Features
| Table | Description |
|-------|-------------|
| `threat_doctor_conversations` | Chat conversation metadata |
| `threat_doctor_messages` | Individual chat messages |

### System Tables
| Table | Description |
|-------|-------------|
| `monitoring_status` | System monitoring state |
| `export_history` | Export operation records |
| `realtime_logs` | System log storage |

---

## ⚡ Edge Functions

| Function | Endpoint | Purpose |
|----------|----------|---------|
| `threat-doctor-chat` | `/functions/v1/threat-doctor-chat` | AI chat assistant |
| `live-threat-stream` | `/functions/v1/live-threat-stream` | Real-time threat data |
| `scan-website` | `/functions/v1/scan-website` | Website vulnerability scan |
| `scan-api` | `/functions/v1/scan-api` | API security audit |
| `analyze-qr` | `/functions/v1/analyze-qr` | QR code analysis |
| `scan-static` | `/functions/v1/scan-static` | Static file analysis |
| `block-entity` | `/functions/v1/block-entity` | Block IP/domain |
| `monitor-control` | `/functions/v1/monitor-control` | Monitoring state control |
| `export-to-cloud` | `/functions/v1/export-to-cloud` | Data export service |
| `multi-agent-analysis` | `/functions/v1/multi-agent-analysis` | Multi-agent threat analysis |

---

## 🏁 Getting Started

### Prerequisites

- **Node.js** v18 or higher
- **npm** or **bun** package manager
- **Supabase** account (for backend services)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd threat-predict
   ```

1. **Install dependencies**

   ```bash
   npm install
   # or
   bun install
   ```

2. **Environment Setup**

   Create a `.env` file in the root directory:

   ```env
   VITE_SUPABASE_URL=your_supabase_url
   VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
   VITE_ENTERPRISE_MODE=true
   ```

3. **Run Development Server**

   ```bash
   npm run dev
   ```

   The application will be available at `http://localhost:8080`

4. **Default Admin Credentials** (for testing/demo)

   ```
   Email: Avinash@tp.com
   Password: 12345678
   ```

### Production Build

```bash
npm run build
npm run preview
```

---

## 🔐 Security

### Authentication & Authorization

- **JWT-based authentication** via Supabase Auth
- **Secure session management** with auto-refresh
- **Role-based access control (RBAC)** with three roles: `admin`, `analyst`, `viewer`
- **Row Level Security (RLS)** policies on all tables
- **Protected routes** for authenticated users only

### Data Protection

- All API keys stored as environment variables
- Sensitive operations require admin role
- Comprehensive audit logging
- Domain-based authentication for enterprise security

### Enterprise Security Features

- **Organization-level isolation** of data
- **Admin approval workflow** for new users
- **Compliance-ready audit trails**
- **Data encryption** at rest and in transit

See [SECURITY.md](./SECURITY.md) for security policy and vulnerability reporting.

---

## 📊 Project Resources

- **SQL Tasks Implementation:** [`sql_task.ipynb`](https://github.com/pratikabhang/AI-DRIVEN-CYBERSECURITY-THREAT-PREDICTION-PLATFORM/blob/main/documents/sql_task.ipynb)
- **Python AI Implementation:** [`python_task.ipynb`](https://github.com/pratikabhang/AI-DRIVEN-CYBERSECURITY-THREAT-PREDICTION-PLATFORM/blob/main/documents/python_task.ipynb)
- **Model Research Paper:** [`model_research.pdf`](https://github.com/pratikabhang/AI-DRIVEN-CYBERSECURITY-THREAT-PREDICTION-PLATFORM/blob/main/documents/model_research.pdf)

- **Platform Demo:** [`demo_video.mp4`](https://github.com/pratikabhang/AI-DRIVEN-CYBERSECURITY-THREAT-PREDICTION-PLATFORM/raw/main/documents/demo_video.mp4)
- **Project Presentation:** [`project_presentation.pptx`](https://github.com/pratikabhang/AI-DRIVEN-CYBERSECURITY-THREAT-PREDICTION-PLATFORM/blob/main/documents/project_presentation.pptx)
- **Agile Project Documentation:** [`project_agile_document.xlsx`](https://github.com/pratikabhang/AI-DRIVEN-CYBERSECURITY-THREAT-PREDICTION-PLATFORM/blob/main/documents/project_agile_document.xlsx)

---

## 📈 Problem Statement

Modern cybersecurity systems heavily rely on human analysts, making them slow, reactive, and error-prone. With the increasing scale and complexity of cyber-attacks, manual monitoring is no longer sufficient. Organizations face challenges with delayed threat detection, overwhelming alert volumes, and limited resources for continuous security monitoring.

---

## 🎯 Objectives

- Develop AI-driven models for real-time cyber threat detection and prediction
- Implement autonomous agents for continuous network monitoring
- Reduce dependency on human security analysts for routine tasks
- Improve organizational resilience through proactive AI-based defense
- Create an intuitive platform for comprehensive security management

---

## 📈 Future Scope

- **Integration with more threat intelligence feeds and SIEM systems**
- **Advanced ML models** for zero-day attack prediction
- **Mobile application** for on-the-go security monitoring
- **Automated incident response** and remediation workflows
- **Blockchain-based** security log immutability
- **IoT and industrial control system** security modules
- **Compliance automation** for regulations (GDPR, HIPAA, PCI-DSS)

---

## 👥 Team Members

- **Ashutosh**
- **Avinash**
- **Gideon**
- **Imran**
- **Manisha**
- **Pratik**
- **Rajeswari**
- **Sneha**
- **Varnik**

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](./LICENSE) file for details.
