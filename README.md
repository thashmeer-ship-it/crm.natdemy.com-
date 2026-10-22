# NATDEMY CRM Live — Android Studio project

This is a starter Android WebView wrapper for the existing CRM at https://crm.natdemy.com/.

## What it does
- Opens the existing CRM inside an Android app shell.
- Uses the CRM website's own login and permissions.
- Shows server-side changes whenever the CRM page/data refreshes.
- Does not copy CRM data into a separate database.

## Important limitations
- This is not a compiled APK. Build it in Android Studio to generate the APK.
- Real-time push notifications, background change monitoring, and native Dashboard/Admissions/Staff Reports screens are not implemented. Those require documented CRM APIs/webhooks and permission-approved backend integration.
- If the CRM blocks WebView, requires external SSO, or is not mobile responsive, the app may need changes.
- Test with an authorized test account before staff rollout.

## Build APK
1. Install Android Studio and a compatible JDK (JDK 17 recommended).
2. Open this folder as an Android Studio project.
3. Allow Gradle sync and install Android SDK Platform 35 if prompted.
4. Select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. The debug APK will be in `app/build/outputs/apk/debug/app-debug.apk`.

## Production hardening before distribution
- Confirm the CRM owner approves the app integration.
- Test login, logout, session expiry, password reset, downloads/uploads, and external links.
- Configure a production signing key securely.
- For true push alerts, request API/webhook documentation and implement a secured backend plus Firebase Cloud Messaging.
