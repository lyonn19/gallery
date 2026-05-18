# Firebase Setup Instructions for Liam Gallery

## Prerequisites
- Free Firebase account (google.com/firebase)
- Liam Gallery project created

## Quick Setup

1. **Create Firestore Database**
   - Go to Firebase Console
   - Click "Firestore Database"
   - Click "Create Database"
   - Select "Start in test mode"
   - Choose region (us-central recommended)
   - Click "Create"

2. **Get Your Firebase Config**
   - Go to Project Settings (gear icon)
   - Copy the config object under "Your apps" section
   - You'll see something like:
   ```
   const firebaseConfig = {
     apiKey: "AIzaSy...",
     authDomain: "liam-gallery.firebaseapp.com",
     projectId: "liam-gallery",
     storageBucket: "liam-gallery.appspot.com",
     messagingSenderId: "123...",
     appId: "1:123..."
   };
   ```

3. **Update index.html**
   - Open the updated index.html in a text editor
   - Find this line: `const firebaseConfig = { /* PASTE YOUR CONFIG HERE */ };`
   - Replace the entire config object with YOUR Firebase config from Step 2
   - Save the file

4. **Deploy to Netlify**
   - Go to app.netlify.com/drop
   - Drag the gallery folder
   - Your gallery now syncs across all devices!

## How It Works

- **First device:** Upload/draw → Saved to Firebase Cloud ☁️
- **Second device:** Opens gallery → Automatically loads your drawings ✅
- **Real-time sync:** Changes appear instantly on all devices

## Testing

1. Open gallery on Device A (phone)
2. Upload a drawing
3. Open gallery on Device B (different phone/computer)
4. Your drawing appears automatically! 🎉

## Troubleshooting

**"Permission denied" error:**
- Make sure Firestore Database is created
- You selected "test mode" (not production)

**Drawings not syncing:**
- Check internet connection on both devices
- Clear browser cache
- Check browser console (F12) for errors

**Need help?**
- Check Firebase Firestore Rules are in test mode
- Verify API credentials are correct
- Make sure both devices use same browser (or clear cache)

## Security (After Testing)

Once you're happy with it, update Firestore Rules for security:
```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /galleries/{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```

This prevents others from accessing your gallery data.
