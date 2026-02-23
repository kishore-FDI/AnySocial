# Background Video Downloader for Android

## Overview
Android application enabling background video downloads from any social media platform using the native Android share sheet. Users continue scrolling content without interruption. No UI launch. No foreground activity. No workflow disruption.

## Core Behavior
1. User scrolls any supported social media app (e.g., Instagram, Twitter/X, Facebook, TikTok, Reddit, YouTube Shorts, etc.).
2. User taps **Share** on a video.
3. User selects this app from the Android share sheet.
4. Video downloads silently in background.
5. User continues scrolling with zero context switch.

## Design Principles
- Zero-friction UX
- No app switching
- No manual URL pasting
- No foreground UI requirement
- Passive background execution
- OS-native integration

## Features
- Android share sheet integration
- Background service downloading
- No app UI required to trigger downloads
- Non-blocking workflow
- Persistent downloads
- System notification download status
- Works across multiple social platforms
- Local storage management

## Architecture
- Share Intent Receiver (`ACTION_SEND`)
- Background Worker (WorkManager / ForegroundService fallback)
- Media resolver
- Downloader service
- Storage manager
- Notification handler

## Flow
```

Social App → Share Button → Android Share Sheet → This App → Background Download → Storage

````

## Permissions
```txt
INTERNET
FOREGROUND_SERVICE
POST_NOTIFICATIONS
READ_MEDIA_VIDEO (Android 13+)
WRITE_EXTERNAL_STORAGE (legacy devices)
````

## Tech Stack

* Kotlin
* Android SDK
* Python
* YT-DLP
* Instaloader

## Installation

```bash
git clone https://github.com/yourusername/your-repo-name.git
```

Open in Android Studio
Sync Gradle
Build
Install APK

