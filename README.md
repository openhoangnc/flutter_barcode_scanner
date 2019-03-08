# flutter_barcode_scanner

A new Flutter plugin supports barcode scanning on both Android and iOS.

![alt text](https://github.com/AmolGangadhare/MyProfileRepo/blob/master/flutter_barcode_scanning_demo.gif "Demo")



## Try example
Just clone the repository, open the project in `Android Studio/ VS Code`, open `pubspec.yaml` and click on `Packages get`.
Connect device and hit `run`. To run on iPhone you need to run from `Xcode first time` and just make `pod install` in `example/ios`.

## Getting Started 
### Android
To use on android, you need to add some permissions and a BarcodeCaptureActivity to AndroidManifest.
1. Add the camera permission to your AndroidManifest.xml

    <uses-permission android:name="android.permission.CAMERA" />

2. Add the BarcodeScanner activity to your AndroidManifest.xml. Do NOT modify the name.

    <activity android:name="com.amolg.flutterbarcodescanner.BarcodeCaptureActivity" />

### iOS

To use on iOS,open the Xcode and add camera usage description in Info.plist

    <key>NSCameraUsageDescription</key>
    <string>Camera permission is required for barcode scanning.</string>

## How to use ?

1. You need to import the package first.

    `import 'package:flutter_barcode_scanner/flutter_barcode_scanner.dart';`
    
2. Then use the `scanBarcode` method to access barcode scanning.
    
    `String barcodeScanRes = await FlutterBarcodeScanner.scanBarcode(COLOR_CODE);`

Here you can pass color which is the line color in barcode overlay.
