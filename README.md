# AgriLink

### Fresh produce. Fairer trade. Direct connections.

AgriLink is a full-stack Flutter marketplace that connects Ethiopian farmers directly with buyers. Farmers can showcase their products, buyers can discover and order local produce, and administrators can manage the marketplace from a dedicated web dashboard.

<p>
  <a href="https://github.com/Kenenisatamenaabdisa/AgriLink1"><img src="https://img.shields.io/badge/status-in%20development-1b6b3a?style=flat-square" alt="Project status"></a>
  <a href="https://flutter.dev"><img src="https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter&logoColor=white" alt="Flutter"></a>
  <a href="https://supabase.com"><img src="https://img.shields.io/badge/backend-Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white" alt="Supabase"></a>
  <img src="https://img.shields.io/badge/license-private-lightgrey?style=flat-square" alt="License">
</p>

## Why AgriLink?

Smallholder farmers deserve better access to customers and clearer pricing. AgriLink provides a digital route from farm to buyer that keeps the experience practical, local, and transparent.

**For buyers**
- Browse products and farmer profiles in one marketplace
- Add produce to a cart and place orders in ETB
- Track orders, review purchases, and message farmers
- Use the app in English, Amharic, or Afaan Oromo

**For farmers**
- Create a public farmer profile and manage products
- Set availability, pricing, categories, and images
- Receive orders and communicate with buyers
- View earnings and manage a direct customer relationship

**For administrators**
- Monitor farmers, products, orders, and support activity
- Manage marketplace data from a responsive Flutter web portal
- Export order data for reporting and operations

## Product Highlights

| Marketplace | Operations | Platform |
| --- | --- | --- |
| Product discovery and search | Order lifecycle and tracking | Flutter mobile app |
| Farmer profiles and reviews | Cart and checkout | Flutter web admin portal |
| Bulk ordering for businesses | Notifications and messaging | Supabase authentication and database |
| Localized buyer experience | Invoice generation | ETB payments with Chapa integration |

## Repository Structure

```text
.
├── AgriLink-main/
│   ├── agridirect_app/       # Main Flutter application for buyers and farmers
│   ├── admin_panel/           # Flutter web administration portal
│   ├── products_migration.sql # Product table migration
│   └── README.md              # App-specific notes
└── README.md                  # Project overview and setup
```

## Technology

- **Client:** Flutter and Dart
- **State and navigation:** Provider
- **Backend:** Supabase Auth, PostgreSQL, Storage, and Realtime
- **Payments:** Chapa with ETB support and a local test mode
- **Notifications:** Firebase Cloud Messaging and local notifications
- **Documents:** PDF invoice generation and printing
- **Supported platforms:** Android, iOS, Web, Windows, macOS, and Linux targets are included in the main app

## Getting Started

### Prerequisites

- Flutter SDK with Dart 3.11 or newer
- A Supabase project
- A Chapa account for live payment testing
- Firebase configuration for push notifications

### 1. Clone the repository

```bash
git clone https://github.com/Kenenisatamenaabdisa/AgriLink1.git
cd AgriLink1/AgriLink-main
```

### 2. Configure the backend

1. Create a Supabase project.
2. Run `agridirect_app/lib/setup/supabase_schema.sql` in the Supabase SQL editor.
3. Apply `products_migration.sql` if your existing database needs the product fields migration.
4. Add the required Supabase, Chapa, and Firebase values to the app's local environment configuration.

Never commit service-account files, secret API keys, or production credentials. Use local configuration and rotate any credential that has been exposed.

### 3. Run the mobile application

```bash
cd agridirect_app
flutter pub get
flutter run
```

### 4. Run the admin portal

```bash
cd ../admin_panel
flutter pub get
flutter run -d chrome
```

For payment development, the app supports a test mode so checkout flows can be exercised without processing a live transaction.

## Development Checks

Run these commands from either Flutter package directory:

```bash
flutter analyze
flutter test
```

## Project Direction

AgriLink is being developed as a practical foundation for a local digital food marketplace. Near-term priorities include strengthening production configuration, improving delivery workflows, and expanding operational reporting for farmers and administrators.

## Contributing

Issues and focused pull requests are welcome. Before opening a change, run the analyzer and relevant tests, describe the user impact, and avoid committing credentials or generated build artifacts.

## License

This project is currently maintained as a private portfolio and development project. Contact the repository owner for reuse or licensing questions.

<p align="center">
  Built to make local food commerce more direct, visible, and fair.
</p>
