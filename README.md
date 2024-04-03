# DevSecOps Proyecto de Prueba

## Propósito

Este repositorio ha sido creado como parte de un ejercicio para demostrar la implementación de prácticas DevSecOps en el ciclo de vida del desarrollo de software. Contiene un proyecto web básico desarrollado en Node.js y utiliza GitHub Actions para automatizar las pruebas de seguridad y otras comprobaciones de calidad en el código.

## Configuración y Ejecución

### Requisitos Previos

Para ejecutar este proyecto, necesitarás tener instalado Node.js y npm en tu sistema. Puedes descargarlos e instalarlos desde [nodejs.org](https://nodejs.org/).

### Pasos para la Ejecución

1. Clona este repositorio en tu máquina local.
2. Abre una terminal y navega al directorio donde has clonado el repositorio.
3. Ejecuta `npm install` para instalar todas las dependencias necesarias.
4. Una vez finalizada la instalación, ejecuta `npm start` para iniciar el servidor.
5. Abre un navegador y visita `http://localhost:3000` para ver la aplicación en acción.

## CI/CD y Comprobaciones de Seguridad

Este proyecto utiliza GitHub Actions para implementar una pipeline de CI/CD que realiza las siguientes acciones:

- **Instalación de Dependencias**: Automatiza la instalación de dependencias necesarias para el proyecto.
- **Pruebas Unitarias**: Ejecuta un conjunto básico de pruebas unitarias para asegurar que el código cumple con los requisitos funcionales básicos.
- **Análisis de Seguridad**:
  - **Dependency-Check**: Utiliza la herramienta `npm audit` para identificar dependencias con vulnerabilidades de seguridad conocidas. Esta es una comprobación crucial para mantener la integridad y seguridad del proyecto.
  - **SonarLint**: Se integra para realizar un análisis estático del código, identificando problemas de seguridad y de calidad en el código fuente.
  - **Detect-Secrets**: Se utiliza para buscar en el código cualquier secreto o credencial hardcodeada que podría representar un riesgo de seguridad.

La configuración de GitHub Actions se encuentra en el archivo `.github/workflows/main.yml` del repositorio. Esta pipeline se ejecuta automáticamente en cada `push` y `pull request` para garantizar que todas las nuevas contribuciones cumplen con las políticas de calidad y seguridad antes de ser integradas en la rama principal.

## Conclusión

Este proyecto es un ejemplo de cómo se pueden integrar prácticas de seguridad en el ciclo de vida del desarrollo de software desde las fases iniciales, utilizando herramientas y procesos automatizados para garantizar la calidad y seguridad del software producido.
