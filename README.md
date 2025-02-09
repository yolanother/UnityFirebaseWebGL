# FirebaseWebGL
A Unity package that makes use of the Firebase Javascript SDK to implement the basic Realtime Database functions on WebGL builds

## Installation
- Copy the FirebaseWebGL folder into your Unity project assets folder.
- Consider also adding the RestClient, Fullserializer and Textmeshpro folders to get the project fully up and running.
- Alternatively,  you can import the latest .unitypackage from the repository releases.

## Usage
  1) Call any of the basics Firebase Javascript SDK functions from the FirebaseBridge.cs class
  2) Build for WebGL
  3) Include the Firebase app configuration in the index.html file generated by Unity (you can use this tutorial [here](https://firebase.google.com/docs/web/setup#from-the-cdn)).
  4) Finally, make sure to also include the Firebase SDKs you need to use in your App (You can find a list of services [here](https://firebase.google.com/docs/web/learn-more#available-libraries)).
  5) EXTRA STEP: Earlier in 2021 Unity made some modifications to their WebGL library. The following line (`this.unityInstance = unityInstance`) must now also be added in your index.html, when the unityInstance is created (after the `}).then((unityInstance) => {` line) so that your app can properly comunicate with Unity.
 
 ## Services
 - Realtime Database
 - Authentication
 - Cloud Functions
 - Storage
 - Firestore
  
## Additional info
- You can find a working implementaiton of this package [here](https://rotolonico.github.io/FirebaseWebGLImplementation/)
- For Storage, you'll also need to set up cors for your bucket. More info [here](https://firebase.google.com/docs/storage/web/download-files#cors_configuration) or in the README.txt file in the Storage example in the project.
