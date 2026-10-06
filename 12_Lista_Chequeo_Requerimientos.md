# 📝 Lista de Chequeo: Requerimientos Técnicos del MVP

Usa esta lista para controlar el avance real del desarrollo. No pases a la siguiente fase hasta que los checks de la fase anterior estén completados.

## 🧱 Fase 1: Inicialización y Base de Datos (Backend)
- [ ] Crear el repositorio local en Git y conectarlo a GitHub Desktop.
- [ ] Inicializar el entorno virtual limpio ejecutando `uv venv`.
- [ ] Instalar el paquete de dependencias iniciales (`fastapi`, `uvicorn`, `sqlalchemy`, `psycopg2-binary`).
- [ ] Crear el archivo `.env` local con las credenciales de la base de datos de pruebas.
- [ ] Escribir los modelos de SQLAlchemy para las 4 tablas base (`companies`, `users`, `folders`, `files`) usando UUIDs.
- [ ] Ejecutar la creación de tablas en la base de datos local y verificar desde un gestor (DBeaver/pgAdmin).

## 🔒 Fase 2: Seguridad, Roles y Multi-Tenant (Backend)
- [ ] Configurar las librerías de seguridad (`passlib`, `bcrypt`, `python-jose`).
- [ ] Crear el endpoint de registro de Gestor SST (`POST /auth/register`).
- [ ] Crear el endpoint de login que retorne el token JWT (`POST /auth/login`).
- [ ] Implementar el endpoint para que el Gestor registre una Empresa Cliente (`POST /companies`).
- [ ] Desarrollar la dependencia `get_current_tenant` que extraiga el `company_id` del token para aislar las consultas.
- [ ] Probar con el archivo `pruebas.http` que un Gestor no pueda ver los datos de empresas que no le pertenecen.

## 📂 Fase 3: Gestión Documental de SST (Backend)
- [ ] Crear endpoints para la gestión de carpetas (`POST /folders` y `GET /folders` estructurados como árbol).
- [ ] Configurar la librería `python-multipart` para recibir archivos pesados.
- [ ] Programar la lógica de almacenamiento físico local en la ruta `./storage/{company_id}/`.
- [ ] Añadir los campos de SST obligatorios a la metadata del archivo (`expiration_date`, `is_critical`).
- [ ] Crear el endpoint de subida de archivos (`POST /files/upload`).
- [ ] Crear el endpoint para listar archivos por carpeta (`GET /folders/{folder_id}/files`).

## 🎨 Fase 4: Panel de Control e Interfaz (Frontend Angular)
- [ ] Inicializar el proyecto Angular e instalar Tailwind CSS para los estilos visuales.
- [ ] Crear el módulo de Autenticación (Pantalla de Login) y guardar el token JWT en el `localStorage`.
- [ ] Diseñar el Dashboard principal con la lista desplegable de "Empresas Clientes" a gestionar.
- [ ] Desarrollar el componente visual del explorador de archivos (carpetas y subcarpetas dinámicas).
- [ ] Crear el botón de cargue de archivos que envíe los PDFs/Fotos mediante un formulario (`FormData`) a la API.
- [ ] Implementar los indicadores visuales de colores para los estados de los documentos (Verde = Vigente, Amarillo = Por Vencer, Rojo = Vencido).
