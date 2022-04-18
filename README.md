# Java Library Scanner
A utility to scan a Linux file system for specific versions of Java libraries, like Log4j or Spring Framework. The scanner looks for jar- and war-files, open them and look for Java libraries by matching file names using regular expressions.

The scanner will find the following libraries:
Log4j ():
* Log4j Core 2.0 to 2.17.0
Spring:
* Spring Core 5.3.0 to 5.3.17
* Spring Core 5.2.0 to 5.2.19
* Older releases of Spring Core

The script can be run using the following command:

```
source <(curl -s https://raw.githubusercontent.com/bvboe/java-library-scanner/main/find-java-libraries.sh)
```

The output will look as follows:
```
$ source <(curl -s https://raw.githubusercontent.com/bvboe/java-library-scanner/main/find-java-libraries.sh)

log4j-api-2.17.0.jar in ./testfiles/bad-versions/log4j-api-2.17.0.jar
spring-core-5.3.1.jar in ./testfiles/bad-versions/spring-core-5.3.1.jar
spring-core-5.1.1.jar in ./testfiles/bad-versions/spring-core-5.1.1.jar
spring-core-4.0.1.jar in ./testfiles/bad-versions/spring-core-4.0.1.jar
log4j-api-2.14.1.jar in ./testfiles/bad-versions/log4j-api-2.14.1.jar
spring-core-5.0.1.jar in ./testfiles/bad-versions/spring-core-5.0.1.jar
log4j-api-2.0.jar in ./testfiles/bad-versions/log4j-api-2.0.jar
spring-core-5.2.19.jar in ./testfiles/bad-versions/spring-core-5.2.19.jar
spring-core-5.3.17.jar in ./testfiles/bad-versions/spring-core-5.3.17.jar
spring-core-5.3.10.jar in ./testfiles/bad-versions/spring-core-5.3.10.jar
spring-core-5.3.16.jar in ./testjar/target/testjar-0.0.1-SNAPSHOT.jar
log4j-api-2.14.1.jar in ./testwar/target/testwar-0.0.1-SNAPSHOT.war
spring-core-5.3.13.jar in ./testwar/target/testwar-0.0.1-SNAPSHOT.war
log4j-api-2.14.1.jar in ./testwar/target/testwar-0.0.1-SNAPSHOT/WEB-INF/lib/log4j-api-2.14.1.jar
spring-core-5.3.13.jar in ./testwar/target/testwar-0.0.1-SNAPSHOT/WEB-INF/lib/spring-core-5.3.13.jar
```
