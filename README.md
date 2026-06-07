# 🚗 DriveVerse

**One Identity. Every Vehicle Service.**

India's most advanced vehicle management ecosystem — built with Next.js, FastAPI, PostgreSQL, and Google Gemini AI.

---

## 🌟 Features

| Feature | Description |
|---------|-------------|
| **Vehicle Management** | Add, manage, and track all your vehicles in one garage |
| **Challan Center** | View, pay, and track traffic challans with e-Challan integration |
| **Navigation** | Live GPS navigation with Google Maps, road alerts, speed limits |
| **Astra AI** | AI co-pilot powered by Google Gemini — voice & multilingual (EN/HI/MR) |
| **Document Vault** | Secure DigiLocker integration for DL, RC, Insurance, PUC, Aadhaar |
| **My IDs** | Unified identity dashboard across government services |
| **Insurance Center** | Policy tracking with 30/15/7 day expiry alerts |
| **PUC Center** | Pollution certificate tracking and compliance |
| **Anti-Theft** | Geofencing safe zones, tamper detection, security monitoring |
| **Notifications** | Real-time alerts for challans, expiry, security events |
| **7 Themes** | Neo Black, Light, Dark, Midnight Blue, Aurora, Cyber Glass, Titanium |
| **Settings** | Full customization — theme, language, notifications, security |

---

## 🛠️ Tech Stack

**Frontend**: Next.js 15 · TypeScript · TailwindCSS · Framer Motion  
**Backend**: FastAPI · Python 3.12 · SQLAlchemy (async) · PostgreSQL · Redis  
**AI**: Google Gemini 2.0 Flash (Astra AI)  
**Maps**: Google Maps API  
**Auth**: JWT + bcrypt + OTP (email/SMS) + Google OAuth  
**Deployment**: Docker Compose · Nginx-ready

---

## 🚀 Quick Start

### Prerequisites
- Node.js 20+
- Python 3.12+
- PostgreSQL 16
- Redis 7

### Option 1: Docker Compose (Recommended)
```bash
cp .env.example .env
# Fill in your API keys in .env
docker-compose up -d
```

### Option 2: Manual Setup

**Backend:**
```bash
cd backend
python -m venv venv
venv\Scripts\activate      # Windows
pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000
```

**Frontend:**
```bash
cd frontend
npm install
npm run dev
```

**Open:** http://localhost:3000

---

## 📁 Project Structure

```
DriveVerse/
├── backend/
│   ├── app/
│   │   ├── config.py          # Settings & env vars
│   │   ├── database.py        # Async SQLAlchemy
│   │   ├── main.py            # FastAPI entry point
│   │   ├── models/            # SQLAlchemy models
│   │   ├── schemas/           # Pydantic schemas
│   │   ├── routers/           # API route handlers
│   │   ├── services/          # Business logic
│   │   ├── integrations/      # External API clients
│   │   ├── middleware/        # Security middleware
│   │   └── utils/             # Validators, security, helpers
│   ├── alembic/               # Database migrations
│   ├── requirements.txt
│   └── Dockerfile
├── frontend/
│   ├── src/
│   │   ├── app/
│   │   │   ├── page.tsx       # Landing page
│   │   │   ├── auth/          # Login, Register
│   │   │   ├── dashboard/     # All dashboard pages
│   │   │   └── globals.css    # Design system (7 themes)
│   │   └── lib/
│   │       └── api.ts         # API client
│   ├── package.json
│   └── Dockerfile
├── docker-compose.yml
├── .env.example
└── README.md
```

---

## 🔑 API Keys Required

| Service | Purpose | Where to get |
|---------|---------|-------------|
| **GEMINI_API_KEY** | Astra AI assistant | [Google AI Studio](https://aistudio.google.com/) |
| **GOOGLE_MAPS_API_KEY** | Live navigation | [Google Cloud Console](https://console.cloud.google.com/) |
| **GOOGLE_OAUTH_CLIENT_ID** | Google Sign-In | [Google Cloud Console](https://console.cloud.google.com/) |
| **SMTP_HOST/USERNAME** | Email OTP | Your email provider |
| **MSG91_API_KEY** | SMS OTP | [MSG91](https://msg91.com/) |
| **DIGILOCKER_CLIENT_ID** | Document sync | [DigiLocker Partners](https://partners.digitallocker.gov.in/) |

> **Note:** The app works without any API keys — features gracefully degrade with informative empty states instead of fake data.

---

## 🎨 Theme System

DriveVerse includes **7 premium themes** that can be switched instantly:

1. **Neo Black** — Deep dark with indigo accents (default)
2. **Light** — Clean and bright
3. **Dark** — Classic dark mode
4. **Midnight Blue** — Deep ocean blue
5. **Aurora** — Northern lights inspired
6. **Cyber Glass** — Futuristic neon
7. **Titanium** — Minimal metallic

---

## 🔒 Security

- **bcrypt** password hashing (12 rounds)
- **JWT** with access + refresh token rotation
- **AES Fernet** encryption for sensitive data (engine numbers, etc.)
- **CSRF** protection
- **Rate limiting** ready
- **Audit logging** for compliance
- Input validation with Pydantic
- CORS configured per environment

---

## 📄 License

This project is proprietary. All rights reserved.

---

**Built with ❤️ for Indian vehicle owners.**
"# DriveLegal" 
