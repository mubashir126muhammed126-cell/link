LINKORAX — EMAIL AUTHENTICATION SETUP

Admin email:
  monumuhammed92@gmail.com

IMPORTANT:
- The password is intentionally NOT included in this website file.
- The website will not sign in until Firebase is configured.
- Do not paste your password into HTML or JavaScript.

SETUP:
1. Open https://console.firebase.google.com/ and create a Firebase project.
2. In Project settings > General, add a Web app and copy its Firebase config.
3. In Authentication > Sign-in method, enable Email/Password.
4. In Authentication > Users, create the admin user using the email above and set a strong password. If you already shared a real password in chat, change it before using it.
5. Open linkorax_email_auth.html in a text editor. Find FIREBASE_CONFIG and replace:
   - PASTE_FIREBASE_API_KEY with apiKey
   - PASTE_PROJECT_ID with projectId and use the same project ID in authDomain
   - PASTE_FIREBASE_APP_ID with appId
   Add storageBucket and messagingSenderId too if supplied by Firebase (they are not required by this basic auth snippet).
6. Host the page on HTTPS (for example, Netlify or Firebase Hosting). Add your deployed domain under Firebase Authentication > Settings > Authorized domains.
7. Test sign-in and the password-reset email.

FEATURES:
- Firebase Email/Password sign-in
- Only the configured admin email is accepted by this page
- Forgot-password email via Firebase Authentication
- Sign-out

LIMITATIONS:
- This only authenticates the admin UI. Portfolio data still uses browser localStorage and is not shared across devices.
- For production, protect database/media with server-side authorization and Firebase Security Rules. Do not rely on client-side email checks to protect sensitive data.
- The Firebase web config identifies your project; it is not a secret. Never include passwords or service-account private keys in the page.
