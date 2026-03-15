# 🌏 GuideU API — Backend for Smart Tourism in Nepal

> **GuideU** is an all-in-one tourism platform focused on Nepal.

---

## Overview

**GuideU** aims to connect travelers with essential services in one ecosystem:
- Live guide booking (location-based, similar to ride-sharing flow)
- Hotel booking
- Vehicle booking
- Flight booking
- Accommodation booking
- Travel package booking

<div align="center">

  ![Alt text](/public/images/GuideU-logo.png)

  <br/>

  ![License](https://img.shields.io/badge/license-MIT-blue.svg)
  <!-- ![NodeJS](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white) -->
  ![ExpressJS](https://img.shields.io/badge/Express-000000?style=flat&logo=express&logoColor=white)
  ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)

  **AI-enabled tourism services platform for Nepal built with Flutter + Backend APIs**
</div>

---

## 🎓 Project Context

The architecture and technology choices are intentionally flexible at this stage as research is still in progress.

Current direction includes:
- **Flutter** for the mobile app
- **Node.js + Express** for backend APIs
- **MongoDB** (or another database if research indicates better fit)

---

## 🚀 Vision

Build a reliable, scalable tourism super-app backend for Nepal that can:
- Digitize fragmented tourism services
- Improve safety and convenience for domestic and international travelers
- Empower local guides, hotels, and operators through technology
- Support future AI-driven recommendations and fraud/risk insights

---

## ✨ Core Platform Modules

### 1) User & Identity
- User registration, login, and profile management
- Role-based access (traveler, guide, vendor, admin)
- JWT-based authentication and authorization

### 2) Live Guide Booking
- Discover nearby guides using geo-location
- Real-time guide availability
- Booking lifecycle: request → accept → ongoing → completed
- Ratings and reviews

### 3) Booking Services
- Hotel booking APIs
- Vehicle booking APIs
- Flight booking integration layer
- Accommodation and travel package booking

### 4) Payments & Transactions (Planned)
- Booking payments
- Commission and settlement model for providers
- Transaction history and invoice endpoints

### 5) Admin & Operations
- Service/provider management
- Booking oversight
- Flagging and moderation tools
- Reports and analytics endpoints

---

## 🧱 Proposed System Architecture

- **Client:** Flutter mobile app
- **API Layer:** RESTful services (Express.js)
- **Data Layer:** MongoDB (initial candidate)
- **Realtime Layer:** WebSocket/Socket.IO for live tracking and status updates
- **External Integrations:** Flight APIs, map/location services, payment gateways
- **Future Extensions:** AI service for recommendation, dynamic pricing insights, and anomaly detection

---

## 🛠 Tech Stack (Tentative)

Because the research phase is ongoing, this stack may evolve.

- **Runtime:** Node.js
- **Framework:** Express.js
- **Language:** TypeScript
- **Database:** MongoDB + Mongoose (current preference)
- **Auth:** JWT + bcrypt
- **Validation:** Zod / Joi
- **Testing:** Jest + Supertest
- **Mobile App:** Flutter (separate repository)

---

## 📁 Backend Structure

```text
guideu_api/
├─ src/
│  ├─ app.ts
│  ├─ server.ts
│  ├─ config/
│  ├─ controllers/
│  ├─ dtos/
│  ├─ errors/
│  ├─ helpers/
│  ├─ interfaces/
│  ├─ middlewares/
│  ├─ models/
│  ├─ repositories/
│  ├─ routes/
│  ├─ schemas/
│  ├─ services/
│  ├─ types/
│  ├─ utils/
│  └─ __tests__/
├─ package.json
├─ tsconfig.json
└─ README.md
```

---

## 🔐 Environment Variables (Example)

Create a `.env` file:

```env
PORT=5000
MONGODB_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/guideu
JWT_SECRET=replace_with_secure_secret
JWT_EXPIRES_IN=7d
NODE_ENV=development
```

> Do not commit secrets to GitHub.

---

## ⚙️ Local Setup

```bash
# 1) Clone repository
git clone https://github.com/<your-username>/guideu_api.git
cd guideu_api

# 2) Install dependencies
npm install

# 3) Add environment variables
cp .env.example .env

# 4) Run in development
npm run dev
```

---

## ▶️ Scripts

- `npm run dev` — Run backend in development mode
- `npm run build` — Compile TypeScript
- `npm start` — Start production build
- `npm test` — Run tests
- `npm run lint` — Run lint checks

---

## 🧪 Research-First Roadmap

### Phase 1 — Literature Review & Problem Definition
- Tourism pain points in Nepal
- Digital adoption barriers
- Existing tourism platforms and gap analysis

### Phase 2 — System Design
- Finalize architecture and data model
- Finalize module boundaries and APIs
- Security and privacy strategy

### Phase 3 - MVP Implementation
- Auth + user profiles
- Live guide booking module
- Core booking services (hotel/vehicle/package)

### Phase 4 — Evaluation and Output
- Performance and usability testing
- Result analysis
- Final report, demo, and presentation

### Phase 5 — Future Extensions (Post-Thesis)
- AI-based destination/package recommendations
- Fraud/risk scoring for bookings and transactions
- Dynamic pricing and demand forecasting

---

## 📌 Initial API Scope (Draft)

- `POST /api/auth/register`
- `POST /api/auth/login`
- `GET /api/users/me`
- `GET /api/guides/nearby`
- `POST /api/guides/bookings`
- `GET /api/bookings/:id`
- `POST /api/hotels/search`
- `POST /api/vehicles/search`
- `POST /api/packages/search`

> Endpoints will be refined after requirement analysis.

---

## 👨‍🎓 Author

**Subham Adhikari**  
Project: **GuideU — Smart Tourism Platform for Nepal**