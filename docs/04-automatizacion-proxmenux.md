# Automatización Operativa y Monitoreo: ProxMenux

Como parte de la estrategia para optimizar la administración del clúster y reducir la carga operativa, se implementó la suite **ProxMenux**. 

Esta integración se desplegó con dos objetivos arquitectónicos principales:
1. **Automatización de Tareas (TUI):** Sustituir la ejecución manual de comandos repetitivos de bajo nivel por flujos de trabajo automatizados mediante una interfaz de terminal, minimizando el margen de error humano en la gestión de discos y recursos.
2. **Telemetría y Monitoreo:** Desplegar *ProxMenux Monitor* para obtener un panel (dashboard) en tiempo real con métricas críticas de salud de hardware (SMART), consumo de CPU y análisis de tráfico de red.

## 1. Despliegue en el Nodo Principal

La herramienta se provisionó ejecutando el script de instalación oficial directamente desde la shell del hipervisor:

```bash
bash -c "$(curl -fsSL [https://raw.githubusercontent.com/MacRimi/ProxMenux/main/proxmenux.sh](https://raw.githubusercontent.com/MacRimi/ProxMenux/main/proxmenux.sh))"