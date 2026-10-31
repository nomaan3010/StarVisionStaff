STAR VISION STAFF APP - Android Studio project
==============================================

This app opens your Star Vision staff page (login, add/edit routers, WhatsApp) inside a normal Android app.
All data stays in your Google Sheet, so you never rebuild the app when records change.

STEP 1 - Install Android Studio (free, on a Windows/Mac/Linux computer)
  https://developer.android.com/studio

STEP 2 - Open the project
  Android Studio > File > Open > choose the unzipped "StarVisionStaff" folder.
  Wait for "Gradle sync" to finish (first time needs internet and a few minutes).
  If it asks to update anything, choose to keep the versions in this project.

STEP 3 - Put the Star Vision logo as the app icon
  Right-click app/src/main/res > New > Image Asset
  Icon Type: Launcher Icons (Adaptive and Legacy)
  Path: choose your logo file (PNG, at least 512x512 - download it from your Drive link)
  Adjust the padding so the logo sits inside the circle, then Next > Finish.
  (A simple red "SV" placeholder icon is included so the app builds before you do this.)

STEP 4 - Build the APK
  Build > Build Bundle(s) / APK(s) > Build APK(s)
  When it finishes, click "locate" in the popup. The file is app-debug.apk.

STEP 5 - Send to staff
  Send app-debug.apk on WhatsApp or Google Drive. On the staff phone tap the file and install.
  Android will ask to allow installs from this source - allow it.
  Staff open "Star Vision Staff", sign in once, and stay signed in for 30 days.

CHANGING THE LINK
  If you ever make a NEW deployment (new URL), edit APP_URL in
  app/src/main/java/com/starvision/staff/MainActivity.java and rebuild.
  Using Deploy > Manage deployments > Edit > New version keeps the same URL, so no rebuild is needed.

NOTES
  - Android only. iPhone cannot install APK files.
  - The QR "Download" button on the dashboard does not save files inside the app.
    Create and download the customer QR from a normal phone/computer browser instead.
