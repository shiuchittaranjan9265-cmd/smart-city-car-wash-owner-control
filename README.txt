SMART CITY CAR WASH — UPDATED WEB APP PACKAGE

Files:
- index.html: Existing car wash management app plus Staff Management, daily attendance,
  staff salary/tiffin/expense entry, tomorrow schedule WhatsApp prompt, and advance-payment
  WhatsApp message option.
- owner-admin.html: Existing Owner Panel for app_users license records.

IMPORTANT:
1. This is a web app package, not a rebuilt Android APK. The APK has not been modified.
2. Export a fresh backup before replacing any live app files. Keep your existing backup too.
3. Existing customer/month/payment records remain under localStorage key SCW_V5. Staff, attendance,
   and staff expense records are added to that same backup data object.
4. Data remains local to the browser/device unless a separate sync solution is configured.
5. WhatsApp messages open in WhatsApp for review and manual sending; this package does not send
   messages automatically in the background.
6. The Owner Panel manages license records only; it does not create Firebase Auth users.
7. Firebase Rules must be configured securely; do not publish permissive rules.

TEST BEFORE LIVE USE:
- Login and license status
- Customer records, month switch, wash count and payment history
- Export and import backup
- Add/edit/deactivate staff
- Attendance date/status and staff expense entry
- WhatsApp schedule / payment message text and recipient number
- Owner Panel license actions

GitHub Pages:
Keep index.html and owner-admin.html in repository root. Back up the currently deployed files
before replacing them.
