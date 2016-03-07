# Gstreamer example updated to Android Studio 2.0 beta 6
Here is a new version of the tutorial-5 example using a more up to date toolset. This compiles on OSX 10.10.5

1. Download and install the 1.7.90 (https://gstreamer.freedesktop.org/data/pkg/android/) gstreamer Android package
2. Download and install the Android NDK release r10e
3. Grab Android Studio 2.0 beta 6 and open project
4. Set ndk.dir in Gradle local.properties to the r10e installation
5. Point GSTREAMER_ROOT_ANDROID in Android.mk to the gstreamer installation
6. Run

# GStreamer 1.0 example "tutorial 5" for Android Studio with Gradle

Here is working tutorial-5 example. Code originally came from [Sebastian Dröge (slomo) blog](https://coaxion.net).
To run this code on Android Studio, you have to make Gradle compile NDK code using .mk files
originally made for Eclipse.

Gradle code is made mainly thanks to [Gaku Ueada's blog post](http://blog.gaku.net/ndk/). For some
more details look at `app/build.gradle`.

## How to

1. Open project with Android Studio (tested with 1.0 version)
2. Edit `local.properties` - set SDK and NDK paths
3. Download GStreamer Android library from [freedesktop page](http://gstreamer.freedesktop.org/data/pkg/android/).
 I was using [1.4.4 version from 08-Nov-2014 10:03](http://gstreamer.freedesktop.org/data/pkg/android/1.4.4/)
 (gstreamer-1.0-android-arm-release-1.4.4.tar.bz2). Extract everything somewhere.
4. Edit `src/main/jni/Android.mk` file and set `GSTREAMER_ROOT_ANDROID` to the path
where your extracted Gstreamer library (step 3).
5. Run
