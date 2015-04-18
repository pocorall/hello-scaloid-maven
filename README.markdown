# Hello Scaloid for maven

This is a template project that can be a starting point of a new [Scaloid](https://github.com/pocorall/scaloid) project. 

This contains minimum code as possible; therefore easy to run, examine and extend.

Prerequisites
-------------
* Maven 3.2 or above
* Android SDK Level 16 or above
 - Level 16 is required for building, while this app retains runtime compatibility from API Level 10. Please refer to `minSdkVersion` property in `AndroidManifest.xml`
 
Build
-----
You can build using Maven:

    $ mvn clean package

This will compile the project and generate an APK. The generated APK is
signed with the Android debug certificate. To generate a zip-aligned APK
that is signed with an actual certificate, use:

    $ mvn clean package -Prelease

The configuration for which certificate to use is in pom.xml.

Run
---
Deploy to an Android virtual device (AVD) and run:

    $ mvn android:deploy android:run

Using an IDE
------------
You can use Maven to generate project files for Eclipse or IDEA:

    $ mvn eclipse:eclipse
    $ mvn idea:idea
    
We do not recommend to use IDE's own Android build system, because proguard settings are complicated.
Use Maven to build and deploy the project.

Troubleshooting
---------------

#### Error `ANDROID-904-002: Found aidl files: Count = 0`
The environment variable `ANDROID_HOME` is incorrect.

Is the build too slow?
----------------------
This maven project works completely. But long build time would matter, which usually takes more than 40 seconds.
We recommend to [build your project with sbt](https://github.com/pocorall/hello-scaloid-sbt), which enables incremental build.
This usually takes only several seconds.

Further Reading
---------------
- [Scaloid](https://github.com/pocorall/scaloid)
- [Scaloid APIdemos](https://github.com/pocorall/scaloid-apidemos)
- [Android Maven Plugin](https://github.com/simpligility/android-maven-plugin)


Origin
------
This project is forked from [android-scala-test](https://github.com/rohansingh/android-scala-test). Thanks [rohansingh](https://github.com/rohansingh)!
