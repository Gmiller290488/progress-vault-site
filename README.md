# Progress Vault website

A plain static site (HTML + CSS, no build step). It has three pages: `index.html` (landing), `privacy.html` (privacy policy) and `support.html` (FAQ and contact).

## Preview locally
```bash
python3 -m http.server 8765
```
Then open http://localhost:8765.

## Before publishing
Search for `data-todo` and `TODO` to find these:
- **App Store link:** the two "Download on the App Store" buttons in `index.html` point to `#`. Also swap the buttons for Apple's official badge (from Apple's [marketing resources](https://developer.apple.com/app-store/marketing/guidelines/)).
- **Privacy policy:** it was written from how the app actually works (on-device storage, no analytics, AdMob with UMP consent, StoreKit, Face ID, a keychain counter for free overlay uses). Read it before publishing, and update it whenever the app's data handling changes.

## Keeping it accurate
The landing page describes features from the custom-camera work (the alignment overlay, self-timer, and Premium unlocking the overlay). Don't publish until those features are released, or adjust the copy first.

## Images
- `images/screen-*.jpg`: simulator screenshots with sample data (`-SeedSamplePhotos`) and a clean status bar (`xcrun simctl status_bar booted override --time 9:41 ...`).
- `images/overlay-*.jpg`: two sample photos used by the animated overlay illustration.
- `images/app-icon.png`, `images/favicon.png`: from the app icon.
