[![Build Status](https://app.travis-ci.com/Huluvu424242/informally-jmod-hub.svg?branch=master)](https://app.travis-ci.com/Huluvu424242/informally-jmod-hub)

# !!!! D A N G E R - THIS is NOT an OFFICIALLY  REPO !!!!

**Only to use if you know what you are doing !!!**

Check the build scripts "build.xml" for correct deps before usage !!!

## There are jmod s based on manually written module-info.java files.  

```shell
# Herstellung der jmod Dateien für auto module
#
# Gezeigt am Beispiel von commons-lang
#
jdeps --generate-open-module ./jdeps ~/.m2/repository/commons-lang/commons-lang/2.6/commons-lang-2.6.jar
jdeps --generate-module-info ./jdeps ~/.m2/repository/commons-lang/commons-lang/2.6/commons-lang-2.6.jar
unzip  ~/.m2/repository/commons-lang/commons-lang/2.6/commons-lang-2.6.jar -d ./jdeps/commons.lang/classes
javac -d ./jdeps/commons.lang/classes ./jdeps/commons.lang/module-info.java
jmod create --class-path ./jdeps/commons.lang/classes src/jmods/commons-lang-2.6.jmod
```
