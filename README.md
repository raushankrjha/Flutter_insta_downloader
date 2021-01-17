# Flutter_Insta_Downloader ![GitHub all releases](https://img.shields.io/github/downloads/raushankrjha/Flutter_insta_downloader/total) ![Pub Version](https://img.shields.io/pub/v/flutter_instagram_downloader)

A Flutter Instagram reels downloader & feed,profile downloader.

## Installation

Dart requires the latest version of [Dart](https://www.dartlang.org/). You can download the latest and greatest [here](https://www.dartlang.org/tools/sdk#install).

### 1. Depend on it

Add this to your package's `pubspec.yaml` file:

```yaml
dependencies:
     flutter_instagram_downloader: ^0.0.2
```


#### 2. Install it

You can install packages from the command line:

```bash
$ pub get
```


#### 3. Import it

Now in your Dart code, you can use:

```Dart
import 'package:flutter_instagram_downloader/flutter_instagram_downloader.dart';
```

## Usage
### Get ReelSVideo
 
```dart
FlutterInsta flutterInsta = new FlutterInsta();
var reelsvideos=await flutterInsta.downloadReelsVideos("https://www.instagram.com/reel/CJSlF7onjeU/?igshid=1ju3ngvjn3e8ndev_raushanjha"); //Video URL
```




Print Reels Details or Show in Widgets()
```dart
print("Username : ${reelsvideos._username}");
print("Full Name : ${reelsvideos._fullname}");
print("ProfilePicURL : ${reelsvideos._profilepicurl}");
print("Followers : ${reelsvideos._followers}");
print("isVerified : ${reelsvideos.isVerified.toString()}");
print("_videourl : ${reelsvideos._videourl}");
print("Image URL":${reelsvideos._imgurl}");
print("Caption":${reelsvideos._caption}");
print("Song Name":${reelsvideos._songName}");
print("Artist Name":${reelsvideos._artistName}");
print("Video Duration":${reelsvideos._videoDuration}");
print("VideoView Count":${reelsvideos._videoViewCount}");
```

### Get profile Data
 
```dart
FlutterInsta flutterInsta = new FlutterInsta();
await flutterInsta.getProfileInfo("dev_raushanjha"); //instagram username
```

Print Profile Details or Show in Text()
```dart
print("Username : ${flutterInsta._username}");
print("Full Name : ${flutterInsta._fullname}");
print("ProfilePicURL : ${flutterInsta._profilepicurl}");
print("Followers : ${flutterInsta._followers}");
print("isVerified : ${flutterInsta.isVerified.toString()}");
print("Bio : ${flutterInsta._bio}");
print("Category Name":${flutterInsta._category_name}");
```
### Get PostImageVideo
 
```dart
FlutterInsta flutterInsta = new FlutterInsta();
var post=await flutterInsta.downloadImage("https://www.instagram.com/p/CKHG24Kj_Xy/?igshid=8tu91c0kghf7"); //Image URL
```

Print Feed Details or Show in Widgets()
```dart
print("Username : ${post._username}");
print("Full Name : ${post._fullname}");
print("ProfilePicURL : ${post._profilepicurl}");
print("Followers : ${post._followers}");
print("isVerified : ${post.isVerified.toString()}");
print("Image URL":${post._imgurl}");
print("Caption":${post._caption}");

```

## Tips

You can also use this repo as a template for creating Dart packages, just clone the repo and start hacking :) 