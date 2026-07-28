# Privacy Policy

**TechFlow — Field Service Management**  
**Effective date:** 28 July 2026  
**Last reviewed:** 28 July 2026

---

## 1. Introduction

TechFlow ("the Application", "we", "us") is a field-service management application designed for mobile technicians and small service businesses. It is published by **Chill Tech Services** and is available on Android and iOS.

TechFlow is built on a **privacy-first, offline-first** architecture. The Application has no server backend, no user accounts, no cloud synchronisation, no analytics, no advertising, and no telemetry of any kind. All business data is stored exclusively on your device.

This Privacy Policy explains what data TechFlow stores, where that data resides, which device permissions the Application requests, how user-initiated backups are handled, and what rights you have over your information.

---

## 2. Data Stored by the Application

TechFlow stores the following categories of data locally on your device:

### 2.1 Business records

| Category | Examples |
|---|---|
| Clients | Name, address, phone number, email address, notes |
| Interventions / Jobs | Description, date, linked client, labour hours, status |
| Invoices | Line items, amounts, VAT, payment status |
| Payments | Amount received, date, method, linked invoice |
| Quotations | Items, pricing, linked client, status |
| Inventory | Item names, quantities, unit prices |

### 2.2 Application settings

- Company profile (name, address, VAT number, logo)
- Invoice and quotation numbering preferences
- Currency and VAT rate preferences
- Notification preferences
- Display and theme preferences

### 2.3 Data the Application does not collect

TechFlow does **not** collect, transmit, or process any of the following:

- Device identifiers (IMEI, advertising ID, etc.)
- Location data
- Browsing history
- Crash reports or diagnostics sent to a remote server
- Usage analytics or behavioural data
- Any data from third-party advertising networks

---

## 3. Where Data Is Stored

All data entered into TechFlow is stored exclusively in the **local storage of your device** using the React Native AsyncStorage system. This data:

- Never leaves your device unless you explicitly initiate a backup export (see Section 5)
- Is not accessible to Chill Tech Services or any third party
- Is not synchronised to any cloud service by the Application

The data is stored in the Application's private sandbox on your device, in accordance with the security model enforced by Android and iOS. Other applications cannot access TechFlow's stored data.

---

## 4. Device Permissions

TechFlow may request the following device permissions. All permissions are optional unless explicitly stated; the core functionality of the Application operates without any of them.

### 4.1 Contacts (optional)

**Permission:** `READ_CONTACTS` (Android) / Contacts access (iOS)

**Purpose:** To allow you to import a client's name and phone number directly from your device's address book when creating a new client record. Contact data imported this way is stored locally as part of the client record; no contact data is transmitted externally.

**When requested:** Only when you tap "Import from contacts". You may decline and enter client details manually.

### 4.2 Calendar (optional)

**Permission:** `READ_CALENDAR`, `WRITE_CALENDAR` (Android) / Calendar access (iOS)

**Purpose:** To allow you to add a job or intervention as an event in your device's calendar application. Calendar events are created directly on your device via the system calendar API; no calendar data is transmitted externally.

**When requested:** Only when you tap "Add to calendar" on a job or intervention. You may decline.

### 4.3 Notifications (optional)

**Permission:** `POST_NOTIFICATIONS` (Android 13+) / Notification authorisation (iOS)

**Purpose:** To deliver local, on-device reminders about upcoming interventions or unpaid work. Notifications are scheduled and delivered entirely on your device; no notification content is transmitted to any server.

**When requested:** When you enable notification reminders in Settings. You may decline; no functionality is lost except reminder alerts.

### 4.4 Storage / File access (implicit)

**Purpose:** To read and write the backup files that you choose to export or import. File access is limited to the files you explicitly select via the system file picker. TechFlow does not perform background file scans.

---

## 5. Backups and Exported Files

TechFlow includes a Backup & Restore feature. All backup operations are **entirely user-initiated**:

