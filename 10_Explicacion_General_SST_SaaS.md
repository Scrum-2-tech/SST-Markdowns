# 📄 Documento de Especificación: SaaS Documental para SST

Este documento explica de forma integral el concepto, la arquitectura, la viabilidad financiera y la estrategia de desarrollo del software de Gestión Documental para Seguridad y Salud en el Trabajo (SST).

---

## 1. El Concepto y Modelo de Negocio (¿Qué es?)
El sistema es una plataforma **SaaS (Software as a Service) Multi-Tenant** enfocada en resolver el desorden documental de los **Gestores de SST, Consultores o Profesionales Independientes**. 

En lugar de manejar carpetas locales, memorias USB o carpetas compartidas de Google Drive que confunden a los clientes, el software le permite al Gestor:
1. Crear un portafolio independiente para cada una de las empresas que asesora.
2. Organizar la documentación obligatoria por ley en subcarpetas dinámicas (Matrices de riesgo, capacitaciones, exámenes médicos).
3. Monitorear fechas de vencimiento críticas para evitar multas legales a sus clientes.
4. Brindar un acceso de "Solo Lectura" (Vista de Auditoría) a los dueños de las empresas para que verifiquen que todo su sistema de gestión está al día.

---

## 2. Arquitectura Tecnológica y Despliegue (¿En qué y dónde se hace?)
Para garantizar la máxima velocidad en la transferencia de archivos pesados (PDFs, imágenes de evidencias) y un aislamiento total de los datos entre empresas, el stack técnico elegido es:

* **El Backend (El motor):** **Python** utilizando el gestor de paquetes **UV** (moderno, eficiente y de alta velocidad) junto con el framework **FastAPI**. FastAPI procesa de forma nativa la subida de archivos binarios mediante formularios web.
* **El Frontend (La interfaz):** **Angular** + **Tailwind CSS**. Nos permite construir un panel de control interactivo, un explorador visual de carpetas ágil y adaptable a cualquier pantalla o dispositivo móvil.
* **La Base de Datos:** **PostgreSQL** (gestionada en la nube mediante proveedores como *Railway* o *Neon.tech*). Utiliza identificadores UUID para máxima seguridad y un modelo relacional auto-referenciado para permitir niveles de subcarpetas infinitos.
* **El Almacenamiento:** **Cloudflare R2**. Los archivos físicos (los PDFs y fotos reales) se guardan directamente en la nube de Cloudflare, mientras que la base de datos de PostgreSQL solo guarda el enlace de texto. Esto evita que el sistema se vuelva lento.

---

## 3. Viabilidad Financiera y Mantenimiento (¿Cuánto cuesta?)
El proyecto destaca por su altísima rentabilidad y nulo riesgo económico en sus etapas iniciales:

* **Fase de Pruebas / MVP (0 a 3 Empresas):** **$0.00 a $13.00 USD mensuales** (~$55.000 COP). Se aprovechan al máximo los planes gratuitos de *Vercel* (frontend), *Render/Railway* (backend) y los primeros 10 GB gratuitos de *Cloudflare R2*.
* **Fase Comercial / Producción (Hasta 100 Empresas):** **$26.50 a $35.00 USD mensuales** (~$110.000 a $150.000 COP). Infraestructura robusta 24/7 con bases de datos que realizan respaldos automáticos diarios. El costo total de los servidores del mes se cubre con la suscripción de un solo cliente; el resto es ganancia neta.

---

## 4. Estrategia de Desarrollo y Evolución con IA
El desarrollo se ejecutará localmente manteniendo un control estricto de versiones en **Git** a través de **GitHub Desktop** [Kiro]. Para optimizar los tiempos de entrega sin consumir excesivos créditos de Inteligencia Artificial (Kiro/Cursor), la IA se usará como un consultor de arquitectura modular:
* El desarrollo rutinario y de interfaz se apoyará en el **autocompletado en línea (gratuito e ilimitado)**.
* Los créditos se reservarán para automatizaciones de la Fase Post-MVP, tales como la **lectura inteligente de PDFs mediante IA (OCR)** para extraer fechas de vencimiento de forma automática, y la integración de **alertas automáticas vía WhatsApp** directas al celular del Gestor.
