# Shelelwa Star Academy - Setup Guide

## Prerequisites

- Node.js 14+ installed
- npm or yarn package manager
- Expo CLI: `npm install -g expo-cli`
- Firebase account
- Git

## Step 1: Clone Repository

```bash
git clone https://github.com/anzimbu-tech/shelelwa-star-academy.git
cd shelelwa-star-academy
```

## Step 2: Install Dependencies

```bash
npm install
# or
yarn install
```

## Step 3: Set Up Firebase

1. Go to [Firebase Console](https://console.firebase.google.com)
2. Create a new project named "shelelwa-star-academy"
3. Enable Authentication (Email/Password)
4. Enable Firestore Database
5. Copy your Firebase config
6. Create `.env` file from `.env.example`:
   ```bash
   cp .env.example .env
   ```
7. Paste your Firebase credentials into `.env`

## Step 4: Run Development Server

```bash
npm start
```

Then press:
- `i` for iOS simulator
- `a` for Android emulator
- `w` for web browser

## Step 5: Build for Production

### Web
```bash
expo export --platform web
```

### Mobile
```bash
eas build
```

## Project Structure

```
shelelwa-star-academy/
├── src/
│   ├── firebase/
│   │   ├── firebaseConfig.js
│   │   ├── auth.js
│   │   └── firestoreService.js
│   ├── screens/
│   │   ├── LoginScreen.js
│   │   ├── HomeScreen.js
│   │   └── StudentsScreen.js
│   ├── services/
│   │   └── SyncService.js
│   └── App.js
├── app.json
├── package.json
└── .env
```

## Key Features

- ✅ Offline-first architecture
- ✅ Real-time Firebase sync
- ✅ Student management
- ✅ Teacher management
- ✅ Attendance tracking
- ✅ Grades management
- ✅ Class scheduling
- ✅ Secure authentication

## Troubleshooting

### Firebase connection issues
- Ensure Firebase config is correctly set in `.env`
- Check Firebase rules allow read/write
- Verify internet connection for sync

### Build errors
- Clear cache: `expo start --clear`
- Reinstall dependencies: `rm -rf node_modules && npm install`

For more help, visit [Expo Documentation](https://docs.expo.dev)