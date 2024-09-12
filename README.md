# TLabWebViewVR

[日本語版READMEはこちら](README-ja.md)

Sample project for using WebView in Oculus quest VR in Unity. Includes Meta XR SDK and XR Interaction Toolkit implementation example.

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/tlabaltoh)

## Operating Environment
|                |                     |
| -------------- | ------------------- |
| Headset        | Oculus Quest 2      |
| GPU            | Qualcomm Adreno 650 |
| Unity          | 2021.37f1           |

## Getting Started

### Set Up
- Build Settings

| Property      | Value   |
| ------------- | ------- |
| Platform      | Android |

- Project Settings

| Property          | Value                                 |
| ----------------- | ------------------------------------- |
| Color Space       | Linear                                |
| Minimum API Level | 29                                    |
| Target API Level  | 30 (Unity 2021), 31 ~ 32 (Unity 2022) |


- Add the following symbols to Project Settings --> Player --> Other Settings (to be used at build time)  

``` 
UNITYWEBVIEW_ANDROID_USES_CLEARTEXT_TRAFFIC 
```
``` 
UNITYWEBVIEW_ANDROID_ENABLE_CAMERA 
```
``` 
UNITYWEBVIEW_ANDROID_ENABLE_MICROPHONE 
```

- XR Plug-in Management

| Property        | Value               |
| --------------- | ------------------- |
| Plugin Provider | Oculus (not OpenXR) |

- If you want to access files that are in external storage (like download, picture). you need to add follow manifest in Android 11 ([detail](https://developer.android.com/training/data-storage/manage-all-files?hl=en)).

```.xml
<uses-permission android:name="android.permission.MANAGE_EXTERNAL_STORAGE" />
```
