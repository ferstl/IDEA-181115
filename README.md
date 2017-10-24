# IDEA-181115
*- Reproduce Issue IDEA-181115*

### Build in IntelliJ
IntelliJ 2017.2.5 generates these type of error messages when building the project:

![Error Messages](/doc/error-messages.png)

### Build with Maven
```
git clone git@github.com:ferstl/IDEA-181115.git
cd IDEA-181115
mvn clean install
```

### Build with javac

The maven-compiler-plugin creates a similar command line than the one below. To run `javac` you might need to adjust the three variables `PROJECT`, `MAVEN_REPO` and `JAVA_HOME`.

```
#Adjust if required
PROJECT="."
MAVEN_REPO="$HOME/.m2/repository"

$JAVA_HOME/bin/javac \
-d $PROJECT/target/classes \
-classpath "\
$PROJECT/target/classes;\
$MAVEN_REPO/com/vaadin/vaadin-server/7.7.0/vaadin-server-7.7.0.jar;\
$MAVEN_REPO/com/vaadin/vaadin-sass-compiler/0.9.13/vaadin-sass-compiler-0.9.13.jar;\
$MAVEN_REPO/org/w3c/css/sac/1.3/sac-1.3.jar;\
$MAVEN_REPO/com/vaadin/external/flute/flute/1.3.0.gg2/flute-1.3.0.gg2.jar;\
$MAVEN_REPO/com/yahoo/platform/yui/yuicompressor/2.4.8/yuicompressor-2.4.8.jar;\
$MAVEN_REPO/rhino/js/1.7R2/js-1.7R2.jar;\
$MAVEN_REPO/com/vaadin/vaadin-shared/7.7.0/vaadin-shared-7.7.0.jar;\
$MAVEN_REPO/org/jsoup/jsoup/1.8.3/jsoup-1.8.3.jar" \
-sourcepath "\
$PROJECT/src/main/java;\
$PROJECT/target/generated-sources/annotations;" \
-s $PROJECT/target/generated-sources/annotations \
-g \
-target 9 \
-source 9 \
-encoding UTF-8 \
src/main/java/com/github/ferstl/test/Test.java
```
