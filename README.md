# qrcode_scan

二维码扫描插件
![Screenshot_20181110-160005.jpg](https://upload-images.jianshu.io/upload_images/3646846-c30da8ba73215907.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### 权限：
- `<uses-permission android:name="android.permission.CAMERA" />`
- `<uses-permission android:name="android.permission.VIBRATE"/>`


编辑app目录下的build.gradle:
```groovy
buildscript {
    ext.kotlin_version = '1.2.31'
    ...
    dependencies {
        ...
        classpath "org.jetbrains.kotlin:kotlin-gradle-plugin:$kotlin_version"
    }
}
```
编辑项目目录下的build.gradle:
```groovy
apply plugin: 'kotlin-android'
...
dependencies {
    implementation "org.jetbrains.kotlin:kotlin-stdlib-jre7:$kotlin_version"
    ...
}
```

编辑 pubspec.yaml 文件
```
dependencies:
 flutter_remote_package:
  git:
   url: git@github.com:leyan95/qrcode_scanner.git
   ref: 0.0.1
```

#### 使用方式
```dart
String barcode = await QrcodeScan.scan();
```

