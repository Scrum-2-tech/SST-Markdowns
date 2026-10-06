# 📌 Resumen General del Proyecto (SST SaaS)

Este documento unifica los puntos clave estructurados en las notas principales para un repaso rápido de la arquitectura del software.

## 1. Enfoque del Producto (Multi-Tenant)
- **Cliente Objetivo:** Diseñado para Gestores de SST profesionales o Consultores Independientes.
- **Estructura:** Un solo Gestor puede administrar múltiples empresas clientes de forma aislada (Portafolios independientes).
- **Acceso de Auditoría:** Vista opcional de "Solo Lectura" para que los dueños de las empresas clientes revisen sus documentos.

## 2. Arquitectura Tecnológica (Stack Técnico)
- **Gestor & Backend:** Python administrado con **UV** + **FastAPI** (Garantiza velocidad y manejo óptimo de archivos pesados).
- **Frontend:** **Angular** (Ideal para interfaces interactivas y componentes de carpetas dinámicas).
- **Base de Datos:** **PostgreSQL** (Uso de UUIDs para seguridad y relaciones padre-hijo para subcarpetas infinitas).
- **Almacenamiento:** Disco local para desarrollo; **Cloudflare R2** para producción (Ahorro crítico: \$0 por datos transferidos).

## 3. Viabilidad Financiera (Costos Mensuales)
- **Fase MVP (Pruebas):** **\$0.00 a \$13.00 USD**. Riesgo económico nulo usando las capas gratuitas de Render, Vercel y Cloudflare R2 (10 GB gratis).
- **Fase Comercial (Hasta 100 empresas):** **\$26.50 a \$35.00 USD**. Infraestructura dedicada y escalable con alta rentabilidad por licenciamiento.

## 4. Seguridad de la Información
- Autenticación segura mediante tokens JWT.
- Validación obligatoria de `company_id` en cada consulta del backend para evitar filtración de datos entre empresas competidoras.
