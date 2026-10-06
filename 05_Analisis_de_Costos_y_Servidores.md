# 💰 Análisis Financiero: Costos de Infraestructura Cloud (SST SaaS)

Este análisis contempla dos escenarios: **Fase de Pruebas (MVP)** para validar el producto con los primeros clientes, y **Fase de Producción (Escalable)** cuando ya se vendan licencias masivas.

## 🟢 Escenario 1: Fase de Pruebas / MVP (0 a 3 Empresas Clientes)
*Ideal para arrancar en casa y mostrar los primeros demos sin arriesgar capital.*

| Concepto | Proveedor | Costo Mensual (USD) | Notas Técnicas |
| :--- | :--- | :--- | :--- |
| **Base de Datos (PostgreSQL)** | Railway.app / Render.com | **$0.00 a $7.00** | Planes iniciales con recursos medidos de RAM y CPU. |
| **Backend (FastAPI)** | Render.com / Railway | **$0.00 a $5.00** | Servidor web que se apaga automáticamente si no recibe tráfico (gratis) o activo 24/7 por $5. |
| **Frontend (Angular)** | Vercel / Netlify | **$0.00** | Despliegue estático global gratuito e ilimitado. |
| **Almacenamiento (Archivos SST)** | Cloudflare R2 | **$0.00** | Los primeros **10 GB** de almacenamiento son totalmente gratis. |
| **Dominio Web (.com)** | Namecheap / GoDaddy | **$1.00** | Pago único anual (aprox. $10 a $12 USD al año). |
| 💳 **TOTAL ESTIMADO** | | **$0.00 a $13.00 / mes** | **Costo de arranque ultra bajo.** |

---

## 🔵 Escenario 2: Fase de Producción Comercial (Hasta 100 Empresas)
*Infraestructura robusta para cuando el software ya genere ingresos recurrentes por ventas.*

| Concepto | Proveedor | Costo Mensual (USD) | Notas Técnicas |
| :--- | :--- | :--- | :--- |
| **Base de Datos Dedicada** | Neon.tech / AWS RDS | **$15.00** | Base de datos relacional con respaldos automáticos diarios. |
| **Backend de Alta Velocidad** | Railway (Pro) / DigitalOcean | **$10.00** | Servidor con 1GB RAM dedicado para responder peticiones en milisegundos. |
| **Almacenamiento Masivo** | Cloudflare R2 | **$0.015 por GB** | Si tus clientes suben **100 GB** de PDFs y fotos de SST, pagas solo **$1.50 USD** al mes. *Nota: R2 no cobra por descarga (egreso), a diferencia de AWS S3.* |
| **Certificados SSL y Seguridad** | Cloudflare (Free Tier) | **$0.00** | Protección contra ataques informáticos (DDoS) y candado de seguridad HTTPS. |
| 💳 **TOTAL ESTIMADO** | | **$26.50 a $35.00 / mes** | **Margen de ganancia altísimo** si cobras una suscripción mensual a cada empresa. |