- **Creating a backup:** You may export a complete backup of your data as a file (JSON format) by navigating to Settings → Backup & Restore → Create Backup. The file is saved to a location of your choosing on your device or a connected storage service (such as Google Drive or iCloud), using the system share sheet.
- **Restoring a backup:** You may import a previously exported backup file at any time.
- **Integrity:** Backup files are protected by a SHA-256 integrity checksum. The Application will refuse to restore a file whose checksum does not match, alerting you to potential corruption or tampering.
- **Encryption:** Current backup files are **not encrypted**. The content of a backup file is readable by anyone who obtains the file. You are responsible for storing backup files securely (for example, in a password-protected folder or a cloud storage service with access controls).
- **Transmission:** Backup files are not transmitted to Chill Tech Services or any server. Where you choose to store the file (e.g. Google Drive, email) is governed by the privacy policy of that service, not by this Privacy Policy.

---

## 6. Third-Party Services

TechFlow does not integrate with any third-party analytics, advertising, or data-processing services.

The Application may open third-party applications installed on your device (such as WhatsApp or your default calendar application) when you explicitly trigger the corresponding action. These interactions are governed by the privacy policies of those applications. TechFlow does not share data with those applications beyond what you explicitly initiate.

PDF generation and Excel import/export are processed entirely on-device using open-source libraries. No documents leave your device unless you share them yourself via the system share sheet.

---

## 7. Data Retention and Deletion

All data stored by TechFlow remains on your device for as long as the Application is installed. You may delete any individual record (client, invoice, intervention, etc.) directly within the Application at any time.

To delete all data stored by TechFlow, uninstall the Application. On Android, you may also clear all Application data via Settings → Apps → TechFlow → Storage → Clear Data.

**Warning:** Uninstalling the Application or clearing its data permanently removes all records and settings. This action cannot be undone. We strongly recommend creating a backup before performing any of these actions.

---

## 8. Children's Privacy

TechFlow is a professional business management tool intended for use by adults. The Application is not directed at children under the age of 16. We do not knowingly collect personal information from children. If you believe a child has entered personal data into the Application, you may delete it directly within the Application or by uninstalling it.

---

## 9. Your Rights

Depending on your country of residence, you may have rights under applicable data protection law (including, where applicable, the European General Data Protection Regulation — GDPR):

| Right | How to exercise it |
|---|---|
| **Access** | All your data is visible directly within the Application. |
| **Rectification** | Edit any record directly within the Application. |
| **Erasure** | Delete individual records within the Application, or uninstall the Application to remove all data. |
| **Portability** | Use the Backup & Restore feature to export a complete copy of your data in JSON format at any time. |
| **Objection / Restriction** | Because TechFlow does not transmit or process your data externally, there is no remote processing to restrict or object to. |

Because all data is stored locally on your device and is not accessible to Chill Tech Services, we are not able to remotely access, modify, or delete your data on your behalf. All data operations must be performed within the Application on your device.

---

## 10. Security

TechFlow takes the following measures to protect your data:

- **Local isolation:** Data is stored in the Application's private sandbox, inaccessible to other applications.
- **Backup integrity:** Exported backups include a SHA-256 checksum to detect corruption or tampering.
- **No remote attack surface:** Because the Application has no server backend and no network communication, your data is not exposed to remote breaches or server-side vulnerabilities.
- **Secure ID generation:** All records use cryptographically generated unique identifiers (via the device's secure random API) to prevent record collisions.

You are responsible for the physical security of your device and for the secure storage of any backup files you export.

---

## 11. Changes to This Privacy Policy

We may update this Privacy Policy from time to time. When we do, we will revise the "Last reviewed" date at the top of this document and release a new version of the Application with the updated policy. We encourage you to review this policy periodically.

Your continued use of the Application after an updated Privacy Policy has been published constitutes your acceptance of the changes.

---

## 12. Contact

If you have any questions about this Privacy Policy, please contact us:

**Chill Tech Services**  
Email: [techflowlb@outlook.com](mailto:techflowlb@outlook.com)  
Website: [https://3nai-pro.github.io/techflow-legal/](https://3nai-pro.github.io/techflow-legal/)

---

*TechFlow · Your business assistant. Always in flow.*
