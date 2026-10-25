# Stockfish Study (Android)

This is an Android Studio starter project for an offline chess-analysis app.
It is intended for study/review, not covert assistance during live Chess.com games.

## Important
This source project does **not** include a precompiled Stockfish engine or a signed APK.
The app expects a compatible UCI engine executable to be selected/copied into its private
files directory as `stockfish`. Android versions/devices differ in whether executable
files can be launched from app-private storage, so the engine-launch path may need a
JNI/native-library integration for a production release.

## Build
1. Open this folder in Android Studio with Android SDK installed.
2. Allow Gradle to sync.
3. Build > Build APK(s).

The UI is a basic analysis shell; it accepts a FEN and shows the engine output when a
working UCI executable is available. The engine must support `uci`, `isready`, `position`,
`go depth`, and `quit`.

## Stockfish license
Stockfish is GPL-3.0-or-later. If you distribute a build containing Stockfish, include
the corresponding license and source/offer required by the GPL. See:
https://github.com/official-stockfish/Stockfish


## Build APK using GitHub Actions
1. Create a GitHub repository and upload this project to its `main` branch.
2. Open the repository's **Actions** tab.
3. Select **Build Android APK** and press **Run workflow**, or push a commit to `main`.
4. Open the completed workflow run and download `StockfishStudy-debug-apk` under **Artifacts**.
5. Extract the artifact ZIP and install `app-debug.apk` on Android.

The generated APK is a debug build. It is an analysis UI shell; the Stockfish executable is not bundled yet.
