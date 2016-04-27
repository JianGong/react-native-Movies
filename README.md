# Movies app
Facebook Movies:[https://github.com/facebook/react-native/tree/master/Examples/Movies](https://github.com/facebook/react-native/tree/master/Examples/Movies)

豆瓣电影：

![1](http://ww4.sinaimg.cn/large/8bd0decfgw1f3be4aqj79j208w0fsmy8.jpg)
![2](http://ww3.sinaimg.cn/large/8bd0decfgw1f3be59mcjfj208w0fs0tp.jpg)

## Running this app

### Running on iOS

Mac OS and Xcode are required.

- Open `Movies/Movies.xcodeproj` in Xcode
- Hit the Run button

See [Running on device](https://facebook.github.io/react-native/docs/running-on-device-ios.html) if you want to use a physical device.

### Running on Android

You'll need to have all the [prerequisites](https://github.com/facebook/react-native/tree/master/ReactAndroid#prerequisites) (SDK, NDK) for Building React Native installed.

Start an Android emulator ([Genymotion](https://www.genymotion.com) is recommended).

    cd react-native
    ./gradlew :Examples:Movies:android:app:installDebug
    ./packager/packager.sh

_Note: Building for the first time can take a while._

Open the Movies app in your emulator.

See [Running on Device](https://facebook.github.io/react-native/docs/running-on-device-android.html) in case you want to use a physical device.

### Running with Buck

Follow the same setup as running with gradle.

Install Buck from [here](https://buckbuild.com/setup/install.html).

Run the following commands from the react-native folder:

    ./gradlew :ReactAndroid:packageReactNdkLibsForBuck
    buck fetch movies
    buck install -r movies
    ./packager/packager.sh

_Note: The native libs are still built using gradle. Full build with buck is coming soon(tm)._

## Built from source

Building the app on both iOS and Android means building the React Native framework from source. This way you're running the latest native and JS code the way you see it in your clone of the github repo.

This is different from apps created using `react-native init` which have a dependency on a specific version of React Native JS and native code, declared in a `package.json` file (and `build.gradle` for Android apps).
