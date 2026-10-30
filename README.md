# CBSE Class 10 Android Widget (GitHub build)

This project builds an Android app with a real home-screen widget. The app opens your GitHub Pages checklist and syncs its ticked checkboxes to the widget.

## Before building
1. Publish your checklist website on GitHub Pages (use the separate GitHub-ready website ZIP).
2. In `app/src/main/res/values/strings.xml`, replace `https://YOUR-USERNAME.github.io/YOUR-REPO/` with your actual Pages URL.
3. Commit the change.

## Build from your Android phone using GitHub Actions
1. Create a new GitHub repository and upload **all files and folders** from this ZIP (including the hidden `.github` folder).
2. Open the repository's **Actions** tab and enable Actions if asked.
3. Select **Build Android APK**. It also runs automatically after you push a commit.
4. Open a successful run, scroll to **Artifacts**, and download `CBSE-Checklist-debug-apk`.
5. Extract the artifact ZIP and install `app-debug.apk` on your phone.

## Add the widget
1. Open the installed CBSE Checklist app once and wait for the checklist to load.
2. Tick or untick chapters **inside the app** to sync progress.
3. Long-press an empty area on your home screen → Widgets → CBSE Progress → drag it onto the screen.

## Important limitations
- The widget is a native Android widget and shows overall progress plus subject progress for Mathematics, Science, Social Science, English, Hindi A and AI.
- It syncs changes made in the checklist opened **inside this app**. It cannot directly read the separate Chrome-installed PWA's local storage. Use the Android app as your checklist if you want the widget to stay updated.
- Internet is needed to load the hosted checklist. Offline behavior depends on the website service worker cache being available from a previous load.
- This ZIP contains source code and an automated GitHub build workflow, **not a prebuilt APK**. GitHub Actions compiles the APK for you.
