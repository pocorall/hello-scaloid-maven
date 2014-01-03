# Hello Scaloid for maven

This is a template project that can be a starting point of a new [Scaloid](https://github.com/pocorall/scaloid) project. 

This contains minimum code as possible; therefore easy to run, examine and extend.

Prerequisites
-------------
* Maven 3
* Android SDK
  - Both SDK Level 8 and the most recent version should be installed.

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
Deploy to an Android virtual device (AVD):

    $ mvn android:deploy

Using an IDE
------------
You can use Maven to generate project files for Eclipse or IDEA:

    $ mvn eclipse:eclipse
    $ mvn idea:idea

Troubleshooting
---------------

#### Error `ANDROID-904-002: Found aidl files: Count = 0`
The environment variable `ANDROID_HOME` is incorrect.


Further Reading
---------------
- [Scaloid](https://github.com/pocorall/scaloid)
- [Scaloid APIdemos](https://github.com/pocorall/scaloid-apidemos)
- [Android Maven Plugin](http://code.google.com/p/maven-android-plugin/)


Origin
------
This project is forked from [android-scala-test](https://github.com/rohansingh/android-scala-test). Thanks [rohansingh](https://github.com/rohansingh)!
