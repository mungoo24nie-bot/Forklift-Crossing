# Forklift Crossing — Android test build

This repository packages the original Forklift Crossing v4 HTML game using Capacitor. No shop, Supabase or internet connection is required to play.

## Build in GitHub Actions (phone-friendly)
1. Create a new **private** GitHub repository with branch `main`.
2. Upload the project files, preserving folders `www/` and `.github/workflows/`.
3. Open **Actions → Build Android APK → Run workflow** (or push to `main`).
4. Wait for a green check, open the completed run and download artifact `forklift-crossing-debug-apk`.
5. Unzip the artifact on your phone and install `app-debug.apk` (Android may ask permission to install from this source).

The APK is a **debug build for personal testing**, not a Google Play release. Google Play requires a release-signed AAB, a stable application ID, icon and store metadata, and current target API compliance.

## Local build (optional)
`npm install && npx cap add android && cd android && ./gradlew assembleDebug`
