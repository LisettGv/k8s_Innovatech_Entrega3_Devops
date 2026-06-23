# 🚀 Innovatech Chile - Plataforma de Microservicios Contenedorizados

Este repositorio contiene el código fuente y la configuración de infraestructura como código de la plataforma unificada de gestión de **Ventas** y **Despachos** para la empresa Innovatech Chile. El proyecto ha evolucionado de un modelo tradicional *Lift & Shift* hacia una arquitectura moderna orientada a la cultura **DevOps**.

## 🏗️ Arquitectura del Sistema
El ecosistema completo está diseñado para ejecutarse de forma aislada y eficiente utilizando **Docker** y **Docker Compose** en una instancia de cómputo optimizada de Amazon Web Services (AWS EC2).

*   **Frontend:** Aplicación SPA (Single Page Application) servida mediante un servidor web **Nginx** de alta eficiencia (Puerto 80).
*   **Backend Ventas:** Microservicio desarrollado en Spring Boot (Puerto 8080).
*   **Backend Despachos:** Microservicio desarrollado en Spring Boot (Puerto 8081).
*   **Base de Datos:** Motor relacional con persistencia mediante volúmenes de Docker (Puerto 3306).

## 🐳 Estrategia de Contenedorización
Todos los componentes de código implementan **Dockerfiles Multi-stage** para reducir significativamente el tamaño de las imágenes de producción y mitigar superficies de ataque eliminando compiladores o dependencias de desarrollo del entorno de ejecución.

### Ejecución Local del Entorno completo:
Para levantar el stack tecnológico completo de forma local, clona este repositorio y ejecuta:
```bash
docker-compose up --build -d
