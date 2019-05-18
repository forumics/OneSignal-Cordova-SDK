### OneSignal Cordova Push Notification Plugin
[![npm version](https://img.shields.io/npm/v/onesignal-silent-cordova-plugin.svg)](https://www.npmjs.com/package/onesignal-silent-cordova-plugin)
[![npm downloads](https://img.shields.io/npm/dm/onesignal-silent-cordova-plugin.svg)](https://www.npmjs.com/package/onesignal-silent-cordova-plugin)
 
## This is a plugin based on onesignal-cordova-plugin. Please visit [their repository](https://github.com/OneSignal/OneSignal-Cordova-SDK) for help with everything except the unique functionality I provide.
This plugin allows you to send background notifications on Android. To accomplish this, you must add `"content_available": true` to the data object on your notification. If the app is open when this notification is received, `handleNotificationReceived` will be called with the argument being a JSON object `j` such that `j['payload']['additionalData']` is the data object you sent. No visible notification will be shown as long as the notification has no title or content.
 
 
 Updated to Onesignal 2.4.6
Tested on android

curl -X POST \
  https://onesignal.com/api/v1/notifications \
  -H 'Accept: */*' \
  -H 'Authorization: Basic MThiOWNiNzItM2I3MC00Yzc0LTgzYTMtMzk5ZjQxNWY0ZGE1' \
  -H 'Cache-Control: no-cache' \
  -H 'Connection: keep-alive' \
  -H 'Content-Type: application/json' \
  -H 'Host: onesignal.com' \
  -H 'Postman-Token: 55b2400e-286e-49ba-b430-575f85ed9c11,3d723550-3a36-498b-b8e8-2fe0cefb9e38' \
  -H 'User-Agent: PostmanRuntime/7.13.0' \
  -H 'accept-encoding: gzip, deflate' \
  -H 'cache-control: no-cache' \
  -H 'content-length: 219' \
  -H 'cookie: __cfduid=da8b7e241c2d1295e6c6acd8273dd3c141555170817' \
  -b __cfduid=da8b7e241c2d1295e6c6acd8273dd3c141555170817 \
  -d '{
  "app_id": "8d871b89-818a-4380-8382-501f97611079",
  "content_available": true,
  "include_player_ids": ["af3e863e-22a3-45d8-8553-d9901031abc1"],
  "data": {"foo": "bar"}
}'
