# Simple-notes-app
 Users can add, view, and delete notes. Notes are saved in Firebase Firestore.

Purpose
The app lets users add, view, and delete notes, with all data stored in Firebase Cloud Firestore. It demonstrates basic CRUD (Create, Read, Delete) operations using Flutter and Firebase integration.

Project Setup
Flutter: This is Google’s UI toolkit for building natively compiled apps for mobile, web, and desktop from a single codebase.
Firebase: A platform by Google providing backend services like authentication, database, analytics, etc.
Firebase Cloud Firestore: A NoSQL cloud database to store and sync data in real-time.

Key Dependencies
firebase_core: Required to initialize Firebase in your Flutter app.
cloud_firestore: Allows access to Firestore database from Flutter.

 App Structure
main.dart
Initializes Firebase with await Firebase.initializeApp(); before the app starts.
Sets NotesPage as the home screen.
notes_page.dart
Provides UI to add a note, displays a list of existing notes, and allows deleting notes.
Uses a TextEditingController to get user input.
Uses a StreamBuilder to listen to real-time updates from Firestore’s notes collection.
When a note is added, it calls add() on the collection.
When a note is deleted, it calls delete() on the note’s document.

UI has:
A text field and add button at the top
A scrollable list of notes below, each with a delete button
4. Firebase Integration Steps
Register your app with Firebase (Android/iOS), download config files (google-services.json or GoogleService-Info.plist), and add to the correct folders.
Update native files as per Firebase setup instructions.
Make sure to call Firebase.initializeApp() before using any Firebase services.

 Running the App
Perform flutter pub get to fetch dependencies.
Use flutter run to start the app on an emulator or device.
You can now add and delete notes, which are synced instantly with Firebase.

 What You Learn
How to set up Firebase with Flutter.
Basic real-time CRUD with Firestore.
Simple state management using StatefulWidget.
Using StreamBuilder to listen to Firestore changes live.
