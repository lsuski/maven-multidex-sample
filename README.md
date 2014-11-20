maven-multidex-sample
=====================

This sample project checks android-maven-plugin multi-dex mechanism.
Flag minimal-main-dex is set to true to ensure that only classes listed in MainDexList.txt come in classes.dex, 
other classes including activities come to secondary dexes.
Proguard is enabled without shrinking.

To make it works you have to install multidex.jar in local m2 repository as

```xml
<groupId>com.android.support</groupId>
<artifactId>multidex</artifactId>
<version>20</version>
