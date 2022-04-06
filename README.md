# CordovaSampleAndroid for CORDOVA 10
## Repo structure:
* demoApp : Android demo app based on Apache Cordova 10 with ClickToAudio and ClickToVideo availability

* smartvideo : Apache Cordova 10 plugin for VideoEngager SmartVideo Android SDK

## Run demoApp
* Follow instructions to install Apache Cordova 10 CLI from here : https://cordova.apache.org/docs/en/11.x/guide/cli/index.html#installing-the-cordova-cli 
* Execute follow commands in terminal:
```bash
cd demoApp
cordova prepare
cordova requirements
cordova build android
cordova run android
```
#### Or if you prefer Android studio 
* Open Project with AndroidStudio located at ```./platforms/android```  then Build and Run . 



## Use ```smartvideo``` plugin in your Application
* Copy plugin folder  ```smartvideo``` to your module root folder.
* Import plugin with command :
```bash
cd <MyAppProjectFolder>
cordova plugin add <ExtModulesRootFolder>/smartvideo
``` 
* Create file ```./platforms/android/app/gradle.properties``` with contents :
```bash
android.useAndroidX=true
android.enableJetifier=true
cdvMinSdkVersion=21
cdvCompileSdkVersion=30
```
* Open Project with AndroidStudio located at ```./platforms/android``` .
* Change some settings or logic based on https://github.com/VideoEngager/SmartVideo-Android-SDK-Demo-App  examples.
* Build and Run app with :
```
cordova build android
cordova run android
```


### Please look at `demoApp/www/index.html` and `demoApp/www/js/index.js` for example usage of plugin.