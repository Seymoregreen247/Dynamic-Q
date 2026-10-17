# Dynamic Q
By Seymore Green

## Start fresh on GitHub + Netlify
1. Create a new GitHub repository, for example `dynamic-q`.
2. Extract this ZIP on your computer.
3. Open the extracted folder. Upload ALL its contents to the top level of the new repository. Keep the `icons` folder intact. Upload the files, not the ZIP itself.
4. Commit the files.
5. In Netlify, import the new repository as a NEW site. Leave the build command empty and set the publish directory to `.`.
6. Open the live HTTPS Netlify address. Test a QR code and refresh once.
7. Tap Install Dynamic Q when it appears, or use the browser menu's Install option. Install from the live website, not a local file or GitHub source page.

## Required files
- index.html: complete app, including bundled QR generator
- manifest.webmanifest: Dynamic Q name, icon, scope, standalone display
- sw.js: offline app shell and online update handling
- icons/dynamic-q-192.png
- icons/dynamic-q-512.png
- netlify.toml: static publish settings and fresh install-file headers
- README.md: these instructions

## Features
My QR Codes: labeled saved codes, search, pin, full-screen display, copy links, downloads, image import, backup and restore.
Make a QR Code: name and paste a link, then create and save.
NFC tools: write website links to writable NDEF tags, erase contents, cancel, and choose saved links. Requires a compatible NFC-equipped Android phone and Chrome on HTTPS. Physical testing is required.
Client Tools: campaign records, branded QR preview, print builder, pricing, and connection settings.

## Keep your saved codes
A new website address gets separate browser storage. On the old site, export My QR Codes before moving. On the new site, use Backup & existing QR images > Restore Backup. This QR backup does not move campaign/pricing records; export the existing campaign CSV separately for your records. Existing campaign/settings storage keys are retained when using the same site address.

## Tracking and connections
Quick QR codes go directly to the saved website. They do not track scans. Dynamic campaign links require a working redirect service with the campaign registered. Client Tools retains the previous Google Apps Script connection; review it before saving client campaigns. The scan simulation is a demonstration, not real customer scan data. No new backend is provisioned by this package.

## Installation troubleshooting
All files must be on the live site with exactly these names and folder paths. If installation fails, open manifest.webmanifest and both icons through the live website to check that they load. Keep the same live address after installing. Download errors in chat and install errors on the website are separate issues.

## Data
QR pictures and links are stored in IndexedDB in the current browser/device. Export backups regularly. Clearing browser/site data can remove saved codes. Hosting alone does not sync codes across devices.
