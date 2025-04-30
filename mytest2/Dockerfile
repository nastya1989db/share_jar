FROM ubuntu:latest
RUN apt-get update 
    # Устанавливаем Java Development Kit (OpenJDK)
RUN apt-get install -y openjdk-8-jdk 
    # Устанавливаем Apache Ant
RUN apt-get install -y ant

# Настройка переменных среды JAVA_HOME и ANT_HOME
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
ENV PATH="${PATH}:${JAVA_HOME}/bin:/usr/share/ant/bin"

# Проверяем установку
RUN java -version && ant -version

CMD ["bash"]
#WORKDIR /app/mytest2
#COPY build.xml /app/mytest2/
#COPY src/* /app/mytest2/src/
#COPY lib/* /app/mytest2/lib/




