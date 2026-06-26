# Lumen — Privacy Policy

**Effective date:** 26 May 2026

## The short version

Lumen is a personal diary app. Your entries, photos, and tags live on your own device. If you choose to enable backup, an encrypted copy is stored in a private folder inside *your own* Google Drive that only Lumen can read. We do not run any servers, we never see your diary, and we do not share, sell, or analyse your content.

## 1. Who we are

Lumen ("the app", "we", "us") is developed and maintained by an independent developer. You can reach us at **jincefrancis63@gmail.com**.

## 2. What information the app handles

### 2.1 Diary content you create

Entries you write — titles, body text, mood selections, tags, and any photos you attach — are stored locally on your device in a SQLite database and a private files folder owned by the app. This content never leaves your device unless you explicitly enable Google Drive backup.

### 2.2 Google account information (only if you enable backup)

If you tap "Connect Google Drive" in Settings, the app uses Google Sign-In to obtain an OAuth access token scoped to `drive.appdata`. Through that process we receive your account email address and a profile identifier so the app can show which account is connected. We do **not** request access to your contacts, calendar, the rest of your Drive, or any other Google data.

### 2.3 Photos and camera

When you attach a photo to an entry, the app reads the image you select from your gallery or captures one with the camera. Photos are copied into the app's private storage and are not uploaded anywhere unless you turn on Drive backup (and even then, only the diary database is uploaded — see Section 4).

### 2.4 Authentication data

If you enable App Lock, the 4-digit PIN you set is one-way hashed (SHA-256, with a per-app salt) before being stored locally. The plain PIN is never written to storage. Biometric prompts are handled by your device's secure subsystem; the app only receives a yes/no result.

### 2.5 What the app does *not* collect

- No analytics or usage tracking SDKs.
- No advertising identifiers.
- No crash reports sent to remote servers.
- No location data.
- No contacts, calendar, or other Google services beyond the appdata Drive scope.

## 3. How we use the information

- **Diary content** — to display, edit, and search your own entries within the app.
- **Google account email** — only to show which account is currently connected to the backup feature and to authenticate API calls to Drive.
- **OAuth tokens** — kept by the Google Sign-In library on your device to refresh access without making you sign in repeatedly. They are not transmitted to us.

We do not use your data for advertising, profiling, training machine-learning models, or any other purpose.

## 4. Google Drive backup — what gets uploaded and where

When you tap "Back up now" the app:

- Serialises your diary entries (text, moods, tags, timestamps) into a single JSON file named `lumen_diary_backup.json`.
- Uploads that file to the **Application Data Folder** of your Google Drive. This is a hidden folder that only the installed copy of Lumen on your authorised devices can read or write. It is not visible in your normal drive.google.com view.
- Replaces any previous backup with the new one.

**Photos are not currently uploaded** — only the diary database is backed up. If you uninstall the app, the photos remain only as long as you keep their copies elsewhere.

The backup is stored within Google's infrastructure under *your* Google account. Their handling of that data is governed by Google's privacy policy: https://policies.google.com/privacy

## 5. Sharing of information

We do not share, sell, rent, or trade any information with third parties. We have no servers and no database. The only data transfer the app performs is between your device and your own Google Drive account, initiated by you.

## 6. Data security

- Local data is stored in the app's private sandbox, which on modern Android is isolated from other apps.
- App Lock (optional) requires a PIN or biometric to open the app.
- The PIN is stored as a SHA-256 hash, not in plain text.
- Drive uploads use HTTPS and are stored within Google's encrypted infrastructure.

No system is perfectly secure. If you suspect your device or Google account has been compromised, please change your Google password and revoke Lumen's access from your Google account settings.

## 7. Your rights and controls

- **Read & edit** — all your entries are visible inside the app at any time.
- **Delete an entry** — open the entry and tap "Delete entry".
- **Delete the backup** — visit https://drive.google.com/drive/u/0/settings → "Manage apps" → find Lumen → "Delete hidden app data". Alternatively, tap "Disconnect" inside Lumen's Settings and the local copy of credentials is forgotten.
- **Delete all local data** — uninstall the app, or use Android's app settings → Storage → Clear data.
- **Revoke Drive access** — visit https://myaccount.google.com/permissions and remove Lumen.
- **Request information** — email us at jincefrancis63@gmail.com with any privacy-related question; we will reply within 30 days.

## 8. Children's privacy

Lumen is not directed at children under 13. We do not knowingly collect data from children. If you believe a child has provided information through the app, please contact us so we can guide you through deletion.

## 9. International users

Lumen runs entirely on your device, so the legal jurisdiction governing your data is wherever your device and Google account reside. If you are in the EU/UK, you have rights under the GDPR/UK GDPR to access, rectify, erase, restrict, or port your personal data — all of which you can perform yourself directly inside the app, since we hold no copy.

## 10. Changes to this policy

If we make material changes, we will update the effective date at the top of this page and, where appropriate, surface a notice inside the app. Continued use of Lumen after a change indicates your acceptance of the revised policy.

## 11. Contact

Questions, requests, or complaints:

**Email:** jincefrancis63@gmail.com
