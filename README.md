45 results - 24 files

README.md:
  1: AgriLink — A direct farm-to-buyer marketplace connecting rural Ethiopian farmers with urban consumers, featuring real-time chat, order tracking, and a dedicated admin web portal. 
  2  

AgriLink-main\products_migration.sql:
  1  -- ============================================================
  2: -- AgriLink: Complete products table migration
  3  -- Run this in Supabase SQL Editor to add all missing columns

AgriLink-main\README.md:
    1: # 🌾 AgriLink — Ethiopia's Direct Farm-to-Table Marketplace
    2  

   34  
   35: **AgriLink** is a full-stack mobile application built to solve the disconnect between Ethiopian farmers and consumers. Smallholder farmers often lack access to markets, fair pricing, and reliable buyers. AgriLink eliminates middlemen by providing a direct, digital marketplace where:
   36  

   91  ```
   92: AgriLink/
   93  ├── agridirect_app/           # 📱 Main Flutter mobile application

  129     ```bash
  130:    git clone https://github.com/kenenisa-abdisa/AgriLink.git
  131:    cd AgriLink
  132     ```

  217  <p align="center">
  218:   <em>🌱 AgriLink — Connecting Ethiopia's Heartbeat to the World 🌍</em>
  219  </p>

AgriLink-main\admin_panel\pubspec.yaml:
  1  name: admin_panel
  2: description: "Admin web portal for AgriLink — Direct farmer-to-buyer agricultural marketplace."
  3  # The following line prevents the package from being accidentally published to

AgriLink-main\admin_panel\lib\main.dart:
   37        debugShowCheckedModeBanner: false,
   38:       title: 'AgriLink Admin Panel',
   39        theme: ThemeData(

  107                    const Text(
  108:                     'AgriLink Admin',
  109                      style: TextStyle(color: Colors.white, fontWeight: FontWeight.bold, fontSize: 18),

AgriLink-main\admin_panel\lib\screens\login_screen.dart:
  45                const Text(
  46:                 'AgriLink Admin',
  47                  style: TextStyle(fontSize: 24, fontWeight: FontWeight.bold),

AgriLink-main\admin_panel\lib\screens\orders_screen.dart:
  64      anchor.href = url;
  65:     anchor.download = 'agrilink_orders_${DateTime.now().millisecondsSinceEpoch}.csv';
  66      anchor.click();

AgriLink-main\agridirect_app\pubspec.yaml:
  1  name: agridirect_app
  2: description: "AgriLink Ethiopia - Direct farmer-to-buyer marketplace"
  3  publish_to: 'none'

AgriLink-main\agridirect_app\android\app\src\main\AndroidManifest.xml:
  8      <application
  9:         android:label="AgriLink"
  10          android:name="${applicationName}"

AgriLink-main\agridirect_app\lib\constants.dart:
   2    'en': {
   3:     'app_name': 'AgriLink Ethiopia',
   4      'tagline': 'Fresh · Local · Direct',

  35    'am': {
  36:     'app_name': 'AgriLink Ethiopia',
  37      'tagline': 'ትኩስ · አካባቢያዊ · ቀጥታ',

  68    'or': {
  69:     'app_name': 'AgriLink Ethiopia',
  70      'tagline': 'Dhibee · Naannoo · Kallattiin',

AgriLink-main\agridirect_app\lib\main.dart:
  68          ],
  69:         child: const AgriLinkApp(),
  70        ),

  77  
  78: class AgriLinkApp extends StatelessWidget {
  79:   const AgriLinkApp({super.key});
  80  

  84        debugShowCheckedModeBanner: false,
  85:       title: 'AgriLink',
  86        theme: ThemeData(

AgriLink-main\agridirect_app\lib\providers\localization_provider.dart:
  38        'Search products, farmers...': 'ምርቶችን፣ ገበሬዎችን ይፈልጉ...',
  39:       'AgriLink Ethiopia': 'አግሪሊንክ ኢትዮጵያ',
  40        'Fresh · Local · Direct': 'ትኩስ · አካባቢያዊ · ቀጥታ',

  46        'Phone': 'ስልክ',
  47:       'New to AgriLink? Sign Up': 'አዲስ ነዎት? ይመዝገቡ',
  48        'Already have an account? Sign In': 'ቀድሞውኑ መለያ አለዎት? ይግቡ',

  53            'የእኛ መድረክ ትኩስ ምርቶችን እና ተመጣጣኝ ዋጋን በማረጋገጥ በቀጥታ ከአካባቢው ገበሬዎች ጋር ያገናኝዎታል።',
  54:       'Welcome to AgriLink! 👋': 'እንኳን ወደ አግሪሊንክ በደህና መጡ! 👋',
  55        'Farmer Profile Created! 🌾': 'የገበሬ ፕሮፋይል ተፈጥሯል! 🌾',

  64        'Search products, farmers...': 'Oomishaa fi qotee bulaa barbaadi...',
  65:       'AgriLink Ethiopia': 'AgriLink Itoophiyaa',
  66        'Fresh · Local · Direct': 'Haaraa · Naannoo · Kallattiin',

  72        'Phone': 'Bilbila',
  73:       'New to AgriLink? Sign Up': 'Haaraadha? Galmaahi',
  74        'Already have an account? Sign In': 'Eenyummeessa qabdaa? Seeni',

  79            'Platformiin keenya kallattiin qotee bulaa naannoo waliin wal isin qunnamsiisa.',
  80:       'Welcome to AgriLink! 👋': 'Baga gara AgriLink nagaan dhuftan! 👋',
  81        'Farmer Profile Created! 🌾': 'Profaayilii qotee bulaa uumameera! 🌾',

AgriLink-main\agridirect_app\lib\screens\checkout_screen.dart:
  140          amount: totalAmount,
  141:         email: authProvider.userEmail.isNotEmpty ? authProvider.userEmail : 'buyer@agrilink.et',
  142          firstName: authProvider.userName.isNotEmpty ? authProvider.userName : 'Buyer',

AgriLink-main\agridirect_app\lib\screens\marketplace_screen.dart:
  432                                    Text(
  433:                                     'AgriLink',
  434                                      style: TextStyle(

AgriLink-main\agridirect_app\lib\screens\profile_screen.dart:
  249          title: const Text('Logout'),
  250:         content: const Text('Are you sure you want to sign out of AgriLink?'),
  251          actions: [

AgriLink-main\agridirect_app\lib\screens\splash_screen.dart:
  61                const Text(
  62:                 'AgriLink Ethiopia',
  63                  style: TextStyle(

AgriLink-main\agridirect_app\lib\screens\auth\login_screen.dart:
   54              const SnackBar(
   55:               content: Text('Account created successfully! Welcome to AgriLink.'),
   56                backgroundColor: Color(0xFF1B6B3A),

  129                    Text(
  130:                     t.translate('AgriLink Ethiopia'),
  131                      style: const TextStyle(

  253                            ? t.translate('Already have an account? Sign In')
  254:                           : t.translate('New to AgriLink? Sign Up'),
  255                        style: const TextStyle(color: Color(0xFF1B6B3A)),

AgriLink-main\agridirect_app\lib\services\auth_service.dart:
  129              'user_id': response.user!.id,
  130:             'title': 'Welcome to AgriLink! 👋',
  131              'body': 'We\'re glad to have you here. Start exploring the marketplace or meet our farmers!',

AgriLink-main\agridirect_app\lib\services\email_service.dart:
  12    Future<void> sendWelcomeEmail(String email, String name) async {
  13:     _logEmail('Welcome', email, 'Hello $name, welcome to AgriLink Ethiopia! Your account is ready.');
  14      // Implementation note: This would call an Edge Function or Email API

AgriLink-main\agridirect_app\lib\services\invoice_service.dart:
  20                  children: [
  21:                   pw.Text('AgriLink Ethiopia - INVOICE', style: pw.TextStyle(fontSize: 24, fontWeight: pw.FontWeight.bold, color: PdfColors.green)),
  22                    pw.Text('Date: ${DateTime.now().toString().split(' ')[0]}'),

AgriLink-main\agridirect_app\lib\services\payment_service.dart:
  37          'customization': {
  38:           'title': 'AgriLink Ethiopia',
  39            'description': 'Payment for your order #$txRef',

AgriLink-main\agridirect_app\lib\setup\fix_all.sql:
  1  -- ═══════════════════════════════════════════════════════════════
  2: -- AgriLink — ONE-SHOT FIX (paste this entire block and click Run)
  3  -- Safe: won't delete or overwrite any existing data

AgriLink-main\agridirect_app\lib\setup\migration.sql:
  1  -- =============================================================================
  2: -- AgriLink Ethiopia — MIGRATION Script (Safe to run on existing database)
  3  -- Run this in Supabase Dashboard → SQL Editor

AgriLink-main\agridirect_app\lib\setup\supabase_schema.sql:
  1  -- =============================================================================
  2: -- AgriLink Ethiopia — Complete Supabase Schema
  3  -- Updated: 2026-05-12
