FROM ubuntu:latest
RUN apt-get update 
    # Устанавливаем Java Development Kit (OpenJDK)
RUN apt-get install -y openjdk-8-jdk 
    # Устанавливаем Apache Ant
RUN apt-get install -y ant

# Настройка переменных среды JAVA_HOME и ANT_HOME
#ENV /usr/lib/jvm/java-8-openjdk-amd64
#ENV ANT_HOME=/usr/share/ant 
# Стандартный путь установки Ant в debian-based дистрибутивах
#ENV PATH="${PATH}:${JAVA_HOME}/bin:${ANT_HOME}/bin"

# Проверяем установку
RUN java -version && ant -version

WORKDIR /app/mytest2
COPY build.xml /app/mytest2/
COPY src/* /app/mytest2/src/
COPY lib/* /app/mytest2/lib/

RUN ant

CMD [ "java", "-cp", "Test2.jar:/app/mytest2/lib/Test1.jar:/app/mytest2/build", "Test2"]


