# Privacy Policy for MapAlarm

**Live page:** [mykhailo-krukovets.github.io/Privacy-Policy-for-MapAlarm](https://mykhailo-krukovets.github.io/Privacy-Policy-for-MapAlarm/)

**Effective date: July 29, 2026**

MapAlarm ("the app", "we", "us") is a location-based alarm clock for Android. This policy explains exactly what the app does with your data, what leaves your device, and how you can stop it.

## Summary

*   There is no MapAlarm account, and we operate no server of our own.
*   Your alarms, saved places, search history and settings never leave your device.
*   Coordinates and search text are sent to Google Maps Platform so the app can show maps, resolve addresses and render place previews.
*   Optional crash reports and anonymous usage statistics are sent to Google Firebase. You can switch this off in **Settings → About → Send anonymous diagnostics**.
*   We do not sell or share your data, we show no advertising, and we do not build a profile of where you go.

## 1. Data the app handles

### 1.1 Location data

*   **Foreground location** shows your current position on the map and lets you place alarm points precisely.
*   **Background location** is the core function: the app keeps checking your position while the screen is off or while you use other apps, so an alarm can fire when you arrive at or leave a place. Tracking runs in a foreground service with a persistent notification, and only while at least one alarm is active or scheduled.
*   Positions are evaluated in memory and are **not** written to any location history. The app stores only the coordinates of the places you choose yourself.

### 1.2 Physical activity

With your permission, the app uses Android Activity Recognition to detect whether you are stationary or moving and to lower the GPS update rate accordingly. This is used purely to save battery and is processed on your device.

### 1.3 Data stored on your device

Stored locally in a Room database and in the app's private preferences:

*   Alarms: coordinates, radius, name, address, trigger type, schedule.
*   Search history: the last 50 places you looked up.
*   A cache of place details, map images and Street View thumbnails, deleted automatically after 30 days.
*   Settings: ringtone, volume, vibration, theme, language, marker colours, radius defaults.

Android backup is disabled for this app (`allowBackup=false`), so none of this is copied into your Google account backup.

## 2. Data that leaves your device

### 2.1 Google Maps Platform (Google LLC)

Required for the app to function. The app sends requests to Google containing:

*   the coordinates you tap, save or move to, for reverse geocoding (`geocode/json`), static map images (`staticmap`) and Street View availability and thumbnails (`streetview`);
*   the text you type in search, plus a nearby location bias, through the Google Places SDK (autocomplete and place details);
*   the map viewport and your position while the interactive map is displayed, through the Google Maps SDK for Android.

Google processes these requests under its own privacy policy, including for service delivery and abuse prevention: [Google Privacy Policy](https://policies.google.com/privacy). See also the [Google Maps Platform Terms of Service](https://cloud.google.com/maps-platform/terms).

### 2.2 Firebase Crashlytics (Google LLC) — optional

If crash reporting is on and the app crashes or hits an error, Crashlytics receives a stack trace, device model, Android version, app version, locale, available memory and storage, a randomly generated installation identifier, and the app's own diagnostic log lines (for example the current GPS polling interval). **Crash reports contain no coordinates, addresses or alarm names.**

### 2.3 Firebase Analytics (Google LLC) — optional

If diagnostics are on, Firebase Analytics reports automatically collected events such as app opens, session length, screen views, app updates and crashes, together with device model, OS version, app version, language and an approximate country derived from your IP address, tied to a pseudonymous app instance identifier. **No precise location, address or search query is sent to Analytics.**

### 2.4 Turning the optional collection off

**Settings → About → Send anonymous diagnostics** disables both Crashlytics and Analytics collection immediately and permanently until you turn it back on. Google Play services and the Maps requests in section 2.1 cannot be disabled without making the app unusable; if you do not want them, please stop using the app.

## 3. What we never do

*   No advertising, no ad identifiers, no ad networks.
*   No selling or sharing of personal data, in the sense of the CCPA/CPRA or otherwise.
*   No user accounts, sign-in, email collection or contact list access.
*   No upload of your alarms, saved places or movement history to us or to anyone else.

## 4. Legal bases (GDPR)

For users in the EEA, the UK and Switzerland:

*   **Performance of a contract** (Art. 6(1)(b)) for location processing and Maps requests: without them the app cannot deliver the alarm function you asked for.
*   **Consent** (Art. 6(1)(a)) for the Android runtime permissions themselves, granted through the system dialogs and revocable at any time in Android settings.
*   **Legitimate interests** (Art. 6(1)(f)) for crash reporting and anonymous usage statistics, namely keeping the app stable. You can object at any time using the diagnostics switch described in section 2.4, with no loss of functionality.

The developer of MapAlarm is the controller for the processing described here. Google LLC acts as our processor for Firebase and as an independent controller for Google Maps Platform.

## 5. International transfers

Firebase and Google Maps Platform process data on Google infrastructure that may be located outside your country, including in the United States. Google relies on the European Commission's Standard Contractual Clauses and on the EU–US Data Privacy Framework for those transfers.

## 6. Retention and deletion

*   Cached place details, map images and Street View thumbnails: deleted automatically 30 days after they were stored.
*   Search history: capped at the 50 most recent entries; older entries are dropped. Individual entries can be removed from the search panel.
*   Alarms and settings: kept until you delete them in the app.
*   **To erase everything at once:** Android Settings → Apps → MapAlarm → Storage → Clear storage, or simply uninstall the app. Because all of this data lives only on your device, uninstalling deletes it irreversibly.
*   Crashlytics reports are retained by Google for up to 90 days; Analytics data is retained for 2 months (the shortest period Google offers) and is then deleted. Switching diagnostics off stops any further collection.

## 7. Your rights

Depending on where you live you may have the right to access, correct, delete, restrict or object to the processing of your personal data, and to receive it in a portable form. Since alarms, places, search history and settings are stored only on your device, you can exercise all of these directly in the app and in Android settings without contacting us.

For the pseudonymous diagnostics data held by Google on our behalf, contact us (section 10) and we will act on your request. EEA and UK users also have the right to lodge a complaint with their national data protection authority. California residents have the right to know, delete and correct their personal information and to non-discrimination; we do not sell or share personal information and have not done so in the preceding 12 months.

## 8. Children

MapAlarm is not directed to children. We do not knowingly collect personal data from children under 13 (or under 16 in the EEA). The app has no social features, no user-generated content visible to others and no advertising. If you believe a child has provided data through the optional diagnostics, contact us and we will have it deleted.

## 9. Permissions

Requested with a system dialog:

*   `ACCESS_FINE_LOCATION` / `ACCESS_COARSE_LOCATION` — locating you and evaluating alarm zones.
*   `ACCESS_BACKGROUND_LOCATION` — triggering alarms while the app is not in the foreground.
*   `POST_NOTIFICATIONS` — alarm alerts, the tracking notification and status messages.
*   `ACTIVITY_RECOGNITION` — battery-saving detection of whether you are moving.
*   `SCHEDULE_EXACT_ALARM` / `USE_EXACT_ALARM` — starting and stopping tracking at scheduled times.
*   `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` — asking to be exempted from battery restrictions so tracking is not killed.

Granted automatically because they carry no privacy risk:

*   `FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_LOCATION`, `FOREGROUND_SERVICE_SHORT_SERVICE` — running the tracking service visibly.
*   `INTERNET`, `ACCESS_NETWORK_STATE` — map tiles and Google requests.
*   `ACCESS_WIFI_STATE`, `CHANGE_WIFI_STATE` — letting Android improve location accuracy from Wi-Fi scans; the app never reads your network list.
*   `WAKE_LOCK`, `VIBRATE`, `MODIFY_AUDIO_SETTINGS`, `USE_FULL_SCREEN_INTENT` — waking the screen and playing the alarm reliably.
*   `RECEIVE_BOOT_COMPLETED` — restoring active alarms after a reboot.

Location and notification permissions can be revoked at any time in Android settings. Revoking location disables the alarm function entirely.

## 10. Security

All personal data stays in the app's private storage, protected by Android's application sandbox and by your device lock screen. Network traffic uses HTTPS only; cleartext traffic is disabled at the platform level. Release builds are code-shrunk and obfuscated. No system is perfectly secure, but the app holds no server-side copy of your data that could be breached.

## 11. Changes to this policy

We may update this policy when the app changes. The effective date above marks the current version, and the latest text is always available inside the app under **Settings → About → Privacy Policy**. Material changes will be announced in the release notes.

## 12. Contact

Questions, requests or privacy complaints: use the **Developer contact** section on the MapAlarm listing in Google Play, or the "Send feedback about this app" link on that page. We respond within 30 days.
