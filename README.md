# Simple java program with maven

## Create project directory

```bash
mkdir Maven_ABC
cd Maven_ABC

execute maven goal- on windows we need ""
mvn archetype:generate "-DgroupId=com.abc.bank" "-DartifactId=ABCBank" "-DarchetypeArtifactId=maven-archetype-quickstart" "-DarchetypeVersion=1.4" "-DinteractiveMode=false"

C:.
├───.vscode
├───docs
├───src
│   ├───main
│   │   └───java
│   │       └───com
│   │           └───abc
    │   └───test-annotations
    ├───maven-archiver
    ├───maven-status
    │   └───maven-compiler-plugin
    │       ├───compile
    │       │   └───default-compile
    │       └───testCompile
    │           └───default-testCompile
    ├───surefire-reports
    └───test-classes
        └───com
            └───abc
                └───bank
```

## Edit pom.xml add manifest specification

```xml
<manifest>
    <addClasspath>true</addClasspath>
    <classpathPrefix>lib/</classpathPrefix>
    <mainClass>com.abc.bank.App</mainClass>
</manifest>
```

## Compile source code and test code and executes Unit Tests

```bash
mvn clean test 
```

## Compile source code and test code and executes Unit Test

mvn clean test 

## Compile source code and test code, executes unit test, if all tests pass, it package compiled code in output archive

```bash
mvn clean package
```

## Compile source/test code, executes unit test, package compiled code and then executes Integration tests

```bash
mvn clean verify
```

## run the app from jar

```bash
C:\Users\..\Maven_ABC\ABCBank>java -jar target\ABCBank-1.0-SNAPSHOT.jar
```
