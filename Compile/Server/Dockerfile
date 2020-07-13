FROM java:ai

# FROM maven:3.6.3-openjdk-14-slim

# ARG source

# COPY $source /src

# RUN cd /src && mvn compile

# RUN cd /src && mvn clean package

# RUN mv /src/target/server-*-SNAPSHOT-jar-with-dependencies.jar /server.jar

# RUN rm -rf /src

COPY server.jar /server.jar

RUN echo "java -jar /server.jar --config=server.conf 2>&1 | tee /debug.log" > run.sh

RUN chmod +x run.sh

CMD ["bash", "run.sh"]
