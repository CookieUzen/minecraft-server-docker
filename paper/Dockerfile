# Use Temurin JRE
FROM eclipse-temurin:21

# Setting up template
RUN mkdir /opt/paper-temp
WORKDIR /opt/paper-temp
COPY start.sh .

RUN curl -o server.jar "https://api.papermc.io/v2/projects/paper/versions/1.21.1/builds/68/downloads/paper-1.21.1-68.jar"
RUN echo "eula=true" > eula.txt

# Run Server
RUN mkdir /opt/paper
WORKDIR /opt/paper

CMD cp -n /opt/paper-temp/start.sh . && bash start.sh
