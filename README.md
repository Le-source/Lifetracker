# Life Tracker

Life Tracker is an Android Application that will facilitate keeping score of your daily habits and will try to make you embrace and enforce your strengths. It is written in Kotlin.

# How to import the project as Android App

Clone this repository. Open an instance of [IntelliJ IDEA](https://www.jetbrains.com/idea/download/) or [Android Studio](https://developer.android.com/studio). Make sure that you have an Android SDK installed. The easiest way to achieve this is to install this in IDEA / Studio directly by navigating to

> File > Project > Android

If you have no Android SDK version installed, here you will be asked to download and install it.

In order to import the project as an Android App, we first have to [Import it from Existing Sources](https://www.jetbrains.com/help/idea/importing-an-existing-android-project.html
) like this:

> File > New > Project from Existing Sources > Select Folder where this Project is located > Import project from external model > Gradle > Use Gradle Wrapper and and and > Finish

Gradle will start building. The Configure build step will fail because we have to specify what the location of the Android SDK is. Add a local.properties file depending on which Operating System you use following this [Stack Overflow Answer](https://stackoverflow.com/a/48155800).

If there are still issues like symbols not being resolved, try to
> File > Invalid Caches/Restart

# How to run the App on an Emulator

Add a run configuration by clicking on *Edit Configuration* (next to the Run button in upper right corner of your IDE). 
> Click on '+' sign in the upper left corner > Android App > name: app / Module: app > Apply

If it says *Please select Android SDK* after trying to run the App, go to
> Tools > Android > Sync Project with Gradle Files

Now, it's time to create a device where Android will be emulated. Go to 
> Tools > Android > Create Virtual Device

Choose a device and Android version of your liking. Just be aware of the recommendations shown in a red box on the right hand side. Best results will be achieved when no red box appears. Following issues can arise:

*Issues on Windows with non-Intel-CPUs*:

When starting the Emulator the screen can stay black. This can be because you cannot use _x64_ or _x86_ based Android versions. Look for Android versions that are based on _armeabi-v7a_ or _armeabi-v8a_.

*Issues on Ubuntu 18.04:*

> /dev/kvm device: permission denied

This [blogpost](https://blog.chirathr.com/android/ubuntu/2018/08/13/fix-avd-error-ubuntu-18-04/) is a nice guide how to set the permission for your current user.

____

Keep in mind that running the Android Emulator can be slow and take some time. It will use as much RAM as you allocated. Once it runs, you can turn on QuickBoot and Snapshots to skip booting time. 

When the Emulator is running, you can run your App by clicking the green triangle (Run button). If everything is configured correctly, it will try to install the App onto your emulated device. You can find it in the Menu of the emulated device and open it.

Feel free to add any solutions to issues to this documentation. Have fun!