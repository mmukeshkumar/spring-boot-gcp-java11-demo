Description:
Demo maven project showcasing Spring boot, Spring cloud GCP, GAE Standard, Clould Pub/Sub and Cloud Spanner Database, its deployable to gae-standard

step 1: Install Java 8 JDK and Maven 3 or above
Build: ./mvnw clean install
step 2: java -jar target/spring-boot-gcp-java11-demo-0.0.1-SNAPSHOT.jar
OR import project into Intellij IDE and run the GcpDemoApplication as a Java application
Step 3:
List REST endpoints
curl -i http://localhost:8080
List orders
curl -i http://localhost:8080/orders

Step 4:
Post a greeting message to the Cloud PUb/SUB
curl -i -XPOST http://localhost:8080/greet/goodday

Deploying to google app engine:
./mvnw appengine:deploy -Dapp.deploy.projectId=[YOUR_PROJECT_ID]



