# Utilizar una imagen base de Ubuntu 16.10
FROM ubuntu:16.10

# Reemplazar la URL del repositorio en sources.list
RUN sed -i 's/http:\/\/archive.ubuntu.com\/ubuntu/http:\/\/old-releases.ubuntu.com\/ubuntu/' /etc/apt/sources.list && \
    sed -i '/^deb.*security.ubuntu.com/s/^/#/' /etc/apt/sources.list && \
    apt-get update && \
    apt-get install -y sudo net-tools openssh-client 