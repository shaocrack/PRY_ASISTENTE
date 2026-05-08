<div align="center">

```text
███████╗██╗  ██╗ █████╗  ██████╗ ████████╗███████╗ ██████╗██╗  ██╗
██╔════╝██║  ██║██╔══██╗██╔═══██╗╚══██╔══╝██╔════╝██╔════╝██║  ██║
███████╗███████║███████║██║   ██║   ██║   █████╗  ██║     ███████║
╚════██║██╔══██║██╔══██║██║   ██║   ██║   ██╔══╝  ██║     ██╔══██║
███████║██║  ██║██║  ██║╚██████╔╝   ██║   ███████╗╚██████╗██║  ██║
╚══════╝╚═╝  ╚═╝╚═╝  ╚═╝ ╚═════╝    ╚═╝   ╚══════╝ ╚═════╝╚═╝  ╚═╝
```

# AuraMed - Asistente de Salud 🇪🇨🏥

**Estimador Agéntico de Copago y Cobertura para el Paciente**

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://streamlit.io/)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![Gemini API](https://img.shields.io/badge/Gemini-Pro_1.5-orange.svg)](https://ai.google.dev/)

</div>

---

## 📖 Descripción del Proyecto

AuraMed (SaludIA) es un agente conversacional inteligente impulsado por **Google Gemini 1.5 Flash**. Diseñado para Ecuador, permite a los pacientes ingresar sus síntomas y, mediante un agente médico empático:

1. **Sugiere** la especialidad médica adecuada (triage).
2. **Consulta** una red médica basada en la ciudad del usuario (ej. Quito, Guayaquil).
3. **Calcula** el copago exacto basado en su plan de seguro médico (SaludSA, Humana, BMI, etc.).

Todo esto mediante *Function Calling*, lo que garantiza que los precios, ubicaciones y cálculos de cobertura sean precisos y no alucinados por el modelo.

## ✨ Características Principales

*   **Interfaz Responsiva:** Construida con Streamlit, ofrece un diseño "premium" adaptable a móviles y escritorio.
*   **Modo Invitado / Modo Afiliado:**
    *   **Invitado:** Recibe sugerencias generales y precios referenciales privados, fomentando el registro.
    *   **Afiliado (Login):** Calcula copagos exactos, cruza datos de cobertura y devuelve la opción más barata en su red.
*   **Lógica Agéntica y Anti-Jailbreak:** Prompting estructurado para evitar que el asistente asuma el rol de doctor o se desvíe del tema médico.

## 📂 Estructura del Proyecto

El repositorio sigue una arquitectura sencilla y eficiente:

```text
PRY_ASISTENTE/
├── app.py                 # Código principal: UI de Streamlit y lógica del Agente Gemini
├── datos_ecuador.json     # Base de datos simulada (Mock DB) de pacientes y hospitales
├── requirements.txt       # Dependencias de Python
├── README.md              # Documentación del proyecto
├── .env.example           # Plantilla de variables de entorno
└── .streamlit/            # Configuración de apariencia de Streamlit
```

## 🚀 Instalación y Ejecución Local

1. **Clona este repositorio** y navega al directorio del proyecto:
   ```bash
   git clone <url-del-repositorio>
   cd PRY_ASISTENTE
   ```

2. **Instala las dependencias necesarias** (se recomienda usar un entorno virtual):
   ```bash
   pip install -r requirements.txt
   ```

3. **Configura tus variables de entorno:**
   Copia el archivo `.env.example` a `.env` y añade tu API key de Google Gemini:
   ```bash
   GEMINI_API_KEY=tu_api_key_aqui
   ```

4. **Ejecuta la aplicación:**
   ```bash
   streamlit run app.py
   ```

## 🌐 Despliegue Público

Esta aplicación está lista para ser desplegada en **Streamlit Community Cloud**. 
1. Sube este repositorio a tu cuenta de GitHub.
2. Vincula el repositorio en [share.streamlit.io](https://share.streamlit.io/).
3. Configura la variable `GEMINI_API_KEY` dentro de la sección **Secrets** de la configuración de tu app en Streamlit.

## 👨‍💻 Autores

Creado por **ShaoTech**

- **Jimmy Guajan** (ShaoPro)
- **Diana Conteron** (Dianis)

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - mira el archivo [LICENSE](LICENSE) para más detalles.

---
<div align="center">
  <i>Desarrollado para el HackIAthon.</i>
</div>
