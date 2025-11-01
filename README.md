Ballu - Android keyword-based notification & SMS blocker (skeleton)

What this archive contains:
- Minimal Android Studio project (Kotlin) with core features:
  * Add/remove keywords
  * NotificationListenerService that cancels notifications containing keywords
  * BroadcastReceiver for SMS that logs matches and attempts abortBroadcast()
  * Local log/history stored in SharedPreferences (viewable in app)
  * Simple modern UI with RecyclerView for keyword chips and history

Important notes:
- Grant Notification Access: Go to Settings -> Notification Access -> enable Ballu so the app can cancel/hide app notifications.
- SMS behavior: On modern Android versions, to fully prevent SMS delivery/storage you must set Ballu as the default SMS app. This project only demonstrates detection and logging; abortBroadcast() may not prevent storage on newer devices.
- Play Store policies: Access to SMS and notification listener requires strong justification for publishing.

How to open:
1. Open Android Studio -> Open an existing project -> select the folder extracted from this ZIP (module app included).
2. Build & run on a device (emulator may not deliver SMS).

Next improvements you can ask me to add:
- Full default SMS app flow (UI to become default SMS app) and sending/reading messages.
- Per-app whitelist/blacklist toggle.
- Better Material 3 styling, animations, icons, and dark mode polish.
- Export/import keywords and logs.
