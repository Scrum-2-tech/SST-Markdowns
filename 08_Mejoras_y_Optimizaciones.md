# 🚀 Mapa de Mejoras, Automatizaciones y Mitigación de Brechas

Este documento detalla el plan de evolución del software (Fase Post-MVP) para aumentar su valor comercial y proteger el sistema.

## 1. Automatizaciones Inteligentes (El gancho comercial con IA)
- [ ] **Lectura Automatizada de Documentos (OCR + IA):** Implementar un módulo para que la IA lea los PDFs subidos (ej. cursos de alturas, licencias), extraiga los datos clave (Nombre, Cédula, Fecha de vencimiento) y llene el formulario de registro automáticamente.
- [ ] **Notificaciones Omnicanal:** Conectar el sistema de alertas con la API de **WhatsApp / Telegram** para notificar al Gestor SST directamente en su celular cuando un documento crucial esté a 15 días de vencerse.
- [ ] **Generador de Informes de Auditoría:** Crear un botón que evalúe la completitud de las carpetas de una empresa y exporte un informe en PDF con gráficas sobre el porcentaje de cumplimiento legal para entregar a Gerencia.

## 2. Optimizaciones de Rendimiento y Código
- [ ] **Subida por Bloques (*Chunked Uploads*):** Configurar en FastAPI la recepción de archivos por fragmentos en lugar de cargarlos completos en la memoria RAM, evitando caídas del servidor con PDFs pesados.
- [ ] **Caché de Consultas:** Implementar Redis o almacenamiento en caché para el árbol de carpetas de Angular, acelerando la navegación del usuario sin saturar la base de datos PostgreSQL en cada clic.

## 3. Mitigación de Brechas de Seguridad (Zonas de Control)
- [ ] **Filtro de Extensiones y "Magic Bytes":** Validar en el backend que los archivos subidos correspondan estrictamente a documentos permitidos (PDF, PNG, JPG, XLSX), bloqueando cualquier intento de subir scripts maliciosos (`.exe`, `.bat`).
- [ ] **Límite de Almacenamiento por Empresa:** Programar un validador en la base de datos que verifique el peso total consumido por cada empresa antes de permitir una nueva subida, evitando que un usuario sature el almacenamiento de forma maliciosa.
