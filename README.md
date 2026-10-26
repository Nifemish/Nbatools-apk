# TrackPort APK

## Easiest: build online (no installs)
1. Create a free GitHub repo and upload everything in this folder (keep the hidden `.github` folder).
2. Open the repo > Actions > "Build Android APK" (it runs on push; or click Run workflow).
3. When it finishes (~5 min), open the run > Artifacts > download `TrackPort-apk`, unzip -> `app-debug.apk`.
4. Send that APK to any Android phone, tap it, allow "Install unknown apps", install.

## Or build locally (Node 20, JDK 17, Android Studio/SDK)
npm install && npx cap add android && npx cap sync android
cd android && ./gradlew assembleDebug
APK: android/app/build/outputs/apk/debug/app-debug.apk

## Updating the app
Replace www/index.html, push again (or `npx cap sync android` locally), rebuild.
