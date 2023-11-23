FROM ubuntu:20.10

# Cambiar la URL de los repositorios
RUN sed -i 's/http:\/\/archive.ubuntu.com\/ubuntu/http:\/\/old-releases.ubuntu.com\/ubuntu/' /etc/apt/sources.list
RUN sed -i '/^deb.*security.ubuntu.com/s/^/#/' /etc/apt/sources.list

# Actualizar repositorios e instalar herramientas
RUN apt update && apt install -y sudo net-tools openssh-client openssh-server tshark

# Configurar el usuario "test" con contraseña "test"
RUN useradd -m test && echo "test:test" | chpasswd && adduser test sudo

# Exponer el puerto 22 para SSH
EXPOSE 22
