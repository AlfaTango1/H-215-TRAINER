AS 532 AL Trainer — Android project
====================================

HOW TO BUILD THE APK
1. Install Android Studio (free): https://developer.android.com/studio
2. Unzip this folder. In Android Studio: File > Open > select the "AS532Trainer" folder.
3. Wait for "Gradle sync" to finish (first time downloads Gradle/SDK, needs internet).
4. Menu: Build > Build App Bundle(s) / APK(s) > Build APK(s).
5. Click "locate" in the popup. The file is:
   app/build/outputs/apk/debug/app-debug.apk
6. Copy it to the phone and open it (allow "Install unknown apps" for your file manager).

Or connect the phone with USB debugging on and press the green Run button.

UPDATING THE CONTENT
Replace app/src/main/assets/index.html with the new version of the trainer,
raise versionCode in app/build.gradle (1 -> 2), and rebuild.

NOTES
- Works fully offline. Progress is saved on the phone (WebView localStorage).
- Minimum Android 7.0 (API 24).
- The phone Back button closes an open lesson, then exits.
- For a signed release APK: Build > Generate Signed Bundle / APK.

BUILD ON GITHUB (no Android Studio needed)
1. Create a new repository on github.com.
2. Upload ALL files of the AS532Trainer folder, including the hidden
   ".github" folder (.github/workflows/build.yml).
3. GitHub builds the app automatically (tab "Actions", about 3-5 min).
4. Download AS532-Trainer.apk from the "Releases" section of the repository.
Every new upload/commit produces a new build.
