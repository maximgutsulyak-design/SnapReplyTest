# Firebase Configuration Setup

## Current Status
Firebase credentials are currently set to placeholder values in `js/firebase.js`. This prevents cloud synchronization features from working.

## How to Add Your Firebase Credentials

1. Go to [Firebase Console](https://console.firebase.google.com)
2. Select your project (or create a new one)
3. Click **Project Settings** (gear icon in top-left)
4. Go to **Your apps** section and select your web app
5. Copy the configuration object with these fields:
   - `apiKey`
   - `authDomain`
   - `projectId`
   - `storageBucket`
   - `messagingSenderId`
   - `appId`

## Configuration Location
Update the credentials in `js/firebase.js` at line 50-55:

```javascript
const config = {
  apiKey: 'YOUR_API_KEY',           // Replace with real value
  authDomain: 'YOUR_AUTH_DOMAIN',   // Replace with real value
  projectId: 'YOUR_PROJECT_ID',     // Replace with real value
  storageBucket: 'YOUR_STORAGE_BUCKET',
  messagingSenderId: 'YOUR_MESSAGING_SENDER_ID',
  appId: 'YOUR_APP_ID'
};
```

## What Works Without Firebase
- All local template management (create, edit, delete, search)
- CSV/XLSX import and export
- Local storage persistence
- Category management
- Grid display modes

## What Requires Firebase
- Cloud synchronization of templates
- Google sign-in authentication
- Cross-device template sync

## After Adding Credentials
1. Save the changes in `js/firebase.js`
2. Refresh the browser (Ctrl+F5 for hard refresh)
3. Click the login button to authenticate with Google
4. Templates will sync automatically
