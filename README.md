# 🐾 Easy Learning – AR Animals for Kids

**Easy Learning** is an educational Flutter app that uses **Augmented Reality (AR)** to teach children about animals. Kids can view animals in AR, hear their sounds, learn facts and take quizzes, in **Arabic** or **English**.

---

## 🚀 Features

- 🐾 **Explore animals** – pick an animal from the in-app wheel and view it in AR on a detected surface.
- 📸 **Scan mode** – point the camera at animal images (e.g. from a printed book) to make the AR content appear (ARCore Augmented Images).
- 🔈 **Animal sounds** – each animal has its own sound; sound effects for selecting, right and wrong answers, and finishing a quiz.
- 🧠 **Quizzes** – test knowledge with questions, with text-to-speech reading the question in English.
- 🎉 **Rewards** – coins and confetti celebrations when a quiz is completed.
- 🗣️ **Bilingual** – Arabic and English, switchable in Settings.
- 🧭 **First-run tutorial** – a one-time guided tour explaining each button.
- ℹ️ **About Us / Contact Us** screens, plus a login screen.

---

## 🧪 Tech Stack

| Area | Package |
| --- | --- |
| Framework | Flutter (Dart) |
| AR | `arcore_flutter_plugin` (Android / ARCore) |
| State management & routing | `get` (GetX) |
| Audio | `just_audio` |
| Text to speech | `flutter_tts` |
| Local storage | `shared_preferences` |
| UI helpers | `flutter_svg`, `confetti`, `circle_wheel_scroll`, `tutorial_coach_mark`, `auto_size_text` |
| Links | `url_launcher` |

---

## 📁 Project Structure

```
lib/
├── main.dart              # Entry point (ARCore checks, SharedPreferences)
├── app.dart               # Root GetMaterialApp
├── common/                # Assets paths, constants, localization, routes, theme
├── model/                 # Animal and quiz models
├── module/                # Screens: splash, login, home, animal_view, animal_quaz, setting, about_us, connect_us
└── widgets/               # Reusable widgets
```

---

## ⚙️ Requirements

- Flutter **2.10.x – 3.0.x** (Dart `>=2.2.2 <3.0.0`; the code is not null-safe)
- Android Studio with the Android SDK
- A physical **Android phone that supports ARCore** (AR does not work on most emulators)
- Google Play Services for AR installed on the phone

---

## ▶️ Getting Started

1. Open the project folder in VS Code (with the Flutter and Dart extensions).
2. If there is no `android/` folder, generate it:
   ```bash
   flutter create --platforms=android .
   ```
3. In `pubspec.yaml`, point the AR plugin at the published package instead of the local path:
   ```yaml
   arcore_flutter_plugin: ^0.0.9
   ```
4. In `android/app/build.gradle`, set `minSdkVersion 24`. In `AndroidManifest.xml`, add the camera permission, `<uses-feature android:name="android.hardware.camera.ar" android:required="true"/>` and `<meta-data android:name="com.google.ar.core" android:value="required"/>`.
5. Make sure the asset folders listed in `pubspec.yaml` exist and contain the files referenced in `lib/common/assets/` (`assets/images/png`, `assets/images/svg`, `assets/sounds`, `assets/translations`).
6. Install packages and run on a connected device:
   ```bash
   flutter pub get
   flutter run
   ```

---

## 📚 Educational Value

- Builds visual recognition of animals
- Reinforces memory through interactive quizzes
- Encourages exploration with AR
- Supports Arabic and English literacy

---

## 👥 Credits

- **Original author:** Mahmoud Alaa – [LinkedIn](https://www.linkedin.com/in/mahmoudalaa2210/) • [GitHub](https://github.com/Mahmoud3laa)
- **Modified and documented by:** Remoen Reda Eid Henein

---

## 📜 License

This project is licensed under the **MIT License**. The original copyright notice and attribution to Mahmoud Alaa must be kept with all copies and modified versions.
