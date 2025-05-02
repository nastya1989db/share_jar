FROM ubuntu:latest
RUN apt-get update 
    # \u0423\u0441\u0442\u0430\u043d\u0430\u0432\u043b\u0438\u0432\u0430\u0435\u043c Java Development Kit (OpenJDK)
RUN apt-get install -y openjdk-21-jdk 
    # \u0423\u0441\u0442\u0430\u043d\u0430\u0432\u043b\u0438\u0432\u0430\u0435\u043c Apache Ant
RUN apt-get install -y ant

# \u041d\u0430\u0441\u0442\u0440\u043e\u0439\u043a\u0430 \u043f\u0435\u0440\u0435\u043c\u0435\u043d\u043d\u044b\u0445 \u0441\u0440\u0435\u0434\u044b JAVA_HOME \u0438 ANT_HOME
#ENV /usr/lib/jvm/java-8-openjdk-amd64
#ENV ANT_HOME=/usr/share/ant 
# \u0421\u0442\u0430\u043d\u0434\u0430\u0440\u0442\u043d\u044b\u0439 \u043f\u0443\u0442\u044c \u0443\u0441\u0442\u0430\u043d\u043e\u0432\u043a\u0438 Ant \u0432 debian-based \u0434\u0438\u0441\u0442\u0440\u0438\u0431\u0443\u0442\u0438\u0432\u0430\u0445
#ENV PATH="${PATH}:${JAVA_HOME}/bin:${ANT_HOME}/bin"

# \u041f\u0440\u043e\u0432\u0435\u0440\u044f\u0435\u043c \u0443\u0441\u0442\u0430\u043d\u043e\u0432\u043a\u0443
RUN java -version && ant -version

WORKDIR /app/mytest2
COPY build.xml /app/mytest2/
COPY src/* /app/mytest2/src/
COPY lib/* /app/mytest2/lib/

RUN ant
#CMD ["bash"]
CMD [ "java", "-cp", "Test2.jar:/app/mytest2/lib/Test1.jar:/app/mytest2/build", "Test2"]