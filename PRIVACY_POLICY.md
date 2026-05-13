# Privacy Policy for TitanSpark Downloader (Extension & Desktop Application)

**Last Updated:** May 13, 2026

## 1. Introduction

This Privacy Policy applies to the entire TitanSpark Downloader ecosystem, which consists of two connected components: the **TitanSpark Browser Extension** and the **TitanSpark Desktop Application**.

We are committed to protecting your privacy. This policy explicitly outlines how local data is handled between your browser, your local machine, and the servers hosting your downloads. At no point does TitanSpark collect, store, or transmit your personal data to the developer or any external third-party analytics services.

## 2. Information Handled by the Browser Extension

The browser extension acts strictly as a local bridge. To successfully intercept and hand off a download, the extension temporarily reads the following data from your active browser session:

- **Download URLs:** The direct link to the file you are attempting to download.
- **Session Cookies:** To ensure the desktop application can authenticate with protected servers.
- **Request Headers:** Such as `Referer` and `User-Agent`, required by host servers to authorize the request.

**Strictly Local Handoff:** When a download is intercepted, this session data is routed securely via Native Messaging directly to the local TitanSpark executable (`com.titanspark.broker`) installed on your computer. The extension does not transmit this data over the internet.

## 3. Information Handled by the Desktop Application

The TitanSpark Desktop Application performs the heavy lifting of multi-threaded downloading.

- **Direct Network Connections:** The desktop application uses the URLs, cookies, and headers provided by the extension to establish direct HTTP connections with the server hosting the file.
- **Local Storage:** Downloaded file segments are saved directly to your device's local storage drives.
- **No Telemetry or Tracking:** The desktop application is entirely self-contained. It does not monitor your computer, it does not maintain a remote cloud backup of your download history, and it does not "phone home" with usage analytics or telemetry.

## 4. Data Retention and Third-Party Sharing

Across both the Extension and the Desktop Application, our data philosophy is identical:

- **No External Transmission:** No user data, personal information, browsing history, cookies, or headers are ever transmitted to the developer, third-party services, or advertisers.
- **No Data Storage:** Neither the extension nor the app remotely stores your browsing history. Required session data exists in memory solely for the duration needed to download the file.
- **No Third-Party Sharing:** We do not sell, trade, rent, or otherwise transfer any of your data to outside parties.

## 5. Required Extension Permissions Justification

To uphold transparency for Chrome Web Store compliance, here is exactly why the extension requests specific browser permissions:

- **`downloads` & `webRequest`:** Used to intercept the browser's native download event and capture necessary headers to prevent download failures.
- **`cookies`:** Used to read the session authentication for the specific file being downloaded, allowing the desktop app to bypass login walls.
- **`nativeMessaging`:** Used as the secure, local-only communication bridge between the browser extension and your installed desktop application.
- **`storage`:** Used entirely locally to save your personal extension preferences, such as toggling interception on or off.

## 6. Compliance

TitanSpark Downloader complies fully with the Chrome Web Store User Data Policy. The extension's use of information received from Chrome APIs adheres to the strictly necessary requirements for providing its core functionality.

## 7. Contact

If you have any questions or concerns regarding this privacy policy or the data handling practices of either the extension or the desktop app, please open an issue on the official project repository:

<https://github.com/sas5/TitanSpark-Public>
