# Visual Studio App Center Sample App for Android 
The Android application in this repository and its corresponding tutorials will help you quickly and easily onboard to Visual Studio App Center.

Written in Java with Android Studio 3.1

&nbsp;  
&nbsp;
&nbsp;

# Distribute

Visual Studio App Center supports distribution of APKs to end users or testers.    

## Getting Started

### app/build.gradle

```
dependencies {
    def appCenterSdkVersion = '1.4.0'
    compile "com.microsoft.appcenter:appcenter-analytics:${appCenterSdkVersion}"
    compile "com.microsoft.appcenter:appcenter-crashes:${appCenterSdkVersion}"
    compile "com.microsoft.appcenter:appcenter-distribute:${appCenterSdkVersion}"
    compile "com.microsoft.appcenter:appcenter-push:${appCenterSdkVersion}"
}
```


### Add the following to the Activity onCreate

```
AppCenter.start(getApplication(), "[APP SECRET]",Distribute.class);
``` 

### Imports

```
import com.microsoft.appcenter.distribute.Distribute;
```

&nbsp;  
&nbsp;
&nbsp;  

## Build

![Build](/art/build1.png)

&nbsp;  
&nbsp;
&nbsp;  

## Public Distribution

The application can be distributed as "Public" using a publish link to download the initial app.   Thereafter the app will deploy via notifications.  Alternatively, closed distribution groups can be configured.

![Distribute](/art/publicdistro.png)

&nbsp;  
&nbsp;
&nbsp;  

## Custom In App Notification

The dialog presented on update can be customized via a DistributeListener.   A CustomDistributeListener is implemented in the sample as an example.

### To use the DistributeListener add the following within the Activity OnCreate:

```
   Distribute.setListener(new CustomDistributeListener());
```



![Update](/art/inappupdate.png)

&nbsp;  
&nbsp;
&nbsp;  

## Tutorials

The Official Visual Studio App Center Tutorials


## Contents
| Tutorial | Description |
|:-|:-|
| [Getting Started](https://docs.microsoft.com/en-us/appcenter/quickstarts/android/getting-started) | Set up the app |
| [Build](https://docs.microsoft.com/en-us/appcenter/quickstarts/android/build) | Build the app |
| [Test](https://docs.microsoft.com/en-us/appcenter/quickstarts/android/test) | Run automated UI tests on real devices |
| [Distribute](https://docs.microsoft.com/en-us/appcenter/quickstarts/android/distribute)| Distribute application to a group of users |
| [Crashes](https://docs.microsoft.com/en-us/appcenter/quickstarts/android/crashes) | Monitor application crashes |
| [Analytics](https://docs.microsoft.com/en-us/appcenter/quickstarts/android/analytics) | View user analytics |
| [Push](https://docs.microsoft.com/en-us/appcenter/quickstarts/android/push) | Send push notifications to your app users |
