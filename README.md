# 🔐 AI-Driven Cybersecurity Threat Prediction Platform

![MIT License](https://img.shields.io/badge/License-MIT-green.svg)
![AI Powered](https://img.shields.io/badge/AI-Powered-purple.svg)
![MERN Stack](https://img.shields.io/badge/Stack-MERN-success.svg)
![Status](https://img.shields.io/badge/Project-Active-success.svg)
![Version](https://img.shields.io/badge/Version-1.0.0-informational.svg)
![Enterprise](https://img.shields.io/badge/Access-Enterprise_Only-blue.svg)

## 🌐 Live Deployment

**Access the platform landing page:** [ai-threatpredict.vercel.app](https://ai-threatpredict.vercel.app/)

**Important Notice**: This is an **enterprise cybersecurity platform**. The login/signin functionality is exclusively available to registered organizations and companies with active subscriptions. Public user registration is not available.

## 📝 Problem Statement

Modern cybersecurity systems heavily rely on human analysts, making them slow, reactive, and error-prone. With the increasing scale and complexity of cyber-attacks, manual monitoring is no longer sufficient. Organizations face challenges with delayed threat detection, overwhelming alert volumes, and limited resources for continuous security monitoring.

## 🎯 Objectives

- Develop AI-driven models for real-time cyber threat detection and prediction
- Implement autonomous agents for continuous network monitoring
- Reduce dependency on human security analysts for routine tasks
- Improve organizational resilience through proactive AI-based defense
- Create an intuitive platform for comprehensive security management

## 📈 Future Scope

- Integration with more threat intelligence feeds and SIEM systems
- Advanced ML models for zero-day attack prediction
- Mobile application for on-the-go security monitoring
- Automated incident response and remediation workflows
- Blockchain-based security log immutability
- IoT and industrial control system security modules
- Compliance automation for regulations (GDPR, HIPAA, PCI-DSS)

## ✨ Key Features

- AI-powered threat prediction and anomaly detection
- Real-time global threat monitoring with 3D visualization
- Comprehensive security scanning suite (Web, API, QR, Static)
- Automated incident management and correlation
- Role-based access control with enterprise security
- Real-time alerting and threat intelligence feed
- Historical data export and compliance reporting

## 📋 Requirements

### Technical Requirements

- Node.js v18+ runtime environment
- Supabase account for backend services
- Modern web browser with JavaScript enabled
- Minimum 4GB RAM for optimal performance
- Stable internet connection for real-time updates

### Functional Requirements

- User authentication and authorization
- Real-time threat monitoring and alerts
- Multiple security scanning capabilities
- Data visualization and reporting
- Export functionality for reports
- AI-based threat prediction
- Incident management system

### Access Requirements

- **Enterprise Subscription**: Platform access requires an active enterprise subscription
- **Organization Account**: Login credentials are provided to registered organizations only
- **Admin Approval**: New users must be approved by organization administrators
- **Domain Verification**: Organization email domain verification for security

## 🔗 Source Code

**GitHub Repository:** [AI-DRIVEN-CYBERSECURITY-THREAT-PREDICTION-PLATFORM](https://github.com/pratikabhang/AI-DRIVEN-CYBERSECURITY-THREAT-PREDICTION-PLATFORM)

## 🏗️ System Architecture

The system follows a modular three-tier architecture:

### Frontend Layer (Presentation Tier)

- **React + TypeScript** application with Vite build tool
- **Tailwind CSS** for responsive UI components
- **Three.js** for 3D visualizations and globe rendering
- **shadcn/ui** for accessible component library

### Backend Layer (Application Tier)

- **Supabase** for authentication and database services
- **Edge Functions** for serverless API endpoints
- **Real-time subscriptions** for live data updates
- **PostgreSQL** database for structured data storage

### AI Layer (Intelligence Tier)

- **Machine Learning models** for anomaly detection
- **Predictive analytics** for threat forecasting
- **Natural Language Processing** for log analysis
- **Pattern recognition** for attack correlation

### Access Control Layer

- **Organization-based authentication**
- **Role-based permissions** (Admin, Analyst, Viewer)
- **Domain whitelisting** for enterprise access
- **Multi-factor authentication** support

## 🏠 Landing Page Features

The public-facing landing page provides information about the platform while restricting access to authorized organizations only:

### Public Information Available

- Platform overview and capabilities
- Feature demonstrations and screenshots
- Case studies and testimonials
- Pricing and subscription information
- Contact form for enterprise inquiries
- Company information and security compliance details

### Restricted Areas (Organization Access Required)

- Dashboard and monitoring tools
- Security scanning functionalities
- Incident management system
- User administration panel
- Real-time threat intelligence
- Report generation and exports

## 🛡️ ThreatPredict Platform Overview

An **agentic AI-based cybersecurity system** that acts as an autonomous guardian, continuously monitoring network traffic, detecting anomalies, predicting threats, and generating real-time security insights. **Exclusively designed for enterprise organizations** with dedicated security teams.

## 📊 ThreatPredict Platform Modules

### **Dashboard**

- **Definition**: Central command center providing real-time security posture overview with key metrics and alerts.
- **Example**: SOC analyst sees "Active Threats: 12", "Risk Score: Medium", and attack attempt graphs from last 24 hours.

### **Scanners**

#### Website Scanner

- **Definition**: Audits websites for vulnerabilities like SQL Injection, XSS, and insecure configurations.
- **Example**: Detects SQL injection vulnerability on `/product?id=1` and recommends parameterized queries.

#### API Scanner

- **Definition**: Analyzes API endpoints for security misconfigurations and OWASP API Top 10 risks.
- **Example**: Flags `GET /api/v1/users` endpoint exposing full user details without proper access control.

#### QR Scanner

- **Definition**: Safely analyzes QR codes for malicious links before user scanning.
- **Example**: Identifies QR code pointing to `http://shady-lnk.biz/claim` as credential phishing domain.

#### Static Analysis

- **Definition**: Examines source code/files without execution to find security flaws and hard-coded secrets.
- **Example**: Detects plain text AWS access key `AKIA...` in Dockerfile line 15.

### **Monitoring**

#### Live Map

- **Definition**: 2D geospatial map showing real-time security events and attack sources globally.
- **Example**: Shows coordinated brute-force attacks from specific country targeting login servers.

#### 3D Globe

- **Definition**: Immersive 3D visualization of global cyber threat trends and botnet activity.
- **Example**: Displays dense clusters of DDoS attack arcs between countries highlighting threat hotspots.

#### Analytics

- **Definition**: In-depth charts and reports on historical threat data for trend analysis.
- **Example**: Shows 300% month-over-month increase in ransomware IOC hits prompting security review.

#### Threat Feed

- **Definition**: Live stream of security alerts, IOCs, and AI-generated threat intelligence.
- **Example**: Alerts about critical CVE-2024-12345 in Apache Web Server affecting 3 company assets.

#### Blocked Attacks

- **Definition**: Log showing successfully prevented attacks by platform security systems.
- **Example**: Lists 100 recently blocked attacks including 78 SQL injection and 22 XSS attempts.

### **AI**

#### Predictions

- **Definition**: ML forecasts of potential future attacks based on historical and current data patterns.
- **Example**: Predicts 87% probability of phishing targeting finance department in next 72 hours.

#### Incidents

- **Definition**: Managed workflow for tracking, investigating, and resolving confirmed security incidents.
- **Example**: Correlates file detection, unusual traffic, and suspicious login into single incident case.

#### Export History

- **Definition**: Export scan reports, logs, and analytics in PDF/CSV/JSON formats for compliance.
- **Example**: Exports quarterly user access logs and vulnerability scans as PDF for auditor review.

#### Users

- **Definition**: Administration panel for role-based access control and user management.
- **Example**: Admin assigns "Analyst" role permitting alert viewing and scans but not system changes.

#### Settings

- **Definition**: Central configuration hub for system preferences, integrations, and notifications.
- **Example**: Configures email and Slack alerts for "Critical" severity threats to #security-alerts channel.

## 🏁 Quick Start

### Prerequisites

- Node.js v18 or higher
- npm or bun package manager
- Supabase account
- **Enterprise subscription** (required for platform access)

### Installation

```bash
npm install
```

### Environment Setup

Create `.env` file in root directory:

```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
VITE_ENTERPRISE_MODE=true
```

### Run Development Server

```bash
npm run dev
```

Visit: `http://localhost:8080`

**Note**: Login functionality will only work with valid organization credentials.

## 🔐 Access Protocol

1. **Organization Registration**: Companies must register through enterprise sales
2. **Domain Verification**: Organization email domains are verified
3. **Admin Setup**: Primary admin account is created by platform administrators
4. **User Invitation**: Admins invite team members using organization email addresses
5. **Role Assignment**: Appropriate security roles assigned based on responsibilities

## 🛠️ Technology Stack

- **Frontend**: React, TypeScript, Vite, Tailwind CSS, Three.js, Recharts
- **Backend**: Supabase (Authentication, Database, Edge Functions)
- **State Management**: TanStack Query, React Hook Form, Zod
- **Security**: JWT, RBAC, Domain-based authentication

## 👥 Team Members (Alphabetical Order)

- Ashutosh
- Avinash
- Gideon
- Imran
- Manisha
- Pratik
- Rajeswari
- Sneha
- Varnik

## 📄 License

MIT License

---

**Source Code**: [GitHub Repository](https://github.com/pratikabhang/AI-DRIVEN-CYBERSECURITY-THREAT-PREDICTION-PLATFORM)

**Enterprise Inquiries**: Contact through landing page form at [ai-threatpredict.vercel.app](https://ai-threatpredict.vercel.app/)
