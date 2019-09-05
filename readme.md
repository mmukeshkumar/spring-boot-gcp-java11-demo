# Description:
Demo Java 11 maven project showcasing Spring boot, Spring cloud GCP, GAE Standard, Clould Pub/Sub and Cloud Spanner Database, its deployable to gae-standard

# Prerequisites 
1. Install Java 11 JDK
2. Set up a project in GCP through https://cloud.google.com/ or gcloud CLI
3. Enable billing

# Building
./mvnw clean install

# Running: 
java -jar target/spring-boot-gcp-java11-demo-0.0.1-SNAPSHOT.jar
OR import project into Intellij IDE and run the GcpDemoApplication as a Java application

# Test:
List REST endpoints
curl -i http://localhost:8080
List orders
curl -i http://localhost:8080/orders

Post a greeting message to the Cloud PUb/SUB
curl -i -XPOST http://localhost:8080/greet/goodday

# Deploying to google app engine:
./mvnw appengine:deploy -Dapp.deploy.projectId=[your-gcp-proeject-name]



