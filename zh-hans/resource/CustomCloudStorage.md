## 自定义云存储

用户自定义去实现云存储面板，参考 [Tuya Smart Camera SDK - 云存储](https://tuyainc.github.io/tuyasmart_camera_android_sdk_doc/zh-hans/resource/CloudStorageProcess.html)

**接口说明**

设置 CloudStoragePanelListener 监听，自定义面板去实现云存储视频播放

```java
TuyaCameraPanelSDK.setCustomCloudStoragePanelListener(CloudStoragePanelListener cloudStoragePanelListener);
```

 **参数说明**

| 参数                      | 说明                                                         |
| :------------------------ | :----------------------------------------------------------- |
| cloudStoragePanelListener | CloudStoragePanelListener 接口，设置此监听，可自定义云存储面板；不设置则跳转到默认涂鸦摄像机云存储面板 |

**示例代码**

```java
TuyaCameraPanelSDK.setCustomCloudStoragePanelListener(new CloudStoragePanelListener() {
    @Override
    public void onCloudStoragePanelClick(String deviceId) {
        L.d(TAG, "云存储面板 -自定义实现" + deviceId);
    }
});
```
