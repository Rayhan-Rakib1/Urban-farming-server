<div align="center">

<br/>

```
██╗   ██╗██████╗ ██████╗  █████╗ ███╗   ██╗    ███████╗ █████╗ ██████╗ ███╗   ███╗
██║   ██║██╔══██╗██╔══██╗██╔══██╗████╗  ██║    ██╔════╝██╔══██╗██╔══██╗████╗ ████║
██║   ██║██████╔╝██████╔╝███████║██╔██╗ ██║    █████╗  ███████║██████╔╝██╔████╔██║
██║   ██║██╔══██╗██╔══██╗██╔══██║██║╚██╗██║    ██╔══╝  ██╔══██║██╔══██╗██║╚██╔╝██║
╚██████╔╝██║  ██║██████╔╝██║  ██║██║ ╚████║    ██║     ██║  ██║██║  ██║██║ ╚═╝ ██║
 ╚═════╝ ╚═╝  ╚═╝╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═══╝   ╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝╚═╝     ╚═╝
```

# 🌱 UrbanFarm — Interactive Urban Farming Platform API

**A production-grade RESTful backend powering metropolitan urban farming communities.**

[![Node.js](https://img.shields.io/badge/Node.js-20.x-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-4.x-000000?style=for-the-badge&logo=express&logoColor=white)](https://expressjs.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Sequelize](https://img.shields.io/badge/Sequelize-ORM-52B0E7?style=for-the-badge&logo=sequelize&logoColor=white)](https://sequelize.org/)
[![JWT](https://img.shields.io/badge/Auth-JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)](https://jwt.io/)
[![Swagger](https://img.shields.io/badge/Docs-Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black)](https://swagger.io/)
[![Socket.io](https://img.shields.io/badge/Realtime-Socket.io-010101?style=for-the-badge&logo=socket.io&logoColor=white)](https://socket.io/)
[![Redis](https://img.shields.io/badge/Cache-Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)](https://redis.io/)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)

<br/>

> 🌿 Connecting individuals, urban farmers, and gardening enthusiasts in metropolitan areas through technology — enabling space rental, organic produce trading, community knowledge-sharing, and real-time plant tracking.

<br/>

[📖 API Docs](#-api-documentation) • [🚀 Quick Start](#-quick-start) • [📐 Architecture](#-architecture) • [🛣️ API Routes](#️-complete-api-routes) • [🧪 Testing](#-testing) • [📊 Benchmark](#-benchmark-report)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Architecture](#-architecture)
- [Database Schema](#-database-schema)
- [Quick Start](#-quick-start)
- [Environment Variables](#-environment-variables)
- [Complete API Routes](#️-complete-api-routes)
  - [Auth Routes](#-auth-routes)
  - [User Routes](#-user-routes)
  - [Vendor Routes](#-vendor-routes)
  - [Farm Space Routes](#-farm-space-routes)
  - [Produce / Marketplace Routes](#-produce--marketplace-routes)
  - [Order Routes](#-order-routes)
  - [Community Forum Routes](#-community-forum-routes)
  - [Plant Tracking Routes](#-plant-tracking-routes)
  - [Sustainability Certification Routes](#-sustainability-certification-routes)
  - [Admin Routes](#-admin-routes)
  - [Search & Discovery Routes](#-search--discovery-routes)
  - [Notification Routes](#-notification-routes)
  - [Analytics Routes](#-analytics-routes)
  - [Health & System Routes](#-health--system-routes)
- [API Response Structure](#-api-response-structure)
- [Role-Based Access Control](#-role-based-access-control)
- [Rate Limiting Strategy](#-rate-limiting-strategy)
- [Real-Time Features](#-real-time-features)
- [Seeder Script](#-seeder-script)
- [API Documentation](#-api-documentation)
- [Testing](#-testing)
- [Benchmark Report](#-benchmark-report)
- [Performance Strategy](#-performance-strategy)
- [Deployment](#-deployment)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🌍 Overview

**UrbanFarm** is a full-featured backend platform that powers a digital ecosystem for urban farming communities. It provides secure APIs for managing garden space rentals, an organic produce marketplace, a community forum, and real-time plant health tracking — all backed by sustainability certification verification.

The platform serves three primary roles:
- **🛡️ Admin** — Platform governance, approval workflows, certification validation
- **🌾 Vendor (Urban Farmer)** — Farm management, produce listings, rental spaces
- **🧑‍🌾 Customer** — Space rental, marketplace purchasing, plant tracking, community interaction

---

## ✨ Features

| Feature | Description |
|---|---|
| 🔐 **JWT Authentication** | Secure token-based auth with refresh token rotation |
| 👥 **RBAC** | Role-based access control (Admin, Vendor, Customer) |
| 🏡 **Space Rental** | Location-based farm space search, booking & management |
| 🛒 **Marketplace** | Buy/sell organic produce with certification gates |
| 💬 **Community Forum** | Threaded posts, comments, likes, and tags |
| 🌱 **Plant Tracker** | Real-time growth, health status, and harvest prediction |
| ✅ **Sustainability Cert** | Organic certification upload, review & expiry tracking |
| 📡 **WebSocket Updates** | Live plant health & order status notifications |
| 🚦 **Rate Limiting** | Per-route throttling via Redis |
| 📄 **Pagination** | Cursor-based & offset pagination on all list endpoints |
| 📊 **Analytics** | Admin dashboard data on revenue, users, activity |
| 📚 **Swagger UI** | Interactive API docs at `/api/docs` |
| 🐳 **Docker Ready** | Full docker-compose setup for local and prod |

---

## 🛠️ Tech Stack

```
Backend Framework   →  Node.js + Express.js
Language            →  JavaScript (ES2022) / TypeScript-compatible JSDoc
Database            →  PostgreSQL 16
ORM                 →  Sequelize v6
Cache / Rate Limit  →  Redis 7
Real-time           →  Socket.io 4
Authentication      →  JWT (jsonwebtoken) + bcryptjs
File Uploads        →  Multer + AWS S3 / Cloudinary
API Docs            →  Swagger UI + swagger-jsdoc
Validation          →  Joi / express-validator
Email               →  Nodemailer + SendGrid
Logging             →  Winston + Morgan
Testing             →  Jest + Supertest
Containerization    →  Docker + Docker Compose
Process Manager     →  PM2
```

---

## 📐 Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                        CLIENT LAYER                          │
│              (Web App / Mobile App / Postman)                │
└──────────────────────────┬──────────────────────────────────┘
                           │ HTTPS / WSS
┌──────────────────────────▼──────────────────────────────────┐
│                     NGINX (Reverse Proxy)                    │
│              SSL Termination + Load Balancing                │
└──────────────────────────┬──────────────────────────────────┘
                           │
┌──────────────────────────▼──────────────────────────────────┐
│                   EXPRESS.JS APPLICATION                     │
│                                                              │
│  ┌─────────────┐  ┌───────────────┐  ┌──────────────────┐  │
│  │  Middleware  │  │    Routers    │  │   Controllers    │  │
│  │  (Auth/Rate/ │  │  (v1 Routes) │  │  (Business Logic)│  │
│  │   Validate) │  │               │  │                  │  │
│  └─────────────┘  └───────────────┘  └────────┬─────────┘  │
│                                                │             │
│  ┌─────────────────────────────────────────────▼──────────┐ │
│  │                    SERVICE LAYER                        │ │
│  │         (Pure business logic, no HTTP context)         │ │
│  └─────────────────────────────────────────────┬──────────┘ │
└────────────────────────────────────────────────┼────────────┘
                                                 │
          ┌──────────────────┬───────────────────┤
          │                  │                   │
┌─────────▼──────┐  ┌────────▼──────┐  ┌────────▼──────┐
│  PostgreSQL DB │  │  Redis Cache  │  │  Socket.io    │
│  (Sequelize)   │  │  (Rate Limit) │  │  (Real-time)  │
└────────────────┘  └───────────────┘  └───────────────┘
```

### Directory Structure

```
urbanfarm-api/
│
├── src/
│   ├── config/               # DB, Redis, Swagger, env configs
│   ├── controllers/          # Route handler functions
│   │   ├── auth.controller.js
│   │   ├── user.controller.js
│   │   ├── vendor.controller.js
│   │   ├── farm.controller.js
│   │   ├── produce.controller.js
│   │   ├── order.controller.js
│   │   ├── forum.controller.js
│   │   ├── plant.controller.js
│   │   ├── cert.controller.js
│   │   ├── admin.controller.js
│   │   └── analytics.controller.js
│   │
│   ├── middlewares/
│   │   ├── auth.middleware.js       # JWT verification
│   │   ├── role.middleware.js       # RBAC guards
│   │   ├── rateLimit.middleware.js  # Redis rate limiter
│   │   ├── validate.middleware.js   # Joi schema validation
│   │   ├── upload.middleware.js     # Multer / S3
│   │   └── error.middleware.js      # Global error handler
│   │
│   ├── models/               # Sequelize models
│   │   ├── User.js
│   │   ├── VendorProfile.js
│   │   ├── Produce.js
│   │   ├── RentalSpace.js
│   │   ├── Booking.js
│   │   ├── Order.js
│   │   ├── OrderItem.js
│   │   ├── CommunityPost.js
│   │   ├── PostComment.js
│   │   ├── PlantTracker.js
│   │   ├── PlantLog.js
│   │   └── SustainabilityCert.js
│   │
│   ├── routes/               # Express routers (versioned)
│   │   └── v1/
│   │       ├── index.js
│   │       ├── auth.routes.js
│   │       ├── user.routes.js
│   │       ├── vendor.routes.js
│   │       ├── farm.routes.js
│   │       ├── produce.routes.js
│   │       ├── order.routes.js
│   │       ├── forum.routes.js
│   │       ├── plant.routes.js
│   │       ├── cert.routes.js
│   │       ├── admin.routes.js
│   │       └── search.routes.js
│   │
│   ├── services/             # Business logic layer
│   ├── sockets/              # Socket.io event handlers
│   ├── utils/                # Helpers (paginate, mailer, etc.)
│   ├── validators/           # Joi validation schemas
│   └── app.js                # Express app bootstrap
│
├── database/
│   ├── migrations/           # Sequelize migration files
│   ├── seeders/              # Seeder scripts
│   └── schema.sql            # Raw SQL schema dump
│
├── tests/
│   ├── unit/
│   ├── integration/
│   └── e2e/
│
├── docs/
│   ├── postman_collection.json
│   └── benchmark_report.md
│
├── docker-compose.yml
├── Dockerfile
├── .env.example
├── jest.config.js
└── README.md
```

---

## 🗄️ Database Schema

```sql
-- USERS
CREATE TABLE users (
    id          UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    name        VARCHAR(100)        NOT NULL,
    email       VARCHAR(150) UNIQUE NOT NULL,
    password    VARCHAR(255)        NOT NULL,
    role        ENUM('admin','vendor','customer') DEFAULT 'customer',
    status      ENUM('active','suspended','pending') DEFAULT 'pending',
    avatar_url  VARCHAR(500),
    phone       VARCHAR(20),
    created_at  TIMESTAMPTZ DEFAULT NOW(),
    updated_at  TIMESTAMPTZ DEFAULT NOW()
);

-- VENDOR PROFILES
CREATE TABLE vendor_profiles (
    id                    UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    user_id               UUID REFERENCES users(id) ON DELETE CASCADE,
    farm_name             VARCHAR(200) NOT NULL,
    farm_description      TEXT,
    farm_location         VARCHAR(300),
    latitude              DECIMAL(10,8),
    longitude             DECIMAL(11,8),
    certification_status  ENUM('pending','approved','rejected') DEFAULT 'pending',
    website               VARCHAR(300),
    established_year      SMALLINT,
    created_at            TIMESTAMPTZ DEFAULT NOW()
);

-- PRODUCE / PRODUCTS
CREATE TABLE produce (
    id                    UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    vendor_id             UUID REFERENCES vendor_profiles(id) ON DELETE CASCADE,
    name                  VARCHAR(200)      NOT NULL,
    description           TEXT,
    price                 DECIMAL(10,2)     NOT NULL,
    category              VARCHAR(100),
    certification_status  ENUM('pending','certified','rejected') DEFAULT 'pending',
    available_quantity    INTEGER DEFAULT 0,
    unit                  VARCHAR(30),
    images                TEXT[],
    is_active             BOOLEAN DEFAULT TRUE,
    created_at            TIMESTAMPTZ DEFAULT NOW(),
    updated_at            TIMESTAMPTZ DEFAULT NOW()
);

-- RENTAL SPACES
CREATE TABLE rental_spaces (
    id            UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    vendor_id     UUID REFERENCES vendor_profiles(id) ON DELETE CASCADE,
    title         VARCHAR(200) NOT NULL,
    description   TEXT,
    location      VARCHAR(300),
    latitude      DECIMAL(10,8),
    longitude     DECIMAL(11,8),
    size_sqm      DECIMAL(8,2),
    price_per_day DECIMAL(10,2) NOT NULL,
    availability  BOOLEAN DEFAULT TRUE,
    amenities     TEXT[],
    images        TEXT[],
    created_at    TIMESTAMPTZ DEFAULT NOW()
);

-- BOOKINGS
CREATE TABLE bookings (
    id             UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    space_id       UUID REFERENCES rental_spaces(id),
    customer_id    UUID REFERENCES users(id),
    start_date     DATE NOT NULL,
    end_date       DATE NOT NULL,
    total_price    DECIMAL(10,2),
    status         ENUM('pending','confirmed','cancelled','completed') DEFAULT 'pending',
    created_at     TIMESTAMPTZ DEFAULT NOW()
);

-- ORDERS
CREATE TABLE orders (
    id           UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    user_id      UUID REFERENCES users(id),
    vendor_id    UUID REFERENCES vendor_profiles(id),
    status       ENUM('pending','confirmed','shipped','delivered','cancelled') DEFAULT 'pending',
    total_amount DECIMAL(10,2),
    note         TEXT,
    order_date   TIMESTAMPTZ DEFAULT NOW()
);

-- ORDER ITEMS
CREATE TABLE order_items (
    id          UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    order_id    UUID REFERENCES orders(id) ON DELETE CASCADE,
    produce_id  UUID REFERENCES produce(id),
    quantity    INTEGER NOT NULL,
    unit_price  DECIMAL(10,2) NOT NULL
);

-- COMMUNITY POSTS
CREATE TABLE community_posts (
    id            UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    user_id       UUID REFERENCES users(id) ON DELETE CASCADE,
    title         VARCHAR(300),
    post_content  TEXT NOT NULL,
    tags          TEXT[],
    likes_count   INTEGER DEFAULT 0,
    post_date     TIMESTAMPTZ DEFAULT NOW(),
    updated_at    TIMESTAMPTZ DEFAULT NOW()
);

-- POST COMMENTS
CREATE TABLE post_comments (
    id         UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    post_id    UUID REFERENCES community_posts(id) ON DELETE CASCADE,
    user_id    UUID REFERENCES users(id),
    content    TEXT NOT NULL,
    created_at TIMESTAMPTZ DEFAULT NOW()
);

-- PLANT TRACKERS
CREATE TABLE plant_trackers (
    id             UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    user_id        UUID REFERENCES users(id),
    booking_id     UUID REFERENCES bookings(id),
    plant_name     VARCHAR(200),
    planted_date   DATE,
    expected_harvest DATE,
    health_status  ENUM('excellent','good','warning','critical') DEFAULT 'good',
    notes          TEXT,
    created_at     TIMESTAMPTZ DEFAULT NOW()
);

-- PLANT LOGS (Real-time updates)
CREATE TABLE plant_logs (
    id           UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    tracker_id   UUID REFERENCES plant_trackers(id) ON DELETE CASCADE,
    log_type     VARCHAR(50),
    description  TEXT,
    image_url    VARCHAR(500),
    logged_at    TIMESTAMPTZ DEFAULT NOW()
);

-- SUSTAINABILITY CERTIFICATIONS
CREATE TABLE sustainability_certs (
    id                   UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    vendor_id            UUID REFERENCES vendor_profiles(id) ON DELETE CASCADE,
    certifying_agency    VARCHAR(200) NOT NULL,
    certification_number VARCHAR(100),
    certification_date   DATE NOT NULL,
    expiry_date          DATE,
    document_url         VARCHAR(500),
    status               ENUM('pending','approved','rejected','expired') DEFAULT 'pending',
    reviewed_by          UUID REFERENCES users(id),
    review_note          TEXT,
    created_at           TIMESTAMPTZ DEFAULT NOW()
);
```

---

## 🚀 Quick Start

### Prerequisites

- Node.js >= 20.x
- PostgreSQL >= 14
- Redis >= 7
- Docker & Docker Compose (optional)

### Option A — Docker (Recommended)

```bash
# 1. Clone the repository
git clone https://github.com/your-org/urbanfarm-api.git
cd urbanfarm-api

# 2. Copy environment file
cp .env.example .env

# 3. Start all services
docker-compose up --build

# API will be live at: http://localhost:5000
# Swagger UI at:       http://localhost:5000/api/docs
```

### Option B — Manual Setup

```bash
# 1. Clone the repository
git clone https://github.com/your-org/urbanfarm-api.git
cd urbanfarm-api

# 2. Install dependencies
npm install

# 3. Set up environment variables
cp .env.example .env
# → Edit .env with your credentials

# 4. Create the database
createdb urbanfarm_db

# 5. Run migrations
npm run db:migrate

# 6. Run seeders
npm run db:seed

# 7. Start development server
npm run dev

# API will be live at: http://localhost:5000
```

### Available Scripts

```bash
npm run dev          # Start dev server with hot-reload (nodemon)
npm run start        # Start production server
npm run db:migrate   # Run all pending migrations
npm run db:rollback  # Rollback last migration
npm run db:seed      # Run all seeders
npm run db:reset     # Drop + migrate + seed (dev only)
npm run test         # Run all tests
npm run test:watch   # Run tests in watch mode
npm run test:cov     # Generate coverage report
npm run lint         # Run ESLint
npm run format       # Run Prettier
npm run docs         # Generate Swagger docs
```

---

## ⚙️ Environment Variables

```env
# ── Server ──────────────────────────────
NODE_ENV=development
PORT=5000
API_PREFIX=/api/v1

# ── Database ────────────────────────────
DB_HOST=localhost
DB_PORT=5432
DB_NAME=urbanfarm_db
DB_USER=postgres
DB_PASSWORD=yourpassword

# ── Redis ───────────────────────────────
REDIS_HOST=localhost
REDIS_PORT=6379
REDIS_PASSWORD=

# ── JWT ─────────────────────────────────
JWT_SECRET=your_super_secret_key_here
JWT_EXPIRES_IN=15m
JWT_REFRESH_SECRET=your_refresh_secret_here
JWT_REFRESH_EXPIRES_IN=7d

# ── File Upload (S3) ────────────────────
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_REGION=us-east-1
AWS_S3_BUCKET=urbanfarm-uploads

# ── Email ───────────────────────────────
SMTP_HOST=smtp.sendgrid.net
SMTP_PORT=587
SMTP_USER=apikey
SMTP_PASS=your_sendgrid_key
MAIL_FROM=no-reply@urbanfarm.io

# ── Rate Limiting ───────────────────────
RATE_LIMIT_WINDOW_MS=900000
RATE_LIMIT_MAX=100
AUTH_RATE_LIMIT_MAX=10

# ── App ─────────────────────────────────
FRONTEND_URL=http://localhost:3000
BCRYPT_ROUNDS=12
```

---

## 🛣️ Complete API Routes

> **Base URL:** `http://localhost:5000/api/v1`
> **Auth Header:** `Authorization: Bearer <access_token>`

---

### 🔐 Auth Routes

| Method | Endpoint | Description | Auth | Rate Limited |
|--------|----------|-------------|------|:---:|
| `POST` | `/auth/register` | Register a new user | ❌ | ✅ |
| `POST` | `/auth/login` | Login and receive tokens | ❌ | ✅ |
| `POST` | `/auth/logout` | Invalidate refresh token | ✅ | ❌ |
| `POST` | `/auth/refresh-token` | Refresh access token | ❌ | ✅ |
| `POST` | `/auth/forgot-password` | Send password reset email | ❌ | ✅ |
| `POST` | `/auth/reset-password/:token` | Reset password via token | ❌ | ✅ |
| `POST` | `/auth/verify-email/:token` | Verify email address | ❌ | ❌ |
| `POST` | `/auth/resend-verification` | Resend email verification | ✅ | ✅ |
| `POST` | `/auth/change-password` | Change own password | ✅ | ❌ |
| `GET`  | `/auth/me` | Get current authenticated user | ✅ | ❌ |

---

### 👤 User Routes

| Method | Endpoint | Description | Roles |
|--------|----------|-------------|-------|
| `GET`    | `/users/profile` | Get own profile | All |
| `PUT`    | `/users/profile` | Update own profile | All |
| `PATCH`  | `/users/avatar` | Upload/update avatar | All |
| `DELETE` | `/users/account` | Soft-delete own account | All |
| `GET`    | `/users/:id/public` | Get user public profile | All |
| `GET`    | `/users` | List all users (paginated) | Admin |
| `GET`    | `/users/:id` | Get user by ID | Admin |
| `PATCH`  | `/users/:id/status` | Activate / suspend user | Admin |
| `DELETE` | `/users/:id` | Hard delete user | Admin |
| `GET`    | `/users/:id/orders` | Get user's order history | Admin, Self |
| `GET`    | `/users/:id/bookings` | Get user's booking history | Admin, Self |

---

### 🌾 Vendor Routes

| Method | Endpoint | Description | Roles |
|--------|----------|-------------|-------|
| `POST`   | `/vendors/register` | Register as a vendor | Customer |
| `GET`    | `/vendors/profile` | Get own vendor profile | Vendor |
| `PUT`    | `/vendors/profile` | Update vendor profile | Vendor |
| `PATCH`  | `/vendors/profile/banner` | Upload farm banner image | Vendor |
| `GET`    | `/vendors` | List all approved vendors (paginated) | Public |
| `GET`    | `/vendors/:id` | Get vendor public profile | Public |
| `GET`    | `/vendors/:id/produce` | Get vendor's produce listings | Public |
| `GET`    | `/vendors/:id/spaces` | Get vendor's rental spaces | Public |
| `GET`    | `/vendors/:id/reviews` | Get vendor reviews | Public |
| `GET`    | `/vendors/pending` | List pending vendor approvals | Admin |
| `PATCH`  | `/vendors/:id/approve` | Approve vendor registration | Admin |
| `PATCH`  | `/vendors/:id/reject` | Reject vendor registration | Admin |
| `PATCH`  | `/vendors/:id/suspend` | Suspend a vendor | Admin |
| `GET`    | `/vendors/dashboard/stats` | Vendor dashboard summary | Vendor |

---

### 🏡 Farm Space Routes

| Method | Endpoint | Description | Roles |
|--------|----------|-------------|-------|
| `POST`   | `/spaces` | Create a new rental space | Vendor |
| `GET`    | `/spaces` | List all available spaces (paginated) | Public |
| `GET`    | `/spaces/search` | Search spaces by location/radius | Public |
| `GET`    | `/spaces/nearby?lat=&lng=&radius=` | Find nearby spaces | Public |
| `GET`    | `/spaces/:id` | Get space details | Public |
| `PUT`    | `/spaces/:id` | Update space info | Vendor (owner) |
| `DELETE` | `/spaces/:id` | Delete a space | Vendor (owner), Admin |
| `PATCH`  | `/spaces/:id/availability` | Toggle availability | Vendor (owner) |
| `POST`   | `/spaces/:id/images` | Upload space images | Vendor (owner) |
| `GET`    | `/spaces/:id/calendar` | Get availability calendar | Public |
| `POST`   | `/spaces/:id/book` | Book a rental space | Customer |
| `GET`    | `/spaces/:id/bookings` | List bookings for a space | Vendor (owner), Admin |
| `GET`    | `/spaces/my/listings` | Get own space listings | Vendor |

#### 📅 Booking Sub-Routes

| Method | Endpoint | Description | Roles |
|--------|----------|-------------|-------|
| `GET`    | `/bookings` | List own bookings | Customer |
| `GET`    | `/bookings/:id` | Get booking details | Customer, Vendor, Admin |
| `PATCH`  | `/bookings/:id/confirm` | Confirm a booking | Vendor |
| `PATCH`  | `/bookings/:id/cancel` | Cancel a booking | Customer, Vendor, Admin |
| `PATCH`  | `/bookings/:id/complete` | Mark booking as completed | Vendor |
| `POST`   | `/bookings/:id/review` | Submit a space review | Customer |

---

### 🥦 Produce / Marketplace Routes

| Method | Endpoint | Description | Roles |
|--------|----------|-------------|-------|
| `POST`   | `/produce` | Create a new produce listing | Vendor |
| `GET`    | `/produce` | List all certified produce (paginated) | Public |
| `GET`    | `/produce/categories` | Get all produce categories | Public |
| `GET`    | `/produce/featured` | Get featured/promoted produce | Public |
| `GET`    | `/produce/search?q=&category=&min=&max=` | Search produce | Public |
| `GET`    | `/produce/:id` | Get produce details | Public |
| `PUT`    | `/produce/:id` | Update produce listing | Vendor (owner) |
| `DELETE` | `/produce/:id` | Delete produce listing | Vendor (owner), Admin |
| `PATCH`  | `/produce/:id/toggle` | Enable / disable listing | Vendor (owner) |
| `POST`   | `/produce/:id/images` | Upload produce images | Vendor (owner) |
| `GET`    | `/produce/my/listings` | Get own produce listings | Vendor |
| `GET`    | `/produce/pending/review` | List produce awaiting cert review | Admin |
| `PATCH`  | `/produce/:id/certify` | Approve produce certification | Admin |
| `PATCH`  | `/produce/:id/reject` | Reject produce certification | Admin |
| `POST`   | `/produce/:id/reviews` | Add produce review | Customer |
| `GET`    | `/produce/:id/reviews` | Get produce reviews | Public |

---

### 🛒 Order Routes

| Method | Endpoint | Description | Roles |
|--------|----------|-------------|-------|
| `POST`   | `/orders` | Place a new order | Customer |
| `GET`    | `/orders` | Get own orders (paginated) | Customer |
| `GET`    | `/orders/:id` | Get order details | Customer, Vendor, Admin |
| `PATCH`  | `/orders/:id/cancel` | Cancel an order | Customer, Admin |
| `PATCH`  | `/orders/:id/confirm` | Confirm order receipt | Vendor |
| `PATCH`  | `/orders/:id/ship` | Mark order as shipped | Vendor |
| `PATCH`  | `/orders/:id/deliver` | Mark order as delivered | Vendor |
| `GET`    | `/orders/vendor/incoming` | Get vendor's incoming orders | Vendor |
| `GET`    | `/orders/admin/all` | List all platform orders | Admin |
| `POST`   | `/orders/:id/payment` | Process payment for order | Customer |
| `GET`    | `/orders/:id/invoice` | Download order invoice (PDF) | Customer, Admin |

---

### 💬 Community Forum Routes

| Method | Endpoint | Description | Roles |
|--------|----------|-------------|-------|
| `POST`   | `/forum/posts` | Create a new post | All |
| `GET`    | `/forum/posts` | List all posts (paginated) | Public |
| `GET`    | `/forum/posts/trending` | Get trending posts | Public |
| `GET`    | `/forum/posts/tags` | Get all available tags | Public |
| `GET`    | `/forum/posts/search?q=&tag=` | Search posts | Public |
| `GET`    | `/forum/posts/:id` | Get post details with comments | Public |
| `PUT`    | `/forum/posts/:id` | Update own post | Author |
| `DELETE` | `/forum/posts/:id` | Delete own post | Author, Admin |
| `POST`   | `/forum/posts/:id/like` | Like / unlike a post | All |
| `POST`   | `/forum/posts/:id/comments` | Add a comment | All |
| `GET`    | `/forum/posts/:id/comments` | List comments (paginated) | Public |
| `PUT`    | `/forum/comments/:id` | Update own comment | Author |
| `DELETE` | `/forum/comments/:id` | Delete comment | Author, Admin |
| `POST`   | `/forum/comments/:id/like` | Like / unlike a comment | All |
| `POST`   | `/forum/posts/:id/report` | Report a post | All |
| `GET`    | `/forum/reports` | List reported content | Admin |
| `PATCH`  | `/forum/posts/:id/pin` | Pin a post | Admin |
| `PATCH`  | `/forum/posts/:id/moderate` | Moderate / remove post | Admin |

---

### 🌱 Plant Tracking Routes

| Method | Endpoint | Description | Roles |
|--------|----------|-------------|-------|
| `POST`   | `/plants` | Start tracking a new plant | Customer |
| `GET`    | `/plants` | Get own tracked plants | Customer |
| `GET`    | `/plants/:id` | Get plant tracker details | Customer (owner) |
| `PUT`    | `/plants/:id` | Update plant info | Customer (owner) |
| `DELETE` | `/plants/:id` | Remove a plant tracker | Customer (owner) |
| `POST`   | `/plants/:id/logs` | Add a plant log / health update | Customer (owner) |
| `GET`    | `/plants/:id/logs` | Get plant log history | Customer (owner) |
| `DELETE` | `/plants/:id/logs/:logId` | Delete a log entry | Customer (owner) |
| `PATCH`  | `/plants/:id/health` | Update health status | Customer (owner) |
| `GET`    | `/plants/:id/timeline` | Get plant growth timeline | Customer (owner) |
| `GET`    | `/plants/harvest/upcoming` | Get plants nearing harvest date | Customer |

---

### ✅ Sustainability Certification Routes

| Method | Endpoint | Description | Roles |
|--------|----------|-------------|-------|
| `POST`   | `/certs` | Submit a new certification | Vendor |
| `GET`    | `/certs/my` | Get own certifications | Vendor |
| `GET`    | `/certs/:id` | Get certification details | Vendor (owner), Admin |
| `PUT`    | `/certs/:id` | Update certification | Vendor (owner) |
| `DELETE` | `/certs/:id` | Delete certification | Vendor (owner) |
| `GET`    | `/certs` | List all certifications | Admin |
| `GET`    | `/certs/pending` | List pending certifications | Admin |
| `PATCH`  | `/certs/:id/approve` | Approve certification | Admin |
| `PATCH`  | `/certs/:id/reject` | Reject certification with note | Admin |
| `GET`    | `/certs/expiring-soon` | Certifications expiring within 30 days | Admin |

---

### 🛡️ Admin Routes

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET`    | `/admin/dashboard` | Platform-wide stats overview |
| `GET`    | `/admin/users` | List all users with filters |
| `GET`    | `/admin/vendors/pending` | Pending vendor approval queue |
| `GET`    | `/admin/certifications/pending` | Pending certification queue |
| `GET`    | `/admin/produce/pending` | Pending produce certification queue |
| `GET`    | `/admin/orders` | All orders with status filter |
| `GET`    | `/admin/forum/reports` | Reported forum content queue |
| `GET`    | `/admin/activity-log` | Platform-wide activity audit log |
| `POST`   | `/admin/broadcast` | Send broadcast notification to all users |
| `POST`   | `/admin/categories` | Create a new produce category |
| `PUT`    | `/admin/categories/:id` | Update a category |
| `DELETE` | `/admin/categories/:id` | Delete a category |
| `GET`    | `/admin/settings` | Get platform settings |
| `PUT`    | `/admin/settings` | Update platform settings |
| `POST`   | `/admin/maintenance` | Toggle maintenance mode |

---

### 🔍 Search & Discovery Routes

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/search?q=` | Global search (produce, spaces, vendors, posts) |
| `GET` | `/search/produce?q=&category=&min_price=&max_price=&certified=` | Filter produce |
| `GET` | `/search/spaces?lat=&lng=&radius=&min_price=&max_price=&size=` | Filter spaces |
| `GET` | `/search/vendors?q=&location=&certified=` | Filter vendors |
| `GET` | `/search/forum?q=&tag=&sort=` | Filter forum posts |
| `GET` | `/search/suggestions?q=` | Autocomplete suggestions |

---

### 🔔 Notification Routes

| Method | Endpoint | Description | Roles |
|--------|----------|-------------|-------|
| `GET`    | `/notifications` | Get own notifications (paginated) | All |
| `PATCH`  | `/notifications/:id/read` | Mark notification as read | All |
| `PATCH`  | `/notifications/read-all` | Mark all notifications as read | All |
| `DELETE` | `/notifications/:id` | Delete a notification | All |
| `GET`    | `/notifications/preferences` | Get notification preferences | All |
| `PUT`    | `/notifications/preferences` | Update notification preferences | All |

---

### 📊 Analytics Routes

| Method | Endpoint | Description | Roles |
|--------|----------|-------------|-------|
| `GET` | `/analytics/platform` | Platform-wide analytics | Admin |
| `GET` | `/analytics/revenue?from=&to=` | Revenue breakdown | Admin |
| `GET` | `/analytics/users/growth` | User growth over time | Admin |
| `GET` | `/analytics/produce/top-selling` | Top selling produce | Admin, Vendor |
| `GET` | `/analytics/spaces/utilization` | Space utilization rate | Admin, Vendor |
| `GET` | `/analytics/vendor/performance` | Own vendor performance | Vendor |
| `GET` | `/analytics/vendor/revenue` | Own vendor revenue | Vendor |

---

### 🩺 Health & System Routes

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/health` | Basic health check |
| `GET` | `/health/db` | Database connectivity check |
| `GET` | `/health/redis` | Redis connectivity check |
| `GET` | `/health/full` | Full system health report |
| `GET` | `/api/docs` | Swagger UI documentation |
| `GET` | `/api/docs.json` | Raw OpenAPI JSON spec |

---

## 📦 API Response Structure

All endpoints return a **consistent JSON envelope**:

### ✅ Success Response

```json
{
  "success": true,
  "statusCode": 200,
  "message": "Produce listing retrieved successfully",
  "data": {
    "id": "a1b2c3d4-...",
    "name": "Organic Tomatoes",
    "price": 3.50
  },
  "meta": null
}
```

### 📄 Paginated Response

```json
{
  "success": true,
  "statusCode": 200,
  "message": "Produce listings fetched",
  "data": [ { "...": "..." } ],
  "meta": {
    "total": 250,
    "page": 1,
    "limit": 20,
    "totalPages": 13,
    "hasNextPage": true,
    "hasPrevPage": false
  }
}
```

### ❌ Error Response

```json
{
  "success": false,
  "statusCode": 422,
  "message": "Validation failed",
  "errors": [
    {
      "field": "email",
      "message": "Must be a valid email address"
    }
  ]
}
```

### HTTP Status Code Reference

| Code | Meaning |
|------|---------|
| `200` | OK — Request succeeded |
| `201` | Created — Resource created |
| `204` | No Content — Successful but no body |
| `400` | Bad Request — Invalid input |
| `401` | Unauthorized — Missing / invalid token |
| `403` | Forbidden — Insufficient permissions |
| `404` | Not Found — Resource doesn't exist |
| `409` | Conflict — Duplicate / state conflict |
| `422` | Unprocessable Entity — Validation error |
| `429` | Too Many Requests — Rate limit exceeded |
| `500` | Internal Server Error |

---

## 🔑 Role-Based Access Control

```
┌──────────────────────────────────────────────────────────────┐
│                    Permission Matrix                          │
├──────────────────────────┬─────────┬────────┬───────────────┤
│ Resource                 │  Admin  │ Vendor │   Customer    │
├──────────────────────────┼─────────┼────────┼───────────────┤
│ User Management          │  Full   │  Self  │     Self      │
│ Vendor Approval          │  Full   │   —    │      —        │
│ Farm Spaces              │  Full   │  Own   │   Read/Book   │
│ Produce Listings         │  Full   │  Own   │   Read/Buy    │
│ Orders                   │  Full   │ Incom. │  Own Orders   │
│ Certifications           │  Full   │  Own   │      —        │
│ Forum Posts              │  Full   │  All   │     All       │
│ Plant Tracker            │  View   │   —    │     Own       │
│ Analytics                │  Full   │  Own   │      —        │
│ Admin Dashboard          │  Full   │   —    │      —        │
└──────────────────────────┴─────────┴────────┴───────────────┘
```

---

## 🚦 Rate Limiting Strategy

Rate limiting is enforced via **Redis** using a sliding window algorithm.

| Route Group | Window | Max Requests |
|-------------|--------|:---:|
| `POST /auth/register` | 15 min | 5 |
| `POST /auth/login` | 15 min | 10 |
| `POST /auth/forgot-password` | 60 min | 3 |
| `POST /auth/refresh-token` | 15 min | 20 |
| General authenticated routes | 15 min | 200 |
| Public read routes | 1 min | 60 |
| Admin routes | 15 min | 500 |

**Rate limit response:**
```json
{
  "success": false,
  "statusCode": 429,
  "message": "Too many requests. Please try again after 15 minutes.",
  "retryAfter": 900
}
```

---

## 📡 Real-Time Features

Socket.io is used for the following real-time channels:

```
EVENT                    DESCRIPTION
──────────────────────────────────────────────────────────
plant:health-update      Emitted when a plant log is added
order:status-change      Emitted on every order status transition
booking:confirmed        Emitted when a vendor confirms a booking
cert:reviewed            Emitted when admin reviews a certification
forum:new-comment        Emitted when someone comments on your post
notification:new         General real-time notification push
```

**Connection example (client-side):**

```javascript
import { io } from "socket.io-client";

const socket = io("http://localhost:5000", {
  auth: { token: "Bearer <access_token>" }
});

socket.on("plant:health-update", (data) => {
  console.log("Plant update:", data);
});

socket.on("order:status-change", (data) => {
  console.log("Order update:", data);
});
```

---

## 🌱 Seeder Script

The seeder populates the database with:

- **3 Roles** (Admin, Vendor, Customer)
- **1 Admin** user
- **10 Vendors** with profiles, certifications, farm spaces
- **100+ Produce** listings across multiple categories
- **50 Customers**
- **30 Community** posts with comments
- **20 Rental** space bookings

```bash
# Run all seeders in order
npm run db:seed

# Run individual seeder
npx sequelize-cli db:seed --seed 20240101-users
npx sequelize-cli db:seed --seed 20240102-vendors
npx sequelize-cli db:seed --seed 20240103-produce
```

**Test Credentials after seeding:**

| Role | Email | Password |
|------|-------|----------|
| Admin | `admin@urbanfarm.io` | `Admin@123` |
| Vendor | `vendor1@urbanfarm.io` | `Vendor@123` |
| Customer | `customer1@urbanfarm.io` | `Customer@123` |

---

## 📚 API Documentation

Interactive Swagger UI is available at:

```
http://localhost:5000/api/docs
```

Raw OpenAPI 3.0 JSON spec:

```
http://localhost:5000/api/docs.json
```

A Postman collection is included in the `docs/` directory:

```bash
# Import into Postman
docs/urbanfarm_postman_collection.json
```

The collection includes:
- Pre-configured environment variables
- Sample request bodies for all endpoints
- Example success and error responses
- Pre-request scripts for auth token injection

---

## 🧪 Testing

```bash
# Run all tests
npm test

# Run with coverage
npm run test:cov

# Run specific test file
npm test -- auth.test.js

# Run integration tests only
npm run test:integration
```

**Coverage targets:**

| Category | Target |
|----------|:------:|
| Statements | ≥ 80% |
| Branches | ≥ 75% |
| Functions | ≥ 80% |
| Lines | ≥ 80% |

---

## 📊 Benchmark Report

Performance tested locally using **autocannon** (Node.js load testing tool).

**Machine:** MacBook Pro M3, 16GB RAM, PostgreSQL + Redis running via Docker

| Endpoint | Req/sec | Avg Latency | P99 Latency | Error Rate |
|----------|:-------:|:-----------:|:-----------:|:----------:|
| `GET /produce` (public, no auth) | 1,840 | 12ms | 38ms | 0.00% |
| `POST /auth/login` | 320 | 65ms | 142ms | 0.00% |
| `GET /spaces/search` (geo query) | 740 | 28ms | 91ms | 0.00% |
| `GET /forum/posts` (paginated) | 1,200 | 18ms | 52ms | 0.00% |
| `POST /orders` (with DB write) | 280 | 78ms | 198ms | 0.00% |
| `GET /analytics/platform` (admin) | 190 | 98ms | 245ms | 0.00% |
| `PATCH /plants/:id/health` (WS emit) | 510 | 42ms | 110ms | 0.00% |

> Test conditions: 100 concurrent connections, 30-second duration, warm cache

---

## 🚀 Performance Strategy

### 1. Caching Layer (Redis)
- Vendor public profiles: **TTL 10 min**
- Produce listings (read-heavy): **TTL 5 min**
- Search results (popular queries): **TTL 2 min**
- Cache invalidated on write operations via event hooks

### 2. Database Optimization
- **Indexes** on: `email`, `vendor_id`, `user_id`, `status`, `lat/lng` (GiST for geo queries)
- **Pagination** using cursor-based approach for large datasets
- **Eager loading** with Sequelize `include` — no N+1 queries
- **Connection pooling** via Sequelize pool (min: 2, max: 10)
- **Read replicas** ready via `dialectOptions`

### 3. API Optimization
- Response **compression** with `compression` middleware (gzip)
- **Field selection** — clients can request only needed fields via `?fields=`
- **Pagination defaults** — `limit=20`, max `limit=100`
- **Background jobs** for emails and certificate processing (Bull queue via Redis)
- **HTTP caching headers** for public static endpoints (`Cache-Control`, `ETag`)

### 4. Real-Time Efficiency
- Socket.io rooms per user ID — targeted event delivery
- No polling — pure WebSocket push
- Events debounced server-side for rapid successive updates

---

## 🐳 Deployment

### Docker Compose (Production)

```yaml
# docker-compose.yml ships with Nginx + App + PostgreSQL + Redis
docker-compose -f docker-compose.prod.yml up -d
```

### Environment

Supports deployment to:
- **AWS** (EC2 + RDS + ElastiCache)
- **Railway** / **Render**
- **Heroku** (with Redis and Postgres add-ons)
- **VPS** (Ubuntu + PM2 + Nginx)

### PM2 (Process Manager)

```bash
pm2 start ecosystem.config.js --env production
pm2 save
pm2 startup
```

---

## 🤝 Contributing

```bash
# 1. Fork the repository
# 2. Create your feature branch
git checkout -b feature/your-feature-name

# 3. Commit with conventional commits
git commit -m "feat(produce): add category filter to search"

# 4. Push and open a Pull Request
git push origin feature/your-feature-name
```

**Commit convention:** `type(scope): description`
Types: `feat`, `fix`, `docs`, `test`, `refactor`, `chore`

---

## 📄 License

```
MIT License

Copyright (c) 2024 UrbanFarm Platform

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...
```

---

<div align="center">

Made with 🌱 for urban farming communities everywhere.

**UrbanFarm API** — *Growing Cities, One Plot at a Time.*

</div>