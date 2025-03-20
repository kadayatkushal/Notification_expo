# Expo Setup Guide for Native Notify Push Notifications

## 📌 Prerequisites
Make sure you have an existing React Native app set up with Expo.

---

## 🚀 Step 1: Install Dependencies
Run the following commands in your Expo project terminal:

```bash
npm install native-notify
npx expo install expo-device expo-notifications expo-constants
```

---

## 📥 Step 2: Import Native Notify
In your `App.js` or `index.js` (for Expo 50+), add the following import at the top:

```javascript
import registerNNPushToken from 'native-notify';
```

---

## 🔧 Step 3: Use a Functional Component
Ensure your `App.js` or `index.js` (for Expo 50+) is a functional component using Hooks:

```javascript
import React from 'react';
import registerNNPushToken from 'native-notify';

export default function App() {
  React.useEffect(() => {
    registerNNPushToken(28478, '4p5Nh62bDRm3KZyNF0EgdL');
  }, []);

  return (
    // Your app components and logic here
  );
}
```

---

## ⚙️ Step 4: Install Expo EAS CLI (Optional)
If not already installed, run the following command:

```bash
npm install -g eas-cli
```

---

## 🔑 Step 5: Log into Expo EAS Account (Optional)
If not already logged in, run the following command and follow the instructions:

```bash
eas login
```

---

## 🆔 Step 6: Initialize EAS Project ID (Optional)
Run the following command to ensure your project has a project ID for push notifications:

```bash
eas init
```

---

## 🏁 Step 7: Start Expo Development Server
Run the following command to start your app in the Expo Go app:

```bash
npx expo start
```

---

## 📲 Step 8: Testing Push Notifications
Open your app in the Expo Go app on your iOS or Android device.

**Note:** Push notifications do not work in an Android emulator or iOS simulator.

---

## 📝 Additional Notes
✅ Ensure your `appId` and `appToken` values in `registerNNPushToken` are correct and not changed.

📖 For more details on Hooks, refer to the [React Hooks documentation](https://react.dev/reference/react).

