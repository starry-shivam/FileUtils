# FileUtils
Small library to get file path from most kinds of content Uri in Android.
For example: internal/external storage Uri, Google Drive uri, Google Photos Uri, WhatsApp files Uri and more!

[![](https://www.jitpack.io/v/starry-shivam/FileUtils.svg)](https://www.jitpack.io/#starry-shivam/FileUtils)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

### Getting Started
**Step 1.** Add the JitPack repository to your build file
```gradle
allprojects {
    repositories {
        ...
        maven { url 'https://www.jitpack.io' }
    }
 }
  ```
**Step 2.** Add the dependency
```gradle
dependencies {
    implementation 'com.github.starry-shivam:FileUtils:1.0.0'
}
```
Thats it!

### Example Usage
```kotlin
val fileUri = Uri.parse("content://com.android.externalstorage.documents/document/primary%3ARYO%20YAMADA%20WALLPAPER.jpg")
val filePath = FileUtils(context).getPath(fileUri)
Log.d(TAG, "File path: $filePath")
```
will output:
```
D/MainActivity: File path: /storage/emulated/0/RYO YAMADA WALLPAPER.jpg
```

### License
```
MIT License

Copyright (c) 2023 Stɑrry Shivɑm

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
