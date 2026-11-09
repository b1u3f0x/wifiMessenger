# wifiMessenger

A lightweight Android application for communicating over the same local WiFi network. The app discovers nearby devices, shows them in a peer list, and enables local messaging between devices without requiring an internet connection or a central server.

## Features

- Discover peers on the same WiFi network
- Display a list of active nearby users
- Open a chat session with a selected contact
- Send text messages locally over the network
- Start and stop a background service for network discovery
- Handle WiFi connectivity and boot state changes
- Includes support for local voice call flow and related networking utilities

## Screenshots

This repository does not include screenshots in the codebase, but the app is structured around:
- a startup screen for setting a username
- a main peer list screen
- a chat activity for messages
- call-related activity and service logic

## Tech Stack

- Java
- Android SDK
- Gradle
- Android support library (`appcompat-v7`)
- WiFi/network discovery using Android services and receivers

## Project Structure

```text
wifiMessenger/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/byteshaft/wifimessenger/
│   │   │   │   ├── activities/
│   │   │   │   ├── database/
│   │   │   │   ├── receivers/
│   │   │   │   ├── services/
│   │   │   │   └── utils/
│   │   │   ├── res/
│   │   │   └── AndroidManifest.xml
│   ├── build.gradle
│   └── proguard-rules.pro
├── build.gradle
├── gradlew
├── gradlew.bat
├── settings.gradle
├── gradle.properties
├── .gitignore
└── wifiMessenger.iml
```

## Main Components

- `MainActivity`: entry point, username setup, peer discovery, user selection
- `ChatActivity`: chat UI and messaging flow
- `CallActivity`: voice call handling
- `LongRunningService`: long-lived background service for connectivity features
- `WifiReceiver` and `BootStateListener`: monitor WiFi and device boot events
- `ServiceHelpers`: network and peer management helpers
- `AppGlobals`: application-wide state storage

## Requirements

- Android Studio
- JDK 7/8
- Android SDK configured for the project
- A physical Android device or emulator
- WiFi enabled and connected to the same local network

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/codebasepk/wifiMessenger.git
   cd wifiMessenger
   ```

2. Open the project in Android Studio.

3. Sync Gradle dependencies.

4. Build and run the app on an Android device.

5. Ensure all devices are connected to the same WiFi network.

## Usage

- Launch the app
- Enter a display name
- Enable the service if needed
- Wait for nearby devices to appear
- Select a peer to start a local chat session

## Notes

- This project is an Android prototype/demo for local WiFi communication.
- It is designed for devices on the same network and is not a production-ready messaging platform.
- The voice call support and messaging components are implemented as local networking features rather than cloud-based services.

## License

This repository does not currently include a license file, so the license status is unspecified.
