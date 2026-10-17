# SmartSwingScanner Android APK builder

This is a native Android starter app for manual-only scanning. It has Dashboard (top 10 candidates at ₹100 or below), Intraday, and BTST tabs. It has no broker API and does not place orders.

## Build the APK in GitHub Actions (no Android Studio required)
1. Sign in to GitHub and create a **private** repository named `SmartSwingScanner-Android`.
2. Upload all files and folders from this ZIP to the repository. Keep the `.github/workflows/build-apk.yml` path intact.
3. Open the repository's **Actions** tab.
4. Select **Build SmartSwingScanner APK** and press **Run workflow**.
5. When the run finishes successfully, open it and download artifact `SmartSwingScanner-debug-apk`.
6. Extract the downloaded artifact ZIP. It contains `app-debug.apk`.
7. Transfer `app-debug.apk` to your Android phone and tap it to install. Android may ask you to allow installation from that source.

## Important limitations
- This is an early native Android starter, not a direct conversion of the existing Streamlit/Python app.
- It fetches market data from Yahoo Finance's unofficial endpoint, which may block requests, change, or return delayed data.
- The stock list is a starter universe, not the full 1,000-share scanner. Dashboard shows up to 10 symbols under ₹100; other tabs show up to 20 candidates.
- Intraday uses 5-minute candles. BTST uses daily candles and 1-month history. The score is a simple momentum ranking, not a validated strategy.
- Verify prices and liquidity in Groww. No profit is guaranteed. No automated trading or Groww account connection is included.
