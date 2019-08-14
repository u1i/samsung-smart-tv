http://192.168.1.XXX:8001/api/v2/

https://developer.samsung.com/tv/develop/extension-libraries/smart-view-sdk/receiver-apps/debugging

[MUST] set TV in development mode
On TV, goto Apps => My Apps and using the remote, enter 12345 in sequence.
Set Developer mode to On.
Input IP Address of client (on same WiFi).
Reboot TV.(Unplug and Plug the TV)
Input http://TV_IP:8001 a browser as same network AP

http://192.168.1.210:8001/

http://192.168.1.210:8001/logs

If you want to do it manually you can use for example "Simple Web Socket Client" extension for Firefox (or Chrome), then use as URL:
CODE: SELECT ALL

https://forum.samygo.tv/viewtopic.php?t=12384

ws://YOUR_TV_IP:8001/api/v2/channels/samsung.remote.control?name=cmNjbGk=
(name= at the end is name of device in base64, here "rccli")
and as request, e.g. (even if TV should already have asked your agreement at this point...)

{"method":"ms.channel.emit","params":{"event": "ed.installedApp.get", "to":"host"}}

ws://192.168.1.210:8001/api/v2/channels/samsung.remote.control?name=cmNjbGk=

https://github.com/razzo04/samsungtv-api

Keys
https://github.com/robertoostenveld/samsung
