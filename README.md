## 🔧 After Cloning: Change the Package Name

To use your own Firebase project or publish this app, you must change the **package name** throughout the Android part of the app.

---

### ✅ Step 1: Update `applicationId` in `build.gradle`

Open:

```
android/app/build.gradle
```

Find the line:

```gradle
applicationId "com.example.messenger"
```

Change it to your desired package name:

```gradle
applicationId "com.yourname.myapp"
```

---

### ✅ Step 2: Rename Java/Kotlin Folder Structure

Navigate to:

```
android/app/src/main/java/com/example/messenger/
```

Now rename the folders to match your new package name:

Example:

```
com/example/messenger → com/yourname/myapp
```

> ⚠ Do **not** rename folders manually!
> Use **Android Studio** → right-click each folder → **Refactor > Rename**

This updates all references safely.

---

### ✅ Step 3: Update Package Declaration in `MainActivity`

Open:

```
android/app/src/main/java/com/yourname/myapp/MainActivity.kt
```

Change the first line to:

```kotlin
package com.yourname.myapp
```

This must match your new folder path and `applicationId`.

---

### ✅ Step 4: Update AndroidManifest.xml

Open:

```
android/app/src/main/AndroidManifest.xml
```

Update the package line at the top:

```xml
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.yourname.myapp">
```

---

### ✅ Step 5: Clean and Run the Project

After all changes are made, run the following in your terminal:

```bash
flutter clean
flutter pub get
flutter run
```

This will rebuild the app with your updated package configuration.

---

## 🔥 Firebase Setup (Required)

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Add a new project or select an existing one
3. Register a new Android app using your updated package name (e.g. `com.yourname.myapp`)
4. Download the `google-services.json` file
5. Place it in:

   ```
   android/app/google-services.json
   ```

---

## 📂 Useful Flutter Resources

* [Flutter Docs](https://docs.flutter.dev/)
* [Firebase for Flutter](https://firebase.flutter.dev/)
* [Rename Flutter Package Guide](https://stackoverflow.com/questions/51534616/how-to-change-package-name-in-flutter)

---

## ✅ Done!

Now you're ready to build and launch your customized messaging app with Firebase!
