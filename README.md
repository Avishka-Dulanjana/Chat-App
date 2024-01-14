# Online Chatting Application

This project is a starting point for a Flutter application.

# Firebase Installation

- [feedbackFirebase CLI reference](https://firebase.google.com/docs/cli#windows-npm)
- [Firebase Auth REST API](https://firebase.google.com/docs/reference/rest/auth)
- [Add Firebase to your Flutter app](https://firebase.google.com/docs/flutter/setup?platform=ios)


## Environment variable set
- C:\Users\Avishka Dulanjana\AppData\Roaming\npm
- C:\Users\Avishka Dulanjana\AppData\Local\Pub\Cache\bin


## Steps

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