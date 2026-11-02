<div align="center">

# 📱 Business Management Mobile App

**A secure, notification-driven Flutter companion app that puts a company's web platform, inbox, members and revenue in your pocket.**

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat-square&logo=dart&logoColor=white)
![GetX](https://img.shields.io/badge/State-GetX-8A2BE2?style=flat-square)
![Firebase](https://img.shields.io/badge/Firebase%20Cloud%20Messaging-FFCA28?style=flat-square&logo=firebase&logoColor=black)
![iOS](https://img.shields.io/badge/iOS-000000?style=flat-square&logo=apple&logoColor=white)
![Android](https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=android&logoColor=white)

</div>

> 🔒 **Source code is private** (commercial project). This page documents what I built, the engineering decisions behind it, and the results. Architecture walkthroughs are available on request.

---

## 🎯 The problem

Business owners and team managers needed to stay on top of their web platform — messages, members, revenue and activity — **without being tied to a desktop**. Email-style alerts were easy to miss, and opening the right page after a notification meant extra taps and logins.

## 💡 The solution

A cross-platform mobile app (one Flutter codebase for **iOS and Android**) that wraps the company's web platform in a fast, native experience, adds **push notifications that deep-link straight to the right screen**, and protects access with **biometric login**.

---

## ✨ Key features

| Feature | What it does for the user |
|---|---|
| 🔔 **Smart push notifications** | Tapping a notification opens the exact website and screen it relates to — no hunting, no extra taps. |
| 🔐 **Biometric authentication** | Face ID / fingerprint unlock with credentials kept in the device's secure storage. |
| 📥 **Inbox with smart sorting** | Messages sorted so the newest and most relevant conversations come first. |
| 👥 **Members & 💰 Revenue views** | At-a-glance business metrics and member management on the go. |
| 🧭 **Activity feed** | Real-time overview of what's happening across the platform. |
| 🌐 **Embedded web experience** | Native navigation (bottom bar, drawers) around the web platform for a seamless feel. |
| 🔑 **Account flows** | Login, forgot password, privacy policy and terms — store-compliant out of the box. |

---

## 🏗️ Architecture & engineering highlights

- **Feature-first modular structure** — each screen (`inbox`, `members`, `revenue`, `activity`, `login`, …) is an isolated module with its own controller, view and binding, making the app easy to extend and test.
- **GetX** for state management, dependency injection and route management — minimal boilerplate, fast iteration.
- **Service layer** separating concerns: API client, notification routing, biometric auth and local preferences.
- **Notification router** that maps push payloads to the correct website + in-app screen, including cold-start and background-tap scenarios.
- **Secure by design** — sensitive data stored with `flutter_secure_storage`; biometric checks via `local_auth`; no secrets in source control.
- **Cross-platform release pipeline** — Firebase configuration, bundle IDs and platform-specific iOS credential handling managed for both stores.
- **Actively maintained** — continuously upgraded with the latest Flutter SDK (Dart 3.9) and dependency updates.

```
lib/
├── app/
│   ├── modules/        # activity · inbox · members · revenue · login · splash …
│   └── routes/         # centralized navigation
├── config/             # environment & theming
├── services/           # api · biometric_auth · notification_router · notifications · prefs
└── widgets/            # reusable UI components
```

## 🧰 Tech stack

**Flutter · Dart · GetX · Firebase Cloud Messaging · flutter_local_notifications · WebView · local_auth · flutter_secure_storage · REST APIs · Shared Preferences · Custom typography (Axiforma)**

---

## 📸 Screenshots

<!-- Replace with real screenshots, e.g. <img src="screenshots/home.png" width="220"/> -->
*Screenshots available on request.*

---

## 🤝 Need something similar built?

I design and ship production-ready mobile apps like this for startups and businesses — from idea to App Store.

📫 **sibghat.developlogix@gmail.com** · 🌐 **[developlogix.com](https://www.developlogix.com)** · 💼 **[LinkedIn](https://www.linkedin.com/in/sibghat-ullah-baig-4a2812a1)**

<sub>Built by [Develop Logix](https://www.developlogix.com)</sub>
