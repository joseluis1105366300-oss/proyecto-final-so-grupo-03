


# Ficha de verificación de versiones - Grupo 03

## Proyecto Final de Sistemas Operativos
**Universidad del Valle - Semestre 2 de 2026**

**Integrantes:**
- José Luis Valencia Cano
- Yahiarón Fernández Fernández

## 1. Fedora Workstation - Máquina gráfica

| Pregunta | Respuesta | Fuente oficial |
|---|---|---|
| Versión y fecha | Fedora Workstation 45. Lanzamiento: 3 de noviembre de 2026. | https://fedoraproject.org/workstation/ |
| Actualizaciones de seguridad | Fin de soporte previsto: 8 de diciembre de 2027. | https://fedoraproject.org/wiki/Releases |
| Requisitos y VirtualBox | Se utilizará VirtualBox 7.x, 2 CPU, 25 GB de disco y entre 2 y 4 GB de RAM, según los requisitos del proyecto. | https://fedoraproject.org/workstation/ |
| Particionado manual | Sí. El instalador Anaconda permite configurar particiones manualmente. | https://docs.fedoraproject.org/ |
| Guía oficial Docker Engine | Sí. Docker tiene instrucciones oficiales para Fedora 45. | https://docs.docker.com/engine/install/fedora/ |
| Imagen base Docker | Existe una imagen oficial de Fedora en Docker Hub. | https://hub.docker.com/_/fedora |

## 2. Ubuntu Server - Máquina de consola

| Pregunta | Respuesta | Fuente oficial |
|---|---|---|
| Versión y fecha | Ubuntu Server 26.04.1 LTS. Lanzamiento: 27 de agosto de 2026. | https://ubuntu.com/download/server |
| Actualizaciones de seguridad | Soporte estándar hasta mayo de 2031. | https://ubuntu.com/about/release-cycle |
| Requisitos y VirtualBox | Se utilizará VirtualBox 7.x, 2 CPU, 25 GB de disco y 2 GB de RAM inicialmente. | https://ubuntu.com/server/docs/ |
| Particionado manual | Sí. El instalador permite configurar manualmente el almacenamiento y las particiones. | https://ubuntu.com/server/docs/installation/ |
| Guía oficial Docker Engine | Sí. Existe una guía oficial para instalar Docker Engine en Ubuntu. | https://docs.docker.com/engine/install/ubuntu/ |
| Imagen base Docker | Existe una imagen oficial de Ubuntu en Docker Hub. | https://hub.docker.com/_/ubuntu |

## 3. Fedora - Imagen base Docker

| Pregunta | Respuesta | Fuente oficial |
|---|---|---|
| Versión y fecha | Fedora 45. Lanzamiento: 3 de noviembre de 2026. | https://fedoraproject.org/ |
| Actualizaciones de seguridad | Fin de soporte previsto: 8 de diciembre de 2027. | https://fedoraproject.org/wiki/Releases |
| Requisitos y VirtualBox | No aplica como máquina virtual. Se utilizará como imagen base de Docker. | https://hub.docker.com/_/fedora |
| Particionado manual | No aplica. Los contenedores no requieren particionado manual durante su construcción. | https://docs.docker.com/build/ |
| Guía oficial Docker Engine | Sí. Docker dispone de instrucciones para instalar Docker Engine en Fedora. | https://docs.docker.com/engine/install/fedora/ |
| Imagen base Docker | Sí. Imagen oficial Fedora disponible en Docker Hub. | https://hub.docker.com/_/fedora |

## 4. Conclusión

El Grupo 03 utilizará Fedora Workstation como sistema operativo gráfico, Ubuntu Server como sistema operativo de consola y Fedora como imagen base para construir el contenedor Docker.

Las versiones seleccionadas se documentarán y verificarán mediante las fuentes oficiales de cada distribución y de Docker.
