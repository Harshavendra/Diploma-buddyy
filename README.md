# Diploma Buddy AI – Native Android App (Kotlin & Jetpack Compose)

**Tagline:** Learn Better. Understand Faster.  
**Package Name:** `com.diplomabuddy.ai`  
**Target Platform:** Modern Android Phones (Android 8.0 / API 26 through Android 14+ / API 34)  
**Founder Contact:** `m20697524@gmail.com`  

---

## 1. Project Overview

Diploma Buddy AI is a native Android application built using:
- **Language:** Kotlin (1.9.22)
- **UI Framework:** Jetpack Compose (Material3)
- **Architecture:** MVVM with Kotlin Coroutines & StateFlow
- **Networking:** Retrofit 2 with OkHttp logging & Gson serialization
- **Security:** Zero client-side API keys; communicates directly with the secure backend proxy

### Features Included:
1. **AI Chat Assistant:** Step-by-step technical explanations in 10 languages with technical English terms preserved.
2. **Explain Any Topic:** Definitions, exam points, mechanisms, and workshop examples.
3. **Notes Generator:** Exam-ready 5-section revision notes with one-click copy.
4. **Quiz & MCQ Generator:** 5, 10, or 20 multiple choice questions with timer, grading, and explanations.
5. **PDF & Syllabus Assistant:** Analyze lecture notes, textbook chapters, and extract exam questions.
6. **Language Support:** English, Telugu, Hindi, Tamil, Kannada, Malayalam, Marathi, Bengali, Gujarati, Punjabi.
7. **Profile & About Us:** View founder details, diploma branch, year of study, and billing tier.

---

## 2. How to Build the Android APK (`app-debug.apk`)

### Option A: Using Android Studio (Recommended)
1. Download and extract `DiplomaBuddyAI-Android-Native.zip`.
2. Open **Android Studio** (Hedgehog, Iguana, Jellyfish, or newer).
3. Select **File > Open** and choose the `android` folder.
4. Allow Gradle to sync dependencies automatically.
5. In the top toolbar, select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
6. Android Studio will generate the APK at:
   ```
   app/build/outputs/apk/debug/app-debug.apk
   ```
7. Click **"locate"** in the popup to get your APK file, transfer it to your Android device via USB/Drive, and install!

### Option B: Using Command Line (Terminal / Command Prompt)
Make sure you have JDK 17 installed:
```bash
# On Linux / macOS:
cd android
chmod +x gradlew
./gradlew assembleDebug

# On Windows:
gradlew.bat assembleDebug
```
The resulting debug APK will be created at:
```
android/app/build/outputs/apk/debug/app-debug.apk
```

---

## 3. How to Install on Your Android Phone

1. Transfer `app-debug.apk` to your phone via USB cable, Google Drive, or WhatsApp/Telegram.
2. Open the file on your Android phone using your **Files** or **Downloads** app.
3. If prompted with *"Install unknown apps"*, tap **Settings** and toggle **"Allow from this source"**.
4. Tap **Install** and open **Diploma Buddy AI**!

---

## 4. Releasing Future Updates Safely

To ensure existing users receive seamless updates without losing their local data:
1. **Keep the same package name:** Always maintain `applicationId = "com.diplomabuddy.ai"`.
2. **Increment versionCode:** In `app/build.gradle.kts`, increment `versionCode` by 1 for each new release (e.g. `versionCode = 2`, `versionName = "1.0.1"`).
3. **Use the same keystore:** For release APKs or Google Play App Bundles (`.aab`), create and safely back up your release keystore (`.jks`). Android requires the exact same signing key for updates to overwrite previous versions cleanly.
