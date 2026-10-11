# Privacy Policy for Aéris Carnet

**Last updated:** October 11, 2026

Aéris Carnet ("we", "our", or "the app") is committed to protecting your privacy. This Privacy Policy outlines how your information is handled when using our Android application.

> **Current version (1.2.0 and later free builds):** in-app purchases and the real-time flight lookup / sync features are not available. The sections below that describe them apply only if those features are offered in a future version, and this policy will be updated before that happens.

## 1. Offline-First Architecture & Data Ownership
Aéris Carnet is engineered as an **offline-first, client-side personal flight logbook**.
- All your personal flight records, ticket information, notes, and passport stamps are stored **locally on your device** in a private SQLite/Room database.
- We do not operate external application servers, databases, or user accounts. We do not sell or monetize your flight history. When you voluntarily use the real-time flight lookup feature, only the queried flight designator and date are sent to the aviation schedule API; your stored logbook history is never uploaded or transmitted.

## 2. Permissions Used by the App
- **CAMERA (`android.permission.CAMERA`)**: Used exclusively on-device when you choose to scan a boarding pass via Google ML Kit Barcode Scanning. The photo you take is processed on your device; a copy is kept only if you attach it to a flight as a ticket photo. Nothing is transmitted to any server.
- **INTERNET (`android.permission.INTERNET`)**: Used only for:
  1. Retrieving live flight schedule details (via public aviation APIs) when you search a flight designator (not available in the current version).
  2. Downloading airline brand logos and aircraft silhouettes for offline caching.
  3. Google Play Billing purchase verification and status reconciliation (not used in the current version).
- **BILLING (`com.android.vending.BILLING`)**: Declared for Google Play's official billing system. The current version sells nothing and does not start a purchase.

## 3. In-App Purchases & Subscriptions
All transactions are handled directly and securely by Google Play. We do not collect, process, or store your credit card numbers, billing addresses, or payment credentials. Your entitlement status is verified on-device via Google Play Billing Client and secured in encrypted local storage (`EncryptedSharedPreferences`).

## 4. Backups and Data Transfer
If you have Android Auto-Backup or Google One cloud backup enabled on your device:
- Your local flight logs may be backed up to your personal private Google Drive account under Android's standard app data backup policy.
- Pro entitlement credentials and device Keystore keys are strictly excluded from backups (`data_extraction_rules.xml`) to safeguard security and license integrity.

## 5. Third-Party Services & Network Requests
The app interacts with the following external third-party services strictly when online features are triggered:
- **Google Play Services**: For In-App Billing processing, ML Kit Document Scanning, and Barcode Parsing.
- **AviationStack (Optional Search)**: When you manually search a flight number/date, the query parameters are sent to AviationStack's public aviation API to fetch schedule details.
- **Public Airline & Aircraft Image CDNs**: Public airline logos and aircraft manufacturer emblems are retrieved on-demand from public content delivery networks (`pics.avs.io`, `images.kiwi.com`, and `upload.wikimedia.org`) for local caching. These requests only transmit standard HTTP headers and your IP address to retrieve image assets.

## 6. Children's Privacy
Aéris Carnet does not knowingly collect or solicit personal information from children under the age of 13.

## 7. Data Retention and Deletion
Aéris Carnet puts you in complete control of your data:
- **Instant In-App Deletion**: You can permanently delete any individual flight record, scanned barcode, or ticket photo at any time directly within the app (tap on any flight card or ticket detail and select Delete).
- **Complete Local Purge**: Because all personal data is stored strictly on your local device in private application sandboxes, clearing the application data/storage via your Android system settings (`Settings -> Apps -> Aéris Carnet -> Storage -> Clear Data`) or uninstalling the app permanently and irreversibly purges 100% of your flight logs, ticket images, and cached assets.
- **Cloud Backup Deletion**: If you have enabled Android Auto-Backup or Google One cloud backup, you can delete your stored app backup at any time through your Google Drive app backup management settings.

## 8. Changes to This Privacy Policy
We may update our Privacy Policy from time to time. Any changes will be posted within this document at https://github.com/kijonggong/aeris-carnet-legal.

## 9. Contact Us
If you have questions, feedback, or concerns regarding our Privacy Policy or data handling practices, please contact us at:
- **Developer Email**: `kijong1002@gmail.com`
- **GitHub Issues**: https://github.com/kijonggong/aeris-carnet-legal/issues
