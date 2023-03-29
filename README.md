# Solution Challenge - YoziCare
## Introduction
Our platform provides a convenient way for people to assess their risk of kidney disease and keep track of their dietary habits with automated analysis. Patients can easily record their food intake and receive personalized insights, while also accessing professional support for any kidney-related concerns.


## Installation instructions and dependencies

### Android Studio Environment

- Android Studio (2022.1.1)
- Android SDK : Android 13.0 (Tiramisu), API LEVEL-33
- install Flutter Dart plugin 

### Usage

1. To start working on this project, you should clone this repository into your local machine by using the following command.
```bash
git clone https://github.com/oscarchew/kidney.git
```

2. Please install the recommended version of Android Studio and set up the appropriate environment before opening the project.
3. After setting up the environment, please enter the following command in the terminal to install the package.
```bash
flutter pub get
```
4. Finally, run main.dart to execute the program. 

⚠️ ***IMPORTANT*** ⚠️
There is a bug in the chatbot's underlying program that needs to be resolved by following the steps below.
1. open SoundStreamPlugin.kt
- if your system is LINUX, go to the path : /home/\<your username\>/.pub-cache/hosted/pub.dartlang.org/sound_stream-0.3.0/android/src/main/kotlin/vn/casperpas/sound_stream/SoundStreamPlugin.kt
- if your system is WINDOWS 10, go to the path :  C:\Users\ <your username>\AppData\Local\Pub\Cache\hosted\pub.dev\sound_stream-0.3.0\android\src\main\kotlin\vn\casperpas\sound_stream\SoundStreamplugin.kt
2. find **onRequestPermissionsResult**, and delete **two** question marks(?).

> override fun onRequestPermissionsResult(requestCode: Int, permissions: Array<out String>?, grantResults: IntArray?): Boolean {

to 

> override fun onRequestPermissionsResult(requestCode: Int, permissions: Array<out String>, grantResults: IntArray): Boolean {
  
## Features and functionalities
- **Chronic kidney disease map** : To make it easier for kidney disease patients to travel throughout Taiwan, we have created a map of dialysis centers that enables patients to quickly locate the nearest center in each county or city. We are using the Google Maps API to provide distance estimation and navigation services, and have also added location-specific information to facilitate appointment scheduling and contact.

- **Chronic kidney disease statistics** : 
  - We conduct a preliminary assessment based on the user's family medical history, medication use, and lifestyle habits.
  - Using indicators such as glomerular filtration rate (GFR) and creatinine levels, we determine the stage of the disease and provide dietary recommendations based on the results (linked to the first point for condition identification). In addition to using Firebase or GCP APIs for analysis, we can also display changes in health status over time using line graphs.
  - Water intake is especially important for kidney disease patients, as it is highly correlated with urine output. Both can be uploaded to Firestore and relevant notifications can be pushed to Google Assistant via Firebase Cloud Messaging (FCM).

- **Chatbot** : Users can ask questions related to kidney disease, and our chatbot will provide answers during the conversation. (e.g. "What are the symptoms of kidney disease?")

- **Food Composition Analysis** :Users can upload a photo of their food or choose an existing photo from their gallery to analyze it on Google Cloud Run. The platform will then determine the composition of the food and analyze whether it's suitable for individuals with kidney disease to consume. The results of the analysis will be displayed for the user.

- **Nutrition Label Extraction** : Users can upload a photo of a food label or select an existing photo from their gallery to analyze on Google Cloud Run. The platform will extract the content of the label and focus on the four components that kidney disease patients need to pay the most attention to - protein, fat, sodium, and carbohydrates. The platform will then calculate and display the remaining daily intake limit for each component for the user.

## Timeline
- Pre-demo meeting (3/5 or 3/6)
- [Registration Form (by 3/17)](https://docs.google.com/forms/d/e/1FAIpQLSfsqfUWatcPdlQVa1J2d5ntHGQNoBBFef3Bf4omynGnJvQ8PA/viewform)
- [Submission Form (by 3/31)](https://docs.google.com/forms/d/e/1FAIpQLSdPrVReDh1LSLOe4Z02FjtsiI1S2YhCpdEONeJsteConJWm3w/closedform?resourcekey=0-xr0PTw19aGfSsBwI6u_Zgw)

## Technical Sharing
- [Flutter installation](https://hackmd.io/@vekMh5uNRK-ZfmBnFj1BgQ/rJSbm04Ai)
- [DDD (Domain Driven Design)、AutoRoute (Screens 之間的切換)、IDE 快捷鍵](https://hackmd.io/@MrXP/ByUjh3O0s)
- [Firebase 相關技術 (歡迎編輯分享)](https://hackmd.io/@MrXP/S1NI50wCo)
- [一次搞懂 Android 行動裝置的偵錯功能](https://hackmd.io/@MrXP/HkfnUYO9o)

## Reference
- [off-nutrition-table-extractor](https://github.com/openfoodfacts/off-nutrition-table-extractor)
- [Inverse Cooking: Recipe Generation from Food Images](https://github.com/facebookresearch/inversecooking)

## Contact us
- 1
- 2
- 3
- 4



