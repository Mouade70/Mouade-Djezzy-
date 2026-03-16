# 🚀 Djezzy Pro v3.0 — دليل البناء
## من مطور معاذ جلال | @MouadeTEK | 🇩🇿

---

## 📦 هيكل المشروع (20 ملف Dart — 4045 سطر)

```
djpro/
├── pubspec.yaml                    ← تعريف المشروع
├── lib/
│   ├── main.dart                   ← نقطة الدخول
│   ├── core/
│   │   ├── theme/app_colors.dart   ← نظام الألوان
│   │   ├── theme/app_theme.dart    ← Material 3 Theme
│   │   └── constants/api_constants.dart ← API Config + MGM limits
│   ├── data/
│   │   ├── services/djezzy_api.dart  ← API مباشر (خوارزمية 1Go_v1.py)
│   │   ├── models/service_model.dart ← 18 خدمة Djezzy
│   │   └── models/models.dart        ← MGM tracker, Account, USSD
│   └── presentation/
│       ├── providers/app_provider.dart ← MVVM State
│       ├── widgets/pro_widgets.dart    ← مكونات UI احترافية
│       └── screens/
│           ├── splash/              ← شاشة البداية
│           ├── auth/                ← تسجيل الدخول OTP
│           ├── home/                ← لوحة القيادة
│           ├── services/            ← 18 خدمة (Tabs: مجاني/مدفوع/تحكم)
│           ├── mgm/                 ← MGM مع حد 5/16 يوم
│           ├── walk/                ← Walk & Win + 3GB Hack
│           ├── recharge/            ← شحن بالكود + Keypad
│           ├── ussd/                ← أكواد USSD مع نسخ
│           ├── profile/             ← حسابات + إعدادات
│           └── about/               ← معلومات المطور
└── android/                        ← Android config
    └── app/
        ├── build.gradle            ← Package: dz.mouadetek.djezzypro
        └── src/main/
            ├── AndroidManifest.xml
            └── res/xml/network_security_config.xml
```

---

## 🔑 خوارزمية MGM — منقولة حرفياً من 1Go_v1.py

```dart
// الخطوات (كما في Python script معاذ جلال):
// 1. توليد رقم عشوائي (077/078/079 + 7 أرقام)
// 2. إرسال دعوة MGM للرقم العشوائي
// 3. تسجيل الرقم العشوائي (request_otp)
// 4. انتظار ثانيتين (كما في البوت الأصلي)
// 5. تفعيل المكافأة للمرسل
// 6. تكرار حتى 50 مرة أو النجاح
// + حد إضافي: 5 تفعيلات كل 16 يوم (ميزة Pro جديدة)
```

---

## 🏗️ خطوات البناء

### المتطلبات:
- Flutter 3.22+
- Android Studio / VS Code
- Android SDK 35

### الأوامر:
```bash
cd djpro
flutter pub get
flutter run                    # تشغيل مباشر
flutter build apk --release    # بناء APK Release
```

### APK مسار:
```
build/app/outputs/flutter-apk/app-release.apk
```

---

## ✅ الميزات المكتملة

| الميزة | الحالة |
|--------|--------|
| تسجيل الدخول OTP | ✅ |
| رصيد + إنترنت (API مباشر) | ✅ |
| 18 خدمة Djezzy | ✅ |
| MGM (خوارزمية 1Go_v1.py) | ✅ |
| حد 5 تفعيلات / 16 يوم | ✅ |
| شحن الرصيد بكود | ✅ |
| Keypad لإدخال الكود | ✅ |
| Walk & Win + 3GB Hack | ✅ |
| أكواد USSD مع نسخ | ✅ |
| تصفية حسب الفئة | ✅ |
| إدارة حسابات متعددة | ✅ |
| واجهة داكنة احترافية | ✅ |
| بدون سيرفر | ✅ |

---

## 📱 معلومات التطبيق

- **Package**: dz.mouadetek.djezzypro
- **Version**: 3.0.0
- **Min SDK**: 24 (Android 7.0)
- **Target SDK**: 35 (Android 15)
- **API**: apim.djezzy.dz (مباشر)

---

## 👨‍💻 المطور

**معاذ جلال** | Mouad Djallel  
📺 @MouadeTEK | 🇩🇿 الجزائر  
Djezzy Pro v3.0 | من مطور معاذ جلال
