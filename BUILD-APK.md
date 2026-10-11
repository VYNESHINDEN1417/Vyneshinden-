# Build the APK

This is your portfolio converted from a server-rendered TanStack Start site into a
static app wrapped with Capacitor 8 (targets Android 15/16, includes edge-to-edge handling).
All media (GIF, music, font, textures) is bundled inside the APK, so it works offline.

## Option A — no installs, free (GitHub Actions)
1. Create a new GitHub repository and upload everything in this folder
   (make sure the hidden `.github` folder is included).
2. Open the repo's **Actions** tab → **Build Android APK** → **Run workflow**
   (it also runs automatically on every push to `main`).
3. When it finishes (about 5–8 minutes), open the run and download the
   **vyneshinden-portfolio-apk** artifact. Unzip it to get `vyneshinden-portfolio.apk`.
4. Copy the APK to the Infinix Hot 60 Pro, tap it, and allow "Install unknown apps"
   for your file manager/browser when asked.

## Option B — on your computer
Needs Node 22+, JDK 21 and the Android SDK (installing Android Studio gives you the SDK).
```
npm install
npm run android
```
The APK is written to `output/vyneshinden-portfolio.apk`.

## Preview in a browser first
```
npm install
npm run dev
```

## Notes
- The APK is debug-signed, which is fine for installing on your own phone.
  (Play Store uploads need a separate release-signed build.)
- App id is `com.vyneshinden.portfolio` (edit `capacitor.config.json` to change it).
- The app is locked to portrait.
