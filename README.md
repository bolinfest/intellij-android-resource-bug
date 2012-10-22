intellij-android-resource-bug
=============================

This is a project that demonstrates a bug in IntelliJ.

If you try building this project in IntelliJ using "Make Project,"
then you will get the following	error:

[app] java.util.zip.ZipException: duplicate entry: AndroidManifest.xml

IntelliJ should be smart enough to include only the AndroidManifest.xml
associated with the app.iml module. (Or if it is not smart enough to
do that automatically, then there should be a way to exclude it
explicitly.)

I believe this bug has to do with a bad interaction when using
a sourceFolder with a packagePrefix in an Android library project.
