FROM openjdk:11

ADD service-quick-hello-1.0-SNAPSHOT.jar service-quick-hello-1.0-SNAPSHOT.jar

ADD example.yml example.yml

CMD java -jar service-quick-hello-1.0-SNAPSHOT.jar server example.yml

EXPOSE 8080
