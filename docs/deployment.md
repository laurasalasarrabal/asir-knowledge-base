# Guía de despliegue

## 1. Introducción

En este documento describimos el procedimiento previsto
para desplegar ASIR Knowledge Base.

## 2. Requisitos previos

- VMware Workstation.
- Rocky Linux 9.
- 2 procesadores virtuales.
- 4 GB de memoria RAM como mínimo.
- 40 GB de almacenamiento.
- Conexión a Internet.
- Usuario con permisos de administración.

## 3. Preparación del servidor

Prepararemos una máquina virtual con Rocky Linux 9
y actualizaremos los paquetes del sistema.

```bash
sudo dnf update -y
```

## 4. Instalación de Docker

Instalaremos Docker y Docker Compose para gestionar
los contenedores de nuestro proyecto.

## 5. Despliegue de BookStack

Desplegaremos BookStack junto con una base de datos
MariaDB mediante Docker Compose.

## 6. Despliegue de Wiki.js

Desplegaremos Wiki.js junto con una base de datos
PostgreSQL mediante Docker Compose.

## 7. Comprobación de los servicios

Comprobaremos el estado de los contenedores mediante:

```bash
docker ps
```

## 8. Seguridad

- Utilizaremos contraseñas seguras.
- Protegemos las credenciales mediante variables de entorno.
- Configuraremos almacenamiento persistente.
- Restringiremos los puertos publicados.

## 9. Estado del despliegue

Pendiente de ejecución y validación durante el
apartado B.2 de la práctica.
