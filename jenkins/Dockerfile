FROM jenkins/jenkins:lts-jdk17

# Cambia a root si necesitas instalar paquetes extra
USER root
# Ejemplo: instalar git
RUN apt-get update && apt-get install -y git && rm -rf /var/lib/apt/lists/*

# Volver al usuario jenkins
USER jenkins

# Instalar plugins desde lista (opcional)
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN jenkins-plugin-cli --plugin-file /usr/share/jenkins/ref/plugins.txt
