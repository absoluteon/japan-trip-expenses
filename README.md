# Japan Trip Expense Tracker

A Progressive Web App (PWA) for tracking and splitting expenses during travel. Built for a 2-week trip to Japan with two people sharing costs.

## Features

- **Flexible Expense Splitting**: Split costs by percentage or fixed JPY amounts
- **Multiple Payment Methods**: Track Cash, Credit Card, and Suica payments for each person
- **Daily Settlement**: Automatic calculation of who owes whom each day
- **Offline Support**: Works completely offline after installation (PWA)
- **Data Persistence**: All data saved locally in browser
- **Excel/CSV Export**: Export all expenses and settlements
- **Customizable Categories**: Pre-defined categories plus ability to add custom ones
- **Android Installation**: Install as a native-like app on Android devices

## Quick Start

### Option 1: Use GitHub Pages (Recommended for Trip)

Visit the hosted version at: `https://[your-username].github.io/japan-trip-expenses/expense-tracker.html`

### Option 2: Run Locally

1. Clone this repository
2. Serve the files using any HTTP server:
   ```bash
   python -m http.server 8000
   ```
3. Open `http://localhost:8000/expense-tracker.html` in your browser

## Installation as Android App

See [INSTALL-ANDROID.md](INSTALL-ANDROID.md) for detailed instructions on installing this app on your Android phone.

### Quick Install Steps:
1. Visit the hosted URL on your Android phone (Chrome)
2. Tap menu (⋮) → "Add to Home screen" or "Install app"
3. The app will work offline after first load

## Files

- `expense-tracker.html` - Main application (single-file app)
- `manifest.json` - PWA manifest for app installation
- `service-worker.js` - Enables offline functionality
- `icon-192.png` & `icon-512.png` - App icons
- `generate-icons.html` - Tool to regenerate app icons if needed
- `INSTALL-ANDROID.md` - Detailed installation guide

## Usage

1. **Set Names**: Click settings (⚙️) to customize person names
2. **Add Expenses**: Click + button to add new expense
3. **Split Costs**: Toggle between % and JPY split modes
4. **Settle Daily**: Click "Settle JPY X" button to mark daily settlement
5. **Export Data**: Use "Export to Excel" to backup your data

## Technical Details

- **No server required**: 100% client-side application
- **Data storage**: localStorage (survives browser restarts)
- **Offline capable**: Service worker caches all resources
- **Excel export**: Uses SheetJS (xlsx) library with CSV fallback

## Browser Support

- Chrome/Edge (recommended)
- Firefox
- Safari (iOS 11.3+)

Best experience on mobile devices.

## License

Free to use for personal travel expense tracking.
