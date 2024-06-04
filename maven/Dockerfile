FROM openjdk:20

ENV MAVEN_HOME /usr/share/maven
ENV MAVEN_VERSION 3.9.2
ENV PATH SMAVEN_HOME/bin:$PATH

RUN apt-get update \
    && apt-get install -y maven \
    && rm -rf /var/Lib/apt/lsts/* \

COPY . /usr/src/app

WORKDIR /usr/src/app

RUN mvn clean install
CMD ["java", "-jar", "target/myapp.jar"]