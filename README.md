# AlaShop — Gestión de inventario y ventas

Aplicación web tipo SaaS para administrar inventario y operaciones de punto de venta, con frontend independiente y API backend.

## Arquitectura
- **Backend:** Python, FastAPI, SQLAlchemy y PostgreSQL.
- **Frontend:** React, Vite y Tailwind CSS.
- **Autenticación:** JWT.
- **Servicios opcionales:** almacenamiento de imágenes, correo y proveedores de pago.
- **Despliegue:** configuración declarativa disponible en el repositorio.

## Estructura
- `alashop-backend/`: API, modelos y configuración del servidor.
- `alashop-frontend/`: aplicación web.
- `render.yaml`: configuración de despliegue que debe revisarse antes de usarla en producción.

## Desarrollo local
Consulta los archivos de cada componente para verificar los comandos actuales y sus requisitos. Configura las variables de entorno a partir de los archivos de ejemplo y usa credenciales de desarrollo nuevas.

## Seguridad antes de desplegar
- Genera una clave de firma JWT única y fuerte en el entorno de despliegue.
- No uses credenciales de demostración en producción.
- Guarda tokens de pago, contraseñas SMTP y claves de servicios en un gestor de secretos.
- Verifica aislamiento por tienda en todas las consultas y operaciones.
- Configura webhooks, CORS, autenticación y permisos antes de habilitar pagos reales.
- Ejecuta pruebas y revisa dependencias antes de publicar.

## Estado
Este README describe el propósito y la arquitectura prevista; la disponibilidad de pagos, almacenamiento y funciones SaaS debe validarse mediante pruebas de integración.
