# APK बनाने के आसान steps

Android Studio की जरूरत नहीं है।

### 1. GitHub खोलें
GitHub पर नया repository बनाएं।

### 2. ZIP की files upload करें
ZIP को GitHub repository में upload/extract करें। ध्यान रहे कि `.github/workflows/build-apk.yml` भी upload हो।

### 3. Actions खोलें
Repository → **Actions** → **Build Ankit Mart APK** → **Run workflow**.

### 4. APK डाउनलोड करें
Build पूरा होने के बाद workflow के नीचे **Artifacts → AnkitMart-APK** दिखाई देगा। उसे डाउनलोड करें और उसके अंदर मौजूद `app-debug.apk` फोन में भेजें।

### 5. फोन में install करें
`app-debug.apk` पर tap करें और Install दबाएं। अगर Android permission मांगे तो जिस browser/file manager से APK खोला है, उसके लिए **Install unknown apps** अनुमति दें।

## APK में क्या रहेगा

यह project uploaded Ankit Mart HTML को Android WebView में चलाता है। इसलिए website का existing product API, cart, profile/login, orders और checkout logic HTML के अंदर जैसा है वैसा ही package किया गया है।
