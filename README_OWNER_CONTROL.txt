SMART CITY CAR WASH — OWNER CONTROL STARTER

Included:
- index.html: your original car-wash dashboard, unchanged.
- owner-admin.html: separate Firebase email/password owner control panel.
- firestore.rules.template: starter rules that restrict app_users to one owner UID.

IMPORTANT LIMITATIONS
1) This is a starter control panel. The existing index.html stores car/customer data in localStorage and does NOT yet check app_users.appEnabled. Therefore switching a user off in this panel will not remotely disable their existing copy of the old app. To enforce paid access, the main app must be changed to authenticate each business and read its license status before showing data; customer data should be stored per authenticated user in Firestore.
2) Do not publish the rules template until you replace REPLACE_WITH_OWNER_AUTH_UID with your own Firebase Authentication UID. The document ID "admin" is not a secure substitute for your UID.
3) Firebase Console > Authentication: enable Email/Password and create the owner account. The owner account must use the exact UID inserted into the rules.
4) Firebase Console > Project settings > General > Your apps > SmartCityCarWashWeb > SDK config: copy the config values into owner-admin.html, replacing PASTE_API_KEY, PASTE_AUTH_DOMAIN, PASTE_PROJECT_ID, PASTE_STORAGE_BUCKET, PASTE_MESSAGING_SENDER_ID, PASTE_APP_ID. Firebase web apiKey is client configuration, not a service-account secret; never place service-account private keys in HTML.
5) In Firestore Rules, replace the existing rules only after reviewing your current app's data needs. The template closes every other collection, which is secure by default but could break existing cloud features if you already use them.
6) Open owner-admin.html through a web server/hosting (not a file:// URL), for example Firebase Hosting, after config and rules are set.
7) Add each user in Firebase Authentication first; then create/update their app_users document with document ID equal to their Authentication UID. Set appEnabled and subscriptionStatus in the panel.

The admin panel can manage records only when authenticated and the published Firestore rules authorize the owner's UID. It does not bypass Firebase security rules.
