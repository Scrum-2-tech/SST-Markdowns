# 🛠️ Ficha Técnica: ¿En qué lo vamos a hacer y dónde se va a montar?

Este es el resumen directo del stack de desarrollo y los servidores elegidos para el proyecto de SST.

## 1. ¿En qué lo vamos a programar? (El Stack de Desarrollo)
- **El Motor (Backend):** **Python** utilizando el gestor de paquetes **UV** (para que sea ultra rápido y moderno) + el framework **FastAPI**.
- **La Interfaz (Frontend):** **Angular** combinado con **Tailwind CSS** (para lograr un diseño visual limpio, profesional y adaptable a celulares).
- **El Cerebro (Base de Datos):** **PostgreSQL** (Garantiza que la información de los usuarios y las subcarpetas no se corrompan y estén ordenadas).

## 2. ¿Cómo se va a manejar el almacenamiento de archivos?
- **Los Archivos (PDFs y Fotos):** Se guardarán en **Cloudflare R2**. 
- **La Estrategia:** En la base de datos de PostgreSQL solo se guarda un texto corto con la URL del archivo; el documento real se almacena en la nube de Cloudflare para no ralentizar el sistema.

## 3. ¿Dónde se va a montar para que funcione en internet? (Servidores Cloud)
- **El Backend (FastAPI):** Se subirá a **Render.com** o **Railway.app** (Servidores en la nube muy económicos y fáciles de conectar con Git).
- **El Frontend (Angular):** Se subirá a **Vercel** o **Netlify** (Son plataformas que distribuyen la interfaz visual por todo el mundo de forma gratuita).
- **El Dominio:** Se comprará un nombre `.com` o `.co` personalizado en **Namecheap** o **GoDaddy**.
