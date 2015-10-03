## WordCard  
&copy; Anand Gaurav (OpenALM)
<br>WordCard is a simple Android app that helps users improve their English vocabulary. 

#### About the app
This app 'WordCard' is useful in improving one's English vocabulary. It uses a static list of interesting Enginsh words and prompts the users to guess the meaning of the word before she can view the actual word definition/meaning.
One can use the *random* mode or *aphabetical* mode.
Also shows the users list of all the words and its definitions/meanings.

### Code
This app uses native Android programming using Android Studio. 
* Uses basic Android programming.
* Tries to use Google's material design
* Target devices: Android Lollipop (5.0 and above)
* Makes use of RecycleView for listing out the words and their meanings/definitions. 
* Uses gradle to build

#### Integrating HockeyApp to the app
Baisc integrations are already done in this app to collect usage info and crash info. Refer to [this document](http://support.hockeyapp.net/kb/client-integration-android/hockeyapp-for-android-sdk) to get more info on hockeyApp SDK integration with Android app.

### Build using Visual studio Online
The app needs gradle to build and hence you would need Gradle task to build the application. Just use the Gradle build task/step and provide the following inputs:
* **Gradle Wrapper:** path to **gradlew.bat** file 
* **Task:** assemple
There would be certain issues in building this project as certain library dependencies cannot be resolved through the online maven or jcenter repos. You would need to download the Android support libraries through Android SDK Manager on the agent machine and point gradle to local repo. 
Reach out to me for more info, if required.

### Deploy to HockeyApp
Use [HockeyApp](https://github.com/ashtom/vso-task-hockeyapp) task to deploy to HockeyApp.
Refer to the instructions [here](https://github.com/ashtom/vso-task-hockeyapp) to use the above mentioned task by building the task ocally and uploading to your account.
_*Note:*_ _This task is still alpha and may under go some changes_
Fill in the following inputs:
* **HockeyApp API token:** Fill in the API token that you can generate from HockeyApp. Login to your HockeyApp account. Go to *Manage Accounts* (click on your name on the top right section) > *API tokens* > *Create API token*	
* **App ID:** Refer to [this document](http://support.hockeyapp.net/kb/client-integration-android/hockeyapp-for-android-sdk) to get the App ID 
* **Binary File Path:** This is the path to apk file generated on build of your app. Try using: 'app\build\outputs\apk\*debug.apk' (without the quotes)



