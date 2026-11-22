
# Guía de despliegue

## 1. Requisitos previos

- VMware Workstation.
- Rocky Linux 9.8.
- Conexión a Internet.
- Usuario con permisos administrativos.

## 2. Preparación del servidor

Ejecutamos el script de preparación del sistema.

```bash
chmod +x 01_preparar_servidor.sh
./01_preparar_servidor.sh
```

## 3. Instalación de Docker

Automatizamos la instalación de Docker y Docker Compose.

```bash
chmod +x 02_instalar_docker.sh
./02_instalar_docker.sh
```

## 4. Despliegue de BookStack y MariaDB

```bash
chmod +x 03_instalar_bookstack.sh
./03_instalar_bookstack.sh
```

Accedemos a http://192.168.63.141:6875.

## 5. Despliegue de Wiki.js y PostgreSQL

```bash
chmod +x 04_instalar_wikijs.sh
./04_instalar_wikijs.sh
```

Accedemos a http://192.168.63.141:3000.

## 6. Comprobaciones finales

```bash
chmod +x 05_comprobar_servicios.sh
./05_comprobar_servicios.sh
```

Comprobamos también los recursos de Docker:

```bash
sudo docker ps
sudo docker volume ls
sudo docker network ls
```

## 7. Resultados obtenidos

- Servicio Docker activo.
- Cuatro contenedores en ejecución.
- Volúmenes persistentes disponibles.
- BookStack: HTTP 200.
- Wiki.js: HTTP 200.

## 8. Seguridad

Utilizamos credenciales independientes y evitamos
publicar archivos .env con información confidencial.
