# Okto SDK React Native Template

This is a React Native template pre-configured with [Okto SDK](https://docs.okto.tech/) for building chain abstracted decentralized applications on mobile. It provides a solid foundation for creating Web3-enabled mobile applications with best practices and essential tooling.

## Features

- ⚡️ **Expo** with the latest SDK
- 🔐 **Okto SDK** integration for seamless Web3 functionality
- 📱 **Cross-platform** support for iOS and Android
- 🔒 **Authentication** setup with Google OAuth

## Prerequisites

Before you begin, ensure you have the following installed:
- Node.js 18.x or later and npm/yarn
- **Okto API Keys:** `clientPrivateKey` and `clientSWA`. Obtain these from the [Okto Developer Dashboard](https://dashboard.okto.tech/login).
- Google OAuth Credentials for each platform (Web, iOS, Android)

## Getting Started

<details>
<summary><b>Expo</b></summary>

1. Clone this template:
   ```bash
   git clone https://github.com/okto-hq/okto-sdkv2-react-native-template-app.git
   cd okto-sdkv2-react-native-template-app
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Configure your credentials in the app:
   ```typescript
   // Update the configuration in app/_layout.tsx
   const config = {
     environment: "sandbox",
     clientPrivateKey: "YOUR_CLIENT_PRIVATE_KEY",
     clientSWA: "YOUR_CLIENT_SWA",
   };
   ```

4. Configure Google OAuth in LoginScreen.tsx:
   ```typescript
   // Update the Google OAuth configuration
   const [request, response, promptAsync] = Google.useAuthRequest({     
     webClientId: "YOUR_GOOGLE_WEB_CLIENT_ID",
     iosClientId: "YOUR_GOOGLE_IOS_CLIENT_ID",
     androidClientId: "YOUR_GOOGLE_ANDROID_CLIENT_ID", 
     scopes: ['openid', 'profile', 'email']
   });
   ```

5. Start the development server:
   ```bash
   npx expo start
   ```

</details>

<details>
<summary><b>React Native CLI</b></summary>

1. Clone this template:
   ```bash
   git clone https://github.com/okto-hq/okto-sdkv2-react-native-template-app.git
   cd okto-sdkv2-react-native-template-app
   ```

2. Install dependencies:
   ```bash
   npm install
   
   # For iOS
   cd ios && pod install && cd ..
   ```

3. Configure your credentials in the app:
   ```typescript
   // Update the configuration in app/_layout.tsx
   const config = {
     environment: "sandbox",
     clientPrivateKey: "YOUR_CLIENT_PRIVATE_KEY",
     clientSWA: "YOUR_CLIENT_SWA",
   };
   ```

4. Configure Google OAuth in LoginScreen.tsx:
   ```typescript
   // Update the Google OAuth configuration
   const [request, response, promptAsync] = Google.useAuthRequest({     
     webClientId: "YOUR_GOOGLE_WEB_CLIENT_ID",
     iosClientId: "YOUR_GOOGLE_IOS_CLIENT_ID",
     androidClientId: "YOUR_GOOGLE_ANDROID_CLIENT_ID", 
     scopes: ['openid', 'profile', 'email']
   });
   ```

5. Start the development server:
   ```bash
   # For iOS
   npx react-native run-ios
   
   # For Android
   npx react-native run-android
   ```

</details>

## Obtaining Credentials

### Okto API Keys
To obtain your Okto API credentials:
1. Sign up or log in to the [Okto Developer Dashboard](https://dashboard.okto.tech/login)
2. Create a new project or select an existing one
3. Navigate to the API Keys section
4. Copy your `clientPrivateKey` and `clientSWA` values

### Google OAuth Credentials
For Google Sign-In functionality:
1. Set up a project in [Google Cloud Console](https://console.cloud.google.com/)
2. Create OAuth 2.0 credentials for each platform:
   - Web Client ID (for Expo Go and web)
   - iOS Client ID
   - Android Client ID
3. Follow the platform-specific setup guides in the [Okto documentation](https://docs.okto.tech/)

## Learn More

- [Okto SDK Documentation](https://docs.okto.tech/)
- [Expo Documentation](https://docs.expo.dev/)
- [React Native Documentation](https://reactnative.dev/docs/getting-started)

## Contributing

Contributions are welcome! Please take a moment to review our [CONTRIBUTING.md](CONTRIBUTING.md) guidelines before submitting any Pull Requests. Your contributions are invaluable to the Okto community.
