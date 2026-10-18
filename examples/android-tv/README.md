# Android TV Harness

A separate, runnable specialization of Vertical Harness for **Android TV and Google TV**. It combines the native tv-vibehack launcher with verified ADB inventory, saved change plans, restricted package operations, execution checkpoints, screenshots and restoration.

**Repository:** [harshith-vaddiparthy/Android-TV-Harness](https://github.com/harshith-vaddiparthy/Android-TV-Harness)

The TV-facing addition is one **@J.A.R.V.I.S.** button. Its future agent workspace connection is deferred. The harness has a JSON CLI and optional stdio MCP adapter; no Hermes configuration is included.

```bash
git clone https://github.com/harshith-vaddiparthy/Android-TV-Harness.git
cd Android-TV-Harness
python3 -m harness doctor
```

Follow that repository's [build and setup instructions](https://github.com/harshith-vaddiparthy/Android-TV-Harness#build). JDK 17, Android SDK 34 and platform-tools are needed for the Android build; Python 3.10+ runs the harness. Build-only work does not change a TV. Device operations require an explicit authorized ADB target and a reviewed plan.

Local runtime tests, Android JVM tests, APK build and lint pass. Native screen, D-pad button focus and the disconnected message were verified in an isolated Android TV 14 emulator. Its stock Home priority prevents default launcher selection; the harness detects that mismatch and recovers. Real-TV compatibility and a connected Hermes workspace remain separate verification steps.

This specialization applies to Android TV/Google TV devices with the required debugging and launcher capabilities. It does not support Samsung Tizen, LG webOS or generic non-Android TVs. Keep the reusable template here and the application/runtime implementation in the separate repository.
