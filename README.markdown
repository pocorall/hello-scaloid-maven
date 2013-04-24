# Hello Scaloid for maven

This is a sample project demonstrates [Scaloid library](https://github.com/pocorall/scaloid) for Android development.

Prerequisites
-------------
* Maven 3
* Android SDK

Build
-----
You can build using Maven:

    $ mvn clean install

This will compile the project and generate an APK. The generated APK is
signed with the Android debug certificate. To generate a zip-aligned APK
that is signed with an actual certificate, use:

    $ mvn clean install -Prelease

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

Once the project files are generated, your IDE should be able to open
the project. Depending on your IDE's configuration, it may not be able
to build the project. You can always build using the Maven command line
as detailed in this readme.

Origin
------
This project is forked from [android-scala-test](https://github.com/rohansingh/android-scala-test). Thanks [rohansingh](https://github.com/rohansingh)!

Further Reading
---------------
- [Android Maven Plugin](http://code.google.com/p/maven-android-plugin/)
