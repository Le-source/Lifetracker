# Life Tracker

# How to import the Project as Android App

https://www.jetbrains.com/help/idea/importing-an-existing-android-project.html

File > New > Project from Existing Sources > Choose Folder where this Project is contained > Import project from external model
> Gradle > Use Gradle Wrapper and and and > Finish

The Configure build step will fail because we have to specify what the location of the Android SDK is. Add a local.properties file:

https://stackoverflow.com/questions/27620262/sdk-location-not-found-define-location-with-sdk-dir-in-the-local-properties-fil

Click on Add Configuration > + sign upper left corner > Android App > name: app / Module: app > Apply

If it says "Please select Android SDK", go to
Tools > Android > Sync Project with Gradle Files

# How to run the App on an Emulator

# Gradle