<div align="center">

<img src="https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white" />
<img src="https://img.shields.io/badge/React_Native-Expo-000020?style=for-the-badge&logo=expo&logoColor=white" />
<img src="https://img.shields.io/badge/Backend-Node.js%20%2F%20Express-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" />
<img src="https://img.shields.io/badge/Database-MongoDB_Atlas-47A248?style=for-the-badge&logo=mongodb&logoColor=white" />
<img src="https://img.shields.io/badge/Status-Closed_Beta-FFD700?style=for-the-badge" />

<br/>
<br/>

# 🚗 UniRide

**Campus-native, peer-to-peer ride sharing — zero fees, zero friction.**

UniRide connects university students for shared commutes. No payments, no commercial overhead, no middlemen. Just students going the same direction.

<br/>

[![Get it on Google Play](https://img.shields.io/badge/Google_Play-Closed_Beta-414141?style=for-the-badge&logo=google-play&logoColor=white)](https://play.google.com/apps/testing/com.alper.uniride)

</div>

---

## 📸 Screenshots


Replace the block below with actual screenshots once available.
Recommended format: 3–5 images side by side using HTML img tags.

<div align="center">
  <img src="mobile/src/assets/screenshots/01-home.jpeg" width="200" />
  <img src="mobile/src/assets/screenshots/02-post.jpeg" width="200" />
  <img src="mobile/src/assets/screenshots/03-profile.jpeg" width="200" />
</div>

---

## ✨ Features

- **Free to use, always** — No credits, no wallets, no payment rails. UniRide is a pure carpooling protocol.
- **OTP Authentication** — Stateless, secure login flow tailored for campus environments.
- **Real-time Ride Matching** — Geospatial matching engine pairs drivers and passengers heading the same way.
- **Campus-first UX** — Designed specifically for student schedules and university geolocations.
- **Cross-platform** — React Native / Expo ensures consistent experience across Android devices.

---

## 🏗️ Architecture

UniRide follows strict **Modular Decoupling** — frontend, backend, and persistence layers are independently deployable.

```mermaid
graph TD
    Client[React Native Handset] -->|HTTPS REST| Gateway[Express API Gateway]
    Gateway --> Auth[OTP & Stateless Auth]
    Gateway --> Matching[Ride Matching Logic]
    Auth --> DB[(MongoDB Atlas)]
    Matching --> DB
```

| Layer | Stack |
|---|---|
| Mobile Client | React Native + Expo |
| API Gateway | Node.js + Express.js |
| ORM / Migrations | Prisma |
| Database | MongoDB Atlas |
| Auth | OTP-based Stateless JWT |

---

## 🚀 Local Development

### Prerequisites

| Dependency | Version |
|---|---|
| Node.js | v18.x or higher |
| Expo CLI | Latest |
| MongoDB Atlas | Active cluster with IP whitelist |

### Setup

```bash
# Clone the repository
git clone https://github.com/Jessitoii/uniride.git
cd uniride

# Install root dependencies
npm install
```

#### Frontend

```bash
cd frontend
npm install
npx expo start
```

#### Backend

```bash
cd backend
npm install

# Configure environment
cp .env.example .env
# Fill in MONGODB_URI, JWT_SECRET, etc.

npm run dev
```

---

## 📁 Project Structure

```
uniride/
├── frontend/          # React Native / Expo app
│   └── README.md      # Client-side engineering docs
├── backend/           # Node.js / Express API
│   └── README.md      # Server & persistence docs
└── README.md          # ← You are here
```

📄 **Module Documentation:**
- [Client-Side Engineering →](frontend/README.md)
- [Server-Side & Persistence →](backend/README.md)

---

## 🧪 Beta Access

UniRide is currently in **closed beta** on Google Play.

[![Join the Beta](https://img.shields.io/badge/Join_Closed_Beta-Google_Play-34A853?style=for-the-badge&logo=google-play&logoColor=white)](https://play.google.com/apps/testing/com.alper.uniride)

If you're a student interested in testing, reach out or request access via the link above.

---

## 📄 License

This project is private and not open-source at this time.

---

<div align="center">
  <sub>Built for students, by students.</sub>
</div>