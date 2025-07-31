# mo_sh

A new Flutter project.


# 🌐 Domain Track - Mobile App

Domain Track is a cross-platform mobile application built with **Flutter**, designed to allow users to query domain availability and fetch WHOIS registration details such as registrar, creation/expiration dates, and emails.

> 🛰️ This mobile app works in conjunction with the backend service: [Whois_py_service](https://github.com/celalaygar/Whois_py_service)

---

## 📱 Features

- 🔍 Search for domain names across multiple TLDs (extensions)
- 🟢 Instantly check if a domain is available or registered
- 🧾 View detailed WHOIS information of registered domains
- 🗂️ Filter domain extensions (e.g., .com, .net, .org)
- 📆 See registrar, registration dates, and contact emails
- 🧠 Intelligent formatting of WHOIS response data
- 🌗 Clean and modern UI with support for dialogs and validation

---

## 📸 Screenshots

> _(You can add screenshots here for better visualization)_  
> ![screenshot1](assets/screenshots/search_screen.png)  
> ![screenshot2](assets/screenshots/result_details.png)

---

## 🛠️ Technologies Used

- **Flutter (Dart)**
- **HTTP Client** (for backend communication)
- **Material Design**
- **url_launcher** (optional future use)
- **Clipboard & AlertDialog**
- RESTful API integration with [Whois_py_service](https://github.com/celalaygar/Whois_py_service)

---

## 🔗 Backend API Integration

This app communicates with a RESTful API built using Python and Flask, hosted in the companion project:

👉 [`Whois_py_service`](https://github.com/celalaygar/Whois_py_service)

The backend provides:
- `/whois_api/check_domains`: WHOIS lookup for given domain and extensions
- `/whois_api/get_extensions`: List of supported domain extensions (TLDs)

You must update the API base URL (currently hardcoded as `http://1.1.1.1:1111`) in `service.dart` to match your backend deployment:

```dart
const String baseUrl = "http://<your_backend_ip>:<port>/whois_api";
```

---

## 🚀 Getting Started

### Prerequisites

- Flutter SDK installed
- Android Studio / Xcode for emulator or physical device testing
- A running instance of [Whois_py_service](https://github.com/celalaygar/Whois_py_service)

### Installation

1. Clone this repository:

```bash
git clone https://github.com/celalaygar/Domain-Track-Mobile-App.git
cd Domain-Track-Mobile-App
```

2. Install dependencies:

```bash
flutter pub get
```

3. Run the app:

```bash
flutter run
```

---

## ⚙️ Configuration

Edit `service.dart` to point to your live backend:

```dart
final String baseUrl = "http://<your_backend_ip>:<port>/whois_api/check_domains";
```

Make sure CORS and network permissions are properly configured, especially for Android (`AndroidManifest.xml`) and iOS (`Info.plist`).

---

## 📂 Project Structure (Simplified)

```
lib/
├── main.dart         # Main entry point of the app
├── service.dart      # HTTP service to communicate with backend
├── assets/           # (Optional) Images and icons
└── ...
```

---

## 📌 Notes

- The WHOIS data comes from public databases. Accuracy and availability depend on the data returned by registrars.
- This project is intended for educational and research purposes.
- The app UI supports basic error handling and feedback dialogs.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 🤝 Contributing

Contributions, suggestions, and improvements are welcome! Feel free to open issues or pull requests.

---

## 👤 Author

Developed by [Celal Aygar](https://github.com/celalaygar)  
💼 Java & Full Stack Developer | AI Enthusiast  
🔗 [LinkedIn](https://www.linkedin.com/in/celalaygar/) | [GitHub](https://github.com/celalaygar)

---

## 📬 Contact

For feedback or questions, feel free to reach out via [GitHub Issues](https://github.com/celalaygar/Domain-Track-Mobile-App/issues).
