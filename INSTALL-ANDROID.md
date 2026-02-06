# Install as Android App

Your expense tracker is now a **Progressive Web App (PWA)** that can be installed on Android like a native app!

## Step 1: Generate Icons

1. Open `generate-icons.html` in your browser
2. Click both download buttons to get `icon-192.png` and `icon-512.png`
3. Save both icon files in the same folder as `expense-tracker.html`

## Step 2: Host the Files

You need to serve the files over HTTP (file:// won't work for PWAs). Choose one option:

### Option A: Using Python (simplest)
```bash
# Navigate to the folder containing your files
cd C:\Users\Verni

# Python 3:
python -m http.server 8000

# Python 2:
python -m SimpleHTTPServer 8000
```

### Option B: Using Node.js
```bash
npx http-server -p 8000
```

### Option C: Upload to a web host
Upload all files to any web hosting service (GitHub Pages, Netlify, Vercel, etc.)

## Step 3: Install on Android

### For local testing (same WiFi network):
1. Find your computer's IP address (e.g., `192.168.1.100`)
2. On your Android phone, open Chrome
3. Visit `http://192.168.1.100:8000/expense-tracker.html`
4. Tap the menu (⋮) → **"Add to Home screen"** or **"Install app"**
5. Tap "Install"

### For production (recommended):
1. Upload files to a web host with HTTPS
2. Visit the URL on your Android phone
3. Tap the menu (⋮) → **"Add to Home screen"** or **"Install app"**
4. Tap "Install"

## Step 4: Use the App

- The app installs with a home screen icon
- Opens in full-screen (no browser UI)
- Works offline after first load
- All data saved in the app (localStorage)

## Files You Need:

```
C:\Users\Verni\
├── expense-tracker.html  (main app)
├── manifest.json         (app metadata)
├── service-worker.js     (offline support)
├── icon-192.png          (small icon - generate this)
└── icon-512.png          (large icon - generate this)
```

## Troubleshooting

**"Add to Home screen" not showing?**
- Make sure you're using HTTPS or localhost
- Icons must be present
- Try reloading the page

**App not working offline?**
- Visit the page once while online
- Check browser console for service worker errors

**Need to update the app?**
- Change `CACHE_NAME` in `service-worker.js` to force update
- Uninstall and reinstall from browser

---

## Alternative: Build a Real APK

If you need a true APK file (for Play Store or sideloading), you can use:

1. **PWA Builder** - https://www.pwabuilder.com/
   - Upload your hosted app URL
   - Download Android APK
   - No coding required

2. **Capacitor** (more advanced)
   ```bash
   npm install @capacitor/core @capacitor/cli
   npx cap init
   npx cap add android
   npx cap open android
   ```

For your 2-week trip, the PWA install is fastest and works great!
