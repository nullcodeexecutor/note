
+ mvn clean install -pl pom.xml
+ mvn clean && mvn compile && mvn install -Dmaven.test.skip=true
+ mvn clean && mvn dependency:copy-dependencies && mvn package -Dmaven.test.skip=true -Pproduction 
+ mvn dependency:analyze
+ mvn dependency:tree