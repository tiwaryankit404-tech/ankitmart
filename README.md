# Ankit Mart — Android APK Project (No Android Studio Required)

This project packages the supplied Ankit Mart mobile `index.html` into an Android WebView app.

## What is included

- The uploaded Ankit Mart `index.html` is copied unchanged into the Android app assets.
- The existing product API URL remains inside the HTML.
- The existing order API URL remains inside the HTML.
- Mobile/portrait Android app shell.
- JavaScript and localStorage/DOM storage enabled.
- Internet permission for API/product/order requests.
- Launcher/splash logo extracted from the supplied HTML logo.
- GitHub Actions workflow that builds an installable `app-debug.apk` in the cloud.
- No Android Studio is required for the cloud build.

## Build the APK for free without Android Studio

1. Create/sign in to a GitHub account.
2. Create a new repository, for example `AnkitMart`.
3. Upload **all files and folders inside this ZIP** to that repository.
4. Open the repository's **Actions** tab.
5. Select **Build Ankit Mart APK**.
6. Click **Run workflow**.
7. Wait for the build to finish successfully.
8. Open the completed workflow run.
9. Under **Artifacts**, download `AnkitMart-APK`.
10. Extract the downloaded artifact ZIP. It contains `app-debug.apk`.
11. Transfer `app-debug.apk` to your Android phone and tap it to install.

The debug APK is signed for testing and can be installed directly on an Android phone.

## If Android blocks the installation

Android may show a message that installation from that source is not allowed. Allow installation of unknown apps for the browser/file manager you used to open the APK, then try again.

## Important

The ZIP is the **source project**, not the APK itself. The APK is produced by the included GitHub Actions workflow. This avoids needing Android Studio on the school computer.

## Project structure

```text
AnkitMart/
├── .github/workflows/build-apk.yml
├── app/
│   ├── build.gradle
│   └── src/main/
│       ├── AndroidManifest.xml
│       ├── assets/index.html
│       ├── java/com/ankitmart/app/MainActivity.java
│       └── res/
├── build.gradle
├── gradle.properties
└── settings.gradle
```
