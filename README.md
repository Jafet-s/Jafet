# CI Pipeline para Laravel

## Objetivo
Automatizar la instalación de dependencias y la ejecución de pruebas de la aplicación Laravel mediante GitHub Actions.

## Tecnologías
- PHP
- Laravel
- Composer
- PHPUnit / Pest
- Git y GitHub
- GitHub Actions

## Requisitos
- PHP (versión compatible)
- Composer
- Git
- Acceso al repositorio de GitHub

## Instalación local
1. Clonar el repositorio.
2. Ejecutar `composer install`.
3. Copiar `.env.example` a `.env`.
4. Ejecutar `php artisan key:generate`.
5. Configurar la base de datos requerida.
6. Ejecutar migraciones si son necesarias.
7. Ejecutar pruebas localmente con `php artisan test`.

## Integración Continua
El workflow `.github/workflows/ci.yml` se ejecuta al enviar cambios (`push`) a la rama `main` o al crear una solicitud de extracción (`pull_request`) hacia ella.

## Pruebas y Evidencias
- **Ejecución local:** Pruebas aprobadas con `php artisan test`.
- **Ejecución exitosa inicial:** [Enlace a la ejecución exitosa de GH Actions]
- **Ejecución fallida controlada:** [Enlace a la ejecución fallida] (se modificó la aserción a HTTP 404 para validar la detección de errores del pipeline).
- **Ejecución exitosa tras corrección:** [Enlace a la ejecución corregida].

## Conclusiones
La implementación del pipeline de CI permite detectar fallos en la etapa de integración de código antes de ser fusionados o desplegados, garantizando la estabilidad y calidad de la aplicación.
