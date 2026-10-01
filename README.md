# 🌾 AgriLink — Ethiopia's Direct Farm-to-Table Marketplace

<p align="center">
  <strong>Connecting Ethiopian farmers directly with buyers</strong>
</p>

<p align="center">
  A modern marketplace for discovering local produce, building farmer-buyer relationships, and managing agricultural orders from one connected platform.
</p>

<p align="center">
  <a href="https://github.com/Kenenisatamenaabdisa/AgriLink1"><img src="https://img.shields.io/badge/status-in%20development-1B6B3A?style=for-the-badge" alt="Project status"></a>
  <a href="https://flutter.dev"><img src="https://img.shields.io/badge/Flutter-3.x-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter"></a>
  <a href="https://dart.dev"><img src="https://img.shields.io/badge/Dart-3.11%2B-0175C2?style=for-the-badge&logo=dart&logoColor=white" alt="Dart"></a>
  <a href="https://supabase.com"><img src="https://img.shields.io/badge/Supabase-Backend-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white" alt="Supabase"></a>
</p>

---

## 📋 Table of Contents

- [About the Project](#-about-the-project)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Admin Panel](#-admin-panel)
- [Database](#-database)
- [Development Checks](#-development-checks)
- [Contributing](#-contributing)
- [Author](#-author)

---

## 📖 About the Project

**AgriLink** is a full-stack Flutter marketplace designed to make agricultural trade more direct and accessible in Ethiopia.

Smallholder farmers can present their products to a wider audience, while buyers can find fresh local produce, communicate with farmers, place orders, and follow delivery progress. A dedicated web admin portal gives platform operators the tools to manage users, products, orders, and support activity.

### The platform connects three experiences

- **Farmers** can create profiles, list products, manage availability, receive orders, and track earnings.
- **Buyers** can browse products, compare farmer profiles, add items to a cart, check out, and review purchases.
- **Administrators** can oversee users, product listings, orders, support requests, and marketplace operations.

---

## 🚀 Key Features

### 🛒 Marketplace

- Product discovery with search, categories, pricing, and availability
- Farmer profiles with location, farm information, ratings, and reviews
- Rich product details with images, stock information, and purchasing actions
- Cart, checkout, order history, and invoice generation
- Bulk ordering support for business buyers

### 👨‍🌾 Farmer Tools

- Farmer registration and profile management
- Product creation and inventory management
- Farmer dashboard with order and earnings views
- Customer messaging and order communication
- Regional farmer information across Ethiopia

### 📦 Orders and Payments

- Order status tracking from pending through delivery
- Chapa payment integration with ETB support
- Cash on Delivery, mobile money, and bank transfer options
- Payment test mode for development checkout flows
- Order notifications and downloadable order data in the admin panel

### 💬 Communication

- Direct buyer-farmer messaging
- Supabase-backed real-time communication services
- Push notifications with Firebase Cloud Messaging
- Local notifications for important order and account events

### 🌍 Localization and Accessibility

- English interface
- Amharic interface (አማርኛ)
- Afaan Oromo interface
- Region-aware marketplace content
- Voice-enabled search support through speech-to-text services

### 📊 Admin Panel

- Dashboard for marketplace activity and key metrics
- User and farmer management
- Product review and moderation workflows
- Order oversight and operational support
- CSV order export for reporting

---

## 🛠 Tech Stack

| Layer | Technology |
| --- | --- |
| Mobile and web client | Flutter and Dart |
| State management | Provider |
| Backend and database | Supabase, PostgreSQL, Auth, Storage, and Realtime |
| Payments | Chapa with ETB support |
| Push notifications | Firebase Cloud Messaging |
| Local notifications | Flutter Local Notifications |
| Offline and local storage | Hive and Shared Preferences |
| Location services | Geolocator |
| Voice search | Speech-to-text |
| Image handling | Image Picker and Cached Network Image |
| Documents | PDF and Printing packages |
| Admin portal | Flutter Web |

---

## 📂 Project Structure

```text
AgriLink1/
├── README.md
└── AgriLink-main/
    ├── agridirect_app/          # Main Flutter app for buyers and farmers
    │   ├── lib/
    │   │   ├── models/          # User, farmer, product, order, and message models
    │   │   ├── providers/       # Application state and localization providers
    │   │   ├── screens/          # Marketplace, auth, orders, chat, and profile screens
    │   │   ├── services/         # Auth, products, orders, payments, and notifications
    │   │   ├── widgets/          # Reusable UI components
    │   │   └── setup/            # Supabase schema and migration scripts
    │   └── pubspec.yaml
    │
    ├── admin_panel/              # Flutter Web admin dashboard
    │   ├── lib/
    │   │   ├── models/           # Admin data models
    │   │   ├── screens/          # Dashboard, farmers, products, orders, and support
    │   │   └── services/         # Admin data services
    │   └── pubspec.yaml
    │
    └── products_migration.sql   # Product table migration
```

---

## 🏁 Getting Started

### Prerequisites

- [Flutter SDK](https://docs.flutter.dev/get-started/install) with Dart 3.11 or newer
- A [Supabase](https://supabase.com/) project
- A [Chapa](https://chapa.co/) account for live payment testing
- A Firebase project for push notifications

### 1. Clone the repository

```bash
git clone https://github.com/Kenenisatamenaabdisa/AgriLink1.git
cd AgriLink1/AgriLink-main
```

### 2. Install mobile app dependencies

```bash
cd agridirect_app
flutter pub get
```

### 3. Configure the backend

1. Create a Supabase project.
2. Run [`supabase_schema.sql`](AgriLink-main/agridirect_app/lib/setup/supabase_schema.sql) in the Supabase SQL Editor.
3. Apply [`migration.sql`](AgriLink-main/agridirect_app/lib/setup/migration.sql) when upgrading an existing database.
4. Apply [`products_migration.sql`](AgriLink-main/products_migration.sql) if the product table needs the additional product fields.
5. Configure the local Supabase, Chapa, Firebase, and notification values required by your environment.

> **Security:** Never commit service-account files, secret API keys, or production credentials. Use local configuration for development and rotate any credential that may have been exposed.

### 4. Run the application

```bash
flutter run
```

The main app includes Android, iOS, web, Windows, macOS, and Linux project targets.

---

## 🖥 Admin Panel

The admin panel is a separate Flutter Web application for marketplace operations.

```bash
cd ../admin_panel
flutter pub get
flutter run -d chrome
```

The portal includes views for the dashboard, farmers, products, orders, and support workflows. Admin authentication and data access are handled through the shared Supabase backend.

---

## 🗃 Database

AgriLink uses Supabase PostgreSQL for structured marketplace data, authentication, storage, and real-time services.

| Table | Purpose |
| --- | --- |
| `users` | Buyer, farmer, business, and admin accounts |
| `farmers` | Farmer profiles, regions, ratings, and verification data |
| `products` | Product listings, pricing, categories, stock, and images |
| `orders` | Buyer orders, farmer relationships, totals, and status |
| `order_items` | Products and quantities belonging to each order |
| `messages` | Direct buyer-farmer conversations |
| `reviews` | Product and farmer ratings and feedback |
| `notifications` | In-app account and order notifications |

The complete schema is available in [`supabase_schema.sql`](AgriLink-main/agridirect_app/lib/setup/supabase_schema.sql).

---

## ✅ Development Checks

Run these commands from either Flutter package directory:

```bash
flutter analyze
flutter test
```

For payment development, use the app's test mode before connecting a live Chapa account.

---

## 🤝 Contributing

Contributions and focused improvements are welcome.

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/your-feature`.
3. Make and test your changes.
4. Run `flutter analyze` and the relevant tests.
5. Commit your work and open a pull request with a clear description of the user impact.

Please do not commit generated build output, service-account files, or secret credentials.

---

## 👤 Author

**Kenenisa Abdisa**

- GitHub: [@Kenenisatamenaabdisa](https://github.com/Kenenisatamenaabdisa)
- Project: [AgriLink1](https://github.com/Kenenisatamenaabdisa/AgriLink1)

---

<p align="center">
  <em>🌱 Connecting Ethiopia's farms to the people they serve. 🌍</em>
</p>
