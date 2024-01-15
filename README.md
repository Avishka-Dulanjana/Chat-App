# Online Chatting Application

This project is a starting point for a Flutter application.

# Firebase Installation

- [feedbackFirebase CLI reference](https://firebase.google.com/docs/cli#windows-npm)
- [Firebase Auth REST API](https://firebase.google.com/docs/reference/rest/auth)
- [Add Firebase to your Flutter app](https://firebase.google.com/docs/flutter/setup?platform=ios)


### Environment variable set
- C:\Users\Avishka Dulanjana\AppData\Roaming\npm
- C:\Users\Avishka Dulanjana\AppData\Local\Pub\Cache\bin


### Steps

- Add Firebase to your Flutter app - all steps in there and refer it carefully

### Need to add this code into main before apps run

```agsl

void main() async {
  WidgetsFlutterBinding.ensureInitialized();
  await Firebase.initializeApp(
     options: DefaultFirebaseOptions.currentPlatform,
  );
  runApp(const MyApp());
  }

```

# Firebase storage setup

<b>Add this security rule to authentic users can view, upload image</b>

```agsl
<b>dsdsd</b>
rules_version = '2';

// Craft rules based on data in your Firestore database
// allow write: if firestore.get(
//    /databases/(default)/documents/users/$(request.auth.uid)).data.isAdmin;
service firebase.storage {
  match /b/{bucket}/o {
    match /{allPaths=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```
<b>Add this dependencies also to upload image to firebase and take images</b>

```agsl
 flutter pub add image_picker 
 flutter pub add firebase_storage
```

# Fire store storage setup

<b>Add this security rule to authentic users can view, upload image</b>

```agsl
rules_version = '2';

service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```
<b>Add this dependencies also to upload image to firebase and take images</b>

```agsl
 flutter pub add cloud_firestore
```