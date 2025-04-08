<p align="center">
  <img width="200" height="auto" src="https://github.com/athuld/revanced-gphotos/blob/main/google-photos-revanced.png" />
</p>

# Revanced GPhotos
Revanced GPhotos 为非 Pixel 设备和非 Root 设备提供无限量的原画质照片备份功能，通过伪造设备指纹为 Pixel XL 实现。

## 安装步骤
* 下载 [GmsCore](https://github.com/ReVanced/GmsCore/releases) 并登录
* 从 [下载页面](https://github.com/lzsq520/revanced-gphotos/releases) 选择所需版本
* 打开 revanced gphotos 并选择账户，这将同步您的内容，请确保开启备份选项

如需使用原版图标的 ReVanced GPhotos，请访问此仓库 - [Unofficial-Life/revanced-gphotos-build](https://github.com/Unofficial-Life/revanced-gphotos-build)

## 为什么创建此仓库？
此定制版本主要为个人使用而制作，因为常规的 revanced gphotos 使用较为繁琐。对于修改版应用，每次登录需要手动选择账户，且由于包名不同，系统会同时安装两个同名同图标的应用，容易造成混淆。

* 本仓库提供两种版本：
  * *rvicon* 版本：带有自定义图标和名称（Photos Revanced），可与官方应用共存并显示在启动器中
  * *rvicon-no-launcher* 版本：功能与 rvicon 相同，但不会出现在启动器。适合仅需自动后台备份的用户

### 注意
若与官方应用同时使用，请关闭官方应用的自动备份功能以避免占用存储空间。

## ReVanced 定制品牌补丁
本仓库的下载文件使用我开发的 [自定义品牌补丁](https://github.com/athuld/revanced-patches/commit/3c561c939d2cce8f89ac26a2a1f240eea9019ce8)（灵感来自 YouTube Revanced 的同类补丁），完整致谢原始补丁作者。

使用 ReVanced CLI 的补丁配置如下：
```json
[{
  "patchName": "GmsCore support",
  "options": [{
    "key": "gmsCoreVendorGroupId",
    "value": "app.revanced"
  }]
}, {
  "patchName": "Custom G-Photos branding",
  "options": [{
    "key": "appName",
    "value": "Photos ReVanced"
  }, {
    "key": "iconPath",
    "value": "ReVanced*Logo"
  }, {
    "key": "isLauncherEnabled",
    "value": "false"
  }]
}, {
  "patchName": "Spoof features",
  "options": [{
    "key": "featuresToEnable",
    "value": ["com.google.android.apps.photos.NEXUS_PRELOAD", "com.google.android.apps.photos.nexus_preload"]
  }, {
    "key": "featuresToDisable",
    "value": ["com.google.android.apps.photos.PIXEL_2017_PRELOAD", ...（完整列表见原版）]
  }]
}]
```
# 以下是原始版本

<p align="center">
  <img width="200" height="auto" src="https://github.com/athuld/revanced-gphotos/blob/main/google-photos-revanced.png" />
</p>

# Revanced GPhotos
Revanced GPhotos provide unlimited photos backup for non-pixel and non-rooted devices with original quality. This is done by spoofing the device fingerprint to Pixel XL.

## Installation
* Download [GmsCore](https://github.com/ReVanced/GmsCore/releases) and login
* Download the desired gphotos variant from [Downloads](https://github.com/athuld/revanced-gphotos/releases)
* Open revanced gphotos and select your account , this will sync your content and make sure allow backup option is turned on.

If you are looking for ReVanced GPhotos with Original Icon you can checkout this repository - [Unofficial-Life/revanced-gphotos-build](https://github.com/Unofficial-Life/revanced-gphotos-build)


## Why this repository ?
This custom build is made mostly for personal use as i find the normal revanced gphotos a bit cumbersome. For the patched gphotos, we have to manually select the account each time we login and since the package name of the revanced gphotos is different , we will be having two googlephotos app installed with the same name and same icon and this will get confusing if we want to use the official gphotos app.
* In this repository downloads there are two build variants
  * *rvicon* version : ReVanced GPhotos build with Custom Icon and Custom Name (Photos Revanced). This version will be installed alongside the official gphotos app and will be shown in your app launcher.
  * *rvicon-no-launcher* version : Same as *rvicon* version but this variant will not show up in the app launcher. This version is made for users which needs to just bakup photos and don't want to see the icon in the launcher. The app will automatically backup in background so this variant will act as an automatic backup up which is handy.

 ### Note
 If you are installing the ReVanced GPhotos alongside the official GPhotos app then turn off automatic backup in Offical app so that you are not using the available space in your account.
 
## ReVanced Custom Branding Patch

The downloads in this repository is patched using my [custom gphotos branding patch](https://github.com/athuld/revanced-patches/commit/3c561c939d2cce8f89ac26a2a1f240eea9019ce8) which is heavily inspired from the youtube revanced custom branding patch. All credits goes to the original patch authors.

Following options is used to patch the app using Revanced CLI
```json
[ {
  "patchName" : "GmsCore support",
  "options" : [ {
    "key" : "gmsCoreVendorGroupId",
    "value" : "app.revanced"
  } ]
}, {
  "patchName" : "Custom G-Photos branding",
  "options" : [ {
    "key" : "appName",
    "value" : "Photos ReVanced"
  }, {
    "key" : "iconPath",
    "value" : "ReVanced*Logo"
  },{
    "key" : "isLauncherEnabled",
    "value" : "false"
  } ]
}, {
  "patchName" : "Spoof features",
  "options" : [ {
    "key" : "featuresToEnable",
    "value" : [ "com.google.android.apps.photos.NEXUS_PRELOAD", "com.google.android.apps.photos.nexus_preload" ]
  }, {
    "key" : "featuresToDisable",
    "value" : [ "com.google.android.apps.photos.PIXEL_2017_PRELOAD", "com.google.android.apps.photos.PIXEL_2018_PRELOAD", "com.google.android.apps.photos.PIXEL_2019_MIDYEAR_PRELOAD", "com.google.android.apps.photos.PIXEL_2019_PRELOAD", "com.google.android.feature.PIXEL_2020_MIDYEAR_EXPERIENCE", "com.google.android.feature.PIXEL_2020_EXPERIENCE", "com.google.android.feature.PIXEL_2021_MIDYEAR_EXPERIENCE", "com.google.android.feature.PIXEL_2021_EXPERIENCE", "com.google.android.feature.PIXEL_2022_MIDYEAR_EXPERIENCE", "com.google.android.feature.PIXEL_2022_EXPERIENCE", "com.google.android.feature.PIXEL_2023_MIDYEAR_EXPERIENCE", "com.google.android.feature.PIXEL_2023_EXPERIENCE", "com.google.android.feature.PIXEL_2024_MIDYEAR_EXPERIENCE", "com.google.android.feature.PIXEL_2024_EXPERIENCE", "com.google.android.feature.PIXEL_2025_MIDYEAR_EXPERIENCE" ]
  } ]
}]
```

Full credit to the [ReVanced](https://github.com/athuld/revanced-patches.git]) team for every tools and patches that is used.
