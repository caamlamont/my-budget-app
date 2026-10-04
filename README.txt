# My Budget Tracker — Backup Edition

This version keeps the existing dark-mode budget tracker workflow and adds a layered backup system.

## Automatic backup
Every data change updates:
1. The normal app storage.
2. An automatic JSON snapshot.
3. An IndexedDB backup snapshot.

The app keeps several recent automatic snapshots on the device. On startup it attempts to recover from the automatic backup if the primary storage is missing.

## Backup file
Use **Save backup file** to create a JSON backup. On iPhone, Safari will let you save/share the file through the Files app, including iCloud Drive if desired.

Use **Restore backup** to select that JSON file later.

## Important limitation
A browser/PWA cannot silently write arbitrary files into iCloud Drive in the background. The automatic backup is therefore an automatic on-device backup. Saving the JSON backup file to Files/iCloud is the extra off-device protection step.

## Excel
The Export all expenses button creates an Excel-compatible CSV containing all months and expenses.

## GitHub Pages
Upload all files to the root of your GitHub repository and publish with GitHub Pages from the `main` branch and `/ (root)`.
