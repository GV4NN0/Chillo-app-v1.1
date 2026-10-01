# Chillo

A mobile game coach with a friendly periwinkle cat. Version 0.1 (starter):

- Chillo on the home screen (blinks, bobs, changes face with your results and the time of day, double-tap to chat)
- One-tap Win / Loss logging with a loss-streak check
- Take five: Chillo asks for a high five, then runs a 5-minute break timer
- Mood picker (Chilling, Restless, Want to improve, Tired) that picks from your games
- Game profiles for MLBB, Honor of Kings, CODM, Free Fire, PUBG Mobile and Bloodstrike (Serious or Fun, difficulty, your reason)
- Everything is stored on the phone. No account, no server.

## Get the APK without Android Studio

1. Create a new **private** repository on GitHub called `chillo-app`.
2. Upload everything from this folder to it (keep the `.github` folder, it holds the build recipe).
   If your computer hides the `.github` folder, use **Add file > Create new file** on GitHub, type
   `.github/workflows/build-apk.yml` as the name, and paste the contents of that file.
3. Open the **Actions** tab. The **Build Chillo APK** run starts by itself (or press **Run workflow**).
4. When it turns green, open the run and download **chillo-debug-apk** under Artifacts. Unzip it.
5. Copy `app-debug.apk` to your phone, tap it, and allow installs from this source when asked.

If the run turns red, open it, copy the red error lines, and send them to Claude to fix.

## Project layout

- `app/src/main/java/com/chillo/app/data/Model.kt` - games, moods, storage, picker logic
- `app/src/main/java/com/chillo/app/ui/ChilloMascot.kt` - Chillo, drawn in code
- `app/src/main/java/com/chillo/app/ui/Screens.kt` - Home, Pick and Games screens
- `app/src/main/java/com/chillo/app/ui/Theme.kt` - colours and theme
- `app/src/main/res/` - app icon (adaptive, with a themed version for Android 13+)

## Next (see the spec)

Quests and XP, playtime widget, bedtime scene, death-reason tagging, coach reports, then automatic result detection starting with MLBB.
