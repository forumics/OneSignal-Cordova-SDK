### OneSignal Cordova Push Notification Plugin
[![npm version](https://img.shields.io/npm/v/onesignal-silent-cordova-plugin.svg)](https://www.npmjs.com/package/onesignal-silent-cordova-plugin)
[![npm downloads](https://img.shields.io/npm/dm/onesignal-silent-cordova-plugin.svg)](https://www.npmjs.com/package/onesignal-silent-cordova-plugin)
 
## This is a plugin based on onesignal-cordova-plugin. Please visit [their repository](https://github.com/OneSignal/OneSignal-Cordova-SDK) for help with everything except the unique functionality I provide.
This plugin allows you to send background notifications on Android. To accomplish this, you must add `"content_available": true` to the data object on your notification. If the app is open when this notification is received, `handleNotificationReceived` will be called with the argument being a JSON object `j` such that `j['payload']['additionalData']` is the data object you sent. No visible notification will be shown as long as the notification has no title or content.
 