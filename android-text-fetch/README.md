# Config Loader APK (legal)

WebView shell (jaise Virtus **structure**), lekin **bina** Firebase clients, bank SMS, UPI PIN, ya device steal logic.

## Behaviour

1. App open → turant tumhari **TEXT_URL** se plain `.txt` fetch.
2. Fail ho to `assets/default.txt`.
3. **📂 Local TXT** — phone se koi bhi text file padho (sirf display).
4. **🔄 Reload** — dubara URL se fetch.

## Virtus jaisa nahi

Virtus Panel = stolen device dashboard (illegal). Ye app = **sirf config/text** dikhata hai.

## Build

Android Studio ya:

```bash
export ANDROID_HOME=...   # SDK path
cd android-text-fetch
./gradlew assembleDebug
```

APK: `app/build/outputs/apk/debug/app-debug.apk`

## Apni text file online

`app/build.gradle.kts` mein:

```kotlin
buildConfigField("String", "TEXT_URL", "\"https://YOUR-HOST/config.txt\"")
```

Rebuild.

## Customize UI

Edit `app/src/main/assets/app.html` — Firebase / SMS code mat daalna agar public store par daalna ho.
