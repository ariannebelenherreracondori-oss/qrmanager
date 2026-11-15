# QRManager

Aplicación web para generar y guardar códigos QR. Permite registrar usuarios, iniciar sesión y crear códigos QR con texto o enlaces.

## Tecnologías
- Python
- NiceGUI
- SQLModel y SQLite
- Passlib y bcrypt
- Docker

## Estructura
- app/core/: configuración, base de datos y seguridad.
- app/models/: modelos de datos.
- app/repositories/: acceso a los datos.
- app/services/: lógica del sistema.
- app/ui/: interfaz de usuario.
- app/main.py: inicio de la aplicación.

## Ejecución con Docker

Construir la imagen:

```bash
docker build -t qrmanager-app .
```

Crear e iniciar el contenedor:

```bash
docker run -d -p 8080:8080 --name qrmanager_container qrmanager-app
```

Abrir en el navegador: http://localhost:8080

Si el contenedor ya existe y está detenido:

```bash
docker start qrmanager_container
```

## Uso
1. Registrar una cuenta.
2. Iniciar sesión.
3. Escribir el título y el contenido del QR.
4. Seleccionar una categoría.
5. Presionar “Generar y guardar QR”.
6. Consultar el código en “Mis Códigos QR Guardados”.