- 22110086 : Tran Van Tuyen

# 📱 Image Loader App

A simple Android application built with React Native that allows users to load an image from a URL and display it in the app UI. This project demonstrates the use of **AsyncTask**, **AsyncTaskLoader**, **network state monitoring**, **broadcast receivers**, and **background service notifications**.

---

## 🎯 Objective

Create an Android app that loads an image from a user-provided URL and displays it in the UI. The app must incorporate:

- AsyncTask / AsyncTaskLoader (React Native equivalent: async/await)
- Internet connection handling (via NetInfo)
- Broadcast receivers (using NetInfo’s event listener)
- Service notifications (via `react-native-push-notification`)

---

## ✅ Features Implemented

### 1. Image Loading

- User enters an image URL.
- Click "Load Image" to fetch and display the image.
- Displays loading status with `ActivityIndicator`.
- Shows success or error status message.

### 2. Internet Connection Handling

- App uses `@react-native-community/netinfo` to detect internet connection.
- "Load Image" button is disabled if no connection is available.
- Displays `"No internet connection"` when offline.

### 3. Periodic Notifications

- App uses `react-native-push-notification` to send a local notification every 5 minutes with message:
  > "Image Loader Service is running"
- Notification setup runs on Android via channel creation.

---

## 🛠️ Technologies Used

- React Native
- TypeScript (or JavaScript)
- NetInfo for connectivity
- PushNotification for background notifications

---

## 🧪 Example Workflow

1. **User Input**:  
   User inputs a valid image URL in the `TextInput`.

2. **Connectivity Check**:  
   The app checks for internet using NetInfo. If offline:

   - Disables Load button
   - Shows `"No internet connection"`

3. **Image Loading**:  
   App fetches the image URL using `fetch()`, and:

   - Displays a loading indicator
   - Shows image if successful
   - Shows error if failed

4. **Background Notification**:  
   Every 5 minutes, a local notification is shown:
   > 📸 Image Loader Service is running

---

## 🔐 Permissions

The following permissions are required and should be added in `AndroidManifest.xml`:

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```
