Maven creates this command line which works fine when called from `javac` directly:

```
-d $PROJECT\target\classes
-classpath
  $PROJECT\target\classes;
  $MAVEN_REPO\repository\com\vaadin\vaadin-server\7.7.0\vaadin-server-7.7.0.jar;
  $MAVEN_REPO\repository\com\vaadin\vaadin-sass-compiler\0.9.13\vaadin-sass-compiler-0.9.13.jar;
  $MAVEN_REPO\repository\org\w3c\css\sac\1.3\sac-1.3.jar;
  $MAVEN_REPO\repository\com\vaadin\external\flute\flute\1.3.0.gg2\flute-1.3.0.gg2.jar;
  $MAVEN_REPO\repository\com\yahoo\platform\yui\yuicompressor\2.4.8\yuicompressor-2.4.8.jar;
  $MAVEN_REPO\repository\rhino\js\1.7R2\js-1.7R2.jar;
  $MAVEN_REPO\repository\com\vaadin\vaadin-shared\7.7.0\vaadin-shared-7.7.0.jar;
  $MAVEN_REPO\repository\org\jsoup\jsoup\1.8.3\jsoup-1.8.3.jar;
-sourcepath
   $PROJECT\src\main\java;
   $PROJECT\target\generated-sources\annotations;
-s $PROJECT\target\generated-sources\annotations
-g
-target 9
-source 9
-encoding UTF-8
```
