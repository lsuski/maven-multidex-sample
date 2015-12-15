# maven-multidex-sample

This sample project shows how to impelent android-maven-plugin multi-dex mechanism.

Procedure:
1) Flag minimal-main-dex is set to true to ensure that only classes listed in MainDexList.txt come in classes.dex, 
other classes including activities come to secondary dexes.

2) Install multidex.jar in local m2 (or any other) repository with following maven properties

```xml
<groupId>com.android.support</groupId>
<artifactId>multidex</artifactId>
<version>20</version>
```
3) Import that dependency in your pom.xml

4) Extend your Application class to MultiDexApplication and specify that name in your Manifest.xml in <application> tag:
```xml
<application
        android:allowBackup="true"
        android:name="com.sample.multidex.MultiDexApplication">
</application>
```

Proguard is enabled without shrinking.