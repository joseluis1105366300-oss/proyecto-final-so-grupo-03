# Ficha de verificación de versiones - Grupo 03

**Proyecto:** Proyecto Final de Sistemas Operativos  
**Curso:** Semestre 2 - 2026  
**Integrantes:** José Luis Valencia Cano y Yahiarón Fernández Fernández  
**Fecha de consulta de fuentes:** 19 de noviembre de 2026

> El documento del curso pide verificar seis aspectos para cada distribución: versión y fecha de lanzamiento; fin de actualizaciones de seguridad; requisitos de hardware y funcionamiento en VirtualBox; particionado manual; guía oficial de Docker Engine; e imagen base en Docker Hub. Revisen las fuentes y completen cualquier dato que dependa de la configuración real de sus máquinas.

## 1. Fedora Workstation - VM gráfica

| Aspecto solicitado | Dato verificado / por confirmar | Fuente |
|---|---|---|
| Versión elegida y fecha de lanzamiento | Fedora Workstation 45. Fecha de lanzamiento publicada: 3 de noviembre de 2026. | https://fedoraproject.org/workstation/download/ |
| Hasta cuándo recibe actualizaciones de seguridad | La información de Fedora 45 indica EOL previsto para el 8 de diciembre de 2027. Verificar nuevamente el calendario oficial al instalar. | https://packages.fedoraproject.org/pkgs/fedora-release/fedora-release-workstation/fedora-45-updates.html |
| Requisitos de hardware y VirtualBox | Fedora recomienda 40 GB de disco y 4 GB de RAM para la mayoría de variantes. El curso establece VirtualBox 7.x, 2 CPU, disco virtual de 25 GB y entre 2 y 4 GB de RAM para la VM gráfica. Deben comprobar y documentar si 25 GB permiten completar la instalación; si no, usar los requisitos de la distribución y registrar la diferencia. | https://fedoraproject.org/workstation/download/ ; documento del curso, sección «Requisitos técnicos». |
| ¿Permite particionado manual? | Sí. El instalador Anaconda ofrece configuración personalizada de almacenamiento y asignación de puntos de montaje. Confirmar la opción disponible en el instalador de la ISO descargada. | https://fedoraproject.org/wiki/Changes/Anaconda_Web_UI_Partitioning |
| ¿Existe guía oficial para instalar Docker Engine en esta familia? | Sí. Docker documenta la instalación de Docker Engine en Fedora y lista Fedora 45 entre las versiones mantenidas compatibles. | https://docs.docker.com/engine/install/fedora/ |
| ¿Existe imagen base para Docker? | Sí. Docker Hub publica la imagen oficial `fedora` y muestra la etiqueta `45`. | https://hub.docker.com/_/fedora |

## 2. Ubuntu Server - VM de consola

| Aspecto solicitado | Dato verificado / por confirmar | Fuente |
|---|---|---|
| Versión elegida y fecha de lanzamiento | Ubuntu Server 26.04.1 LTS. Fecha de lanzamiento: 27 de agosto de 2026. Se elige la LTS más reciente, como indica el documento del curso para distribuciones con soporte largo. | https://lists.ubuntu.com/archives/ubuntu-announce/2026-August/000326.html ; https://ubuntu.com/download/server |
| Hasta cuándo recibe actualizaciones de seguridad | Soporte estándar hasta mayo de 2031. Ubuntu Pro puede extender el mantenimiento, sujeto a sus condiciones. | https://wiki.ubuntu.com/Releases |
| Requisitos de hardware y VirtualBox | Ubuntu Server publica 1.5 GB de RAM y 5 GB de disco como mínimos para instalación ISO; recomienda 3 GB de RAM o más y 25 GB de almacenamiento. El curso establece VirtualBox 7.x, 2 CPU, disco de 25 GB y 2 GB de RAM inicialmente (3 GB para Sprint 3). Confirmar el resultado con la versión instalada. | https://ubuntu.com/server/docs/reference/installation/system-requirements/ ; documento del curso, sección «Requisitos técnicos». |
| ¿Permite particionado manual? | Sí. El instalador permite seleccionar «Custom storage layout» y editar las particiones. | https://ubuntu.com/server/docs/installation/ ; https://ubuntu.com/tutorials/install-ubuntu-server |
| ¿Existe guía oficial para instalar Docker Engine en esta familia? | Sí. Docker incluye Ubuntu 26.04 LTS entre las versiones compatibles y publica los pasos para instalar Docker Engine. | https://docs.docker.com/engine/install/ubuntu/ |
| ¿Existe imagen base para Docker? | Docker Hub dispone de la imagen oficial `ubuntu`. No es la imagen asignada al Dockerfile del Grupo 03; la imagen base asignada al grupo es Fedora. | https://hub.docker.com/_/ubuntu |

## 3. Fedora - Imagen base del Dockerfile

| Aspecto solicitado | Dato verificado / por confirmar | Fuente |
|---|---|---|
| Versión elegida y fecha de lanzamiento | Fedora 45. Lanzamiento de Fedora Linux 45: 3 de noviembre de 2026. Para el Dockerfile se propone fijar la etiqueta `fedora:45` en lugar de depender de `latest`. | https://fedoraproject.org/workstation/download/ ; https://fedoramagazine.org/announcing-fedora-linux-45/ |
| Hasta cuándo recibe actualizaciones de seguridad | Fedora 45 tiene EOL previsto para el 8 de diciembre de 2027. Revisar el calendario oficial antes de construir o actualizar la imagen. | https://packages.fedoraproject.org/pkgs/fedora-release/fedora-release-workstation/fedora-45-updates.html |
| Requisitos de hardware y VirtualBox | No aplica como VM independiente: Fedora se usará como imagen base de un contenedor Docker. La ejecución depende de los recursos de la VM anfitriona donde se instale Docker. | https://hub.docker.com/_/fedora |
| ¿Permite particionado manual? | No aplica a la imagen de contenedor. El particionado corresponde al sistema operativo anfitrión/VM, no a la imagen base. | https://docs.docker.com/build/ |
| ¿Existe guía oficial para instalar Docker Engine en esta familia? | Sí. Docker publica una guía oficial para instalar Docker Engine en Fedora 45. Esta guía se aplica al sistema anfitrión Fedora, no a la imagen base del contenedor. | https://docs.docker.com/engine/install/fedora/ |
| ¿Existe imagen base para Docker? | Sí. La imagen oficial `fedora` está publicada en Docker Hub y ofrece la etiqueta `45`. | https://hub.docker.com/_/fedora |

## 4. Verificaciones que debe completar el equipo

- [ ] Confirmar la versión exacta descargada de Fedora Workstation y Ubuntu Server.
- [ ] Registrar la RAM asignada realmente a cada VM en VirtualBox.
- [ ] Comprobar durante la instalación las opciones de particionado manual.
- [ ] Guardar los enlaces oficiales consultados y la fecha de consulta.
- [ ] Si algún requisito de la distribución no coincide con el mínimo del curso, registrar el intento, el resultado y el ajuste aplicado.
- [ ] Comprobar que la etiqueta `fedora:45` siga disponible al construir el Dockerfile.

## 5. Distribuciones asignadas

| Uso | Distribución |
|---|---|
| VM gráfica | Fedora Workstation |
| VM de consola | Ubuntu Server |
| Imagen base del Dockerfile | Fedora |

