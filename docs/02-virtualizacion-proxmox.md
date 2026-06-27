# Capa de Virtualización: Proxmox VE

Para la administración de recursos y despliegue de los distintos servicios de la red, se implementó **Proxmox Virtual Environment (VE)**. Se eligió esta plataforma por ser una solución *bare-metal* de grado empresarial, open-source, y por su excelente soporte tanto para máquinas virtuales (KVM) como para contenedores ligeros (LXC).

## Proceso de Instalación y Configuración Base

### 1. Despliegue del Sistema Operativo
* Se generó un medio de instalación *bootable* utilizando la imagen ISO oficial de Proxmox VE.
* **Sistema de Archivos:** Durante la instalación se configuró el disco utilizando *ext4* para asegurar la integridad de las máquinas virtuales.

### 2. Configuración de Red (Management Interface)
Para garantizar la conectividad y administración constante del hipervisor, se asignó una configuración de red estática vinculada a la interfaz física del servidor:

### Configuración IP del Nodo Proxmox
IP Address: 192.168.1.200/24 

Gateway: 192.168.1.1

DNS Server: 1.1.1.1