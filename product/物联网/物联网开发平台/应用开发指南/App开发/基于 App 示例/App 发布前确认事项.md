
## iOS  

* 确认填写用户自己的 Bundle ID 和对应的发布证书。
* 根据实际情况调整配置文件中的内容，需要配置的内容可参考[ App 参数写入配置文件](https://cloud.tencent.com/document/product/1081/45902#app-.E5.8F.82.E6.95.B0.E5.86.99.E5.85.A5.E9.85.8D.E7.BD.AE.E6.96.87.E4.BB.B6)，获取到相应的 ID 和 key 值替换 App 中的字符串
* 如果用户确认接入 Firebase，用户需要使用从 Firebase 官网自建应用获得 **GoogleService-Info.plist**，替换 App 中 [GoogleService-Info.plist](https://github.com/tencentyun/iot-link-ios/blob/master/Source/LinkApp/Supporting%20Files/GoogleService-Info.plist) 文件。   

## Android   
1. 请根据实际情况调整 **[app-config.json](https://github.com/tencentyun/iot-link-android/blob/master/app-config.json)** 中的内容。除配置内容外，Android 还需要获取数字签名，具体设置及操作请参考 [发布前确认事项](https://github.com/tencentyun/iot-link-android/blob/master/doc/APP%E5%8F%91%E5%B8%83%E5%89%8D%E7%A1%AE%E8%AE%A4%E4%BA%8B%E9%A1%B9.md)

	**注意：同时请遵从官方建议自建微信接入服务器，保证 App Secret 不被泄露**。

2. 项目配置 **Firebase** 插件。
 - 若用户确认使用 Firebase 功能，需通过 Firebase 官网创建应用并获取 **google-services.json**，替换项目中的 [google-services.json](https://github.com/tencentyun/iot-link-android/blob/master/app/google-services.json) 文件。
 - 若不使用 Firebase 功能，需要在 [build.gradle](https://github.com/tencentyun/iot-link-android/blob/master/build.gradle) 文件中注释掉对应依赖，详情请参考 GitHub 源代码说明文件  [发布前确认事项](https://github.com/tencentyun/iot-link-android/blob/master/doc/APP%E5%8F%91%E5%B8%83%E5%89%8D%E7%A1%AE%E8%AE%A4%E4%BA%8B%E9%A1%B9.md)。
