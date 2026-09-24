NASA Space Apps Cairo - Materials PWA
=========================================

This PWA is already connected to:
https://script.google.com/macros/s/AKfycbwa3WPXybwpIkAzfSLsdrH5f4BpeUjX9SK1FpC9qPoDgb6LhHP6eZP-VRuvwZ8pL5s/exec

FILES
-----
index.html
manifest.json
service-worker.js
icon-192.png
icon-512.png

IMPORTANT - APPS SCRIPT
-----------------------
Your Apps Script doGet() must allow embedding inside the PWA.

Use:

function doGet() {
  return HtmlService
    .createHtmlOutputFromFile('Index')
    .setTitle('NASA Space Apps Cairo - Materials')
    .setXFrameOptionsMode(HtmlService.XFrameOptionsMode.ALLOWALL);
}

Then:
Deploy > Manage deployments > Edit > New version > Deploy

HOST ON GITHUB PAGES
--------------------
1. Create a new GitHub repository, for example:
   nasa-materials-pwa

2. Upload all 5 files in this folder to the repository root.

3. Open:
   Settings > Pages

4. Under Build and deployment choose:
   Deploy from a branch

5. Select:
   Branch: main
   Folder: /(root)

6. Save.

Your PWA URL will look like:
https://YOUR-USERNAME.github.io/nasa-materials-pwa/

ANDROID INSTALL
---------------
Open the GitHub Pages URL in Chrome.
Use:
Menu (⋮) > Install app
or
Add to Home screen

IPHONE / IPAD
-------------
Open the GitHub Pages URL in Safari.
Tap Share > Add to Home Screen.

NOTES
-----
- The PWA shell can be installed.
- The actual NASA Materials system still needs internet because it uses
  Google Apps Script, Google Sheets and Google Drive.
- If the embedded app is blank, confirm the doGet() ALLOWALL line above
  and redeploy Apps Script.
