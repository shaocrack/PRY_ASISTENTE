# SaludIA - Estimador Agéntico de Copago y Cobertura 🇪🇨🏥

Este proyecto es una solución para el reto **"Estimador Agéntico de Copago y Cobertura para el Paciente"** del HackIAthon.

## Descripción
SaludIA es un agente conversacional inteligente impulsado por Google Gemini. Permite a los pacientes en Ecuador ingresar sus síntomas, el agente sugiere la especialidad médica adecuada, y mediante una base de datos simulada y llamadas a herramientas (Function Calling), calcula el copago exacto basado en su plan de seguro (SaludSA, Humana, BMI, etc.) y la ciudad (Quito, Guayaquil).

## Características
- **Interfaz amigable:** Construida con Streamlit, ofrece una experiencia de chat fluida y atractiva.
- **Lógica Agéntica:** El LLM (Gemini 1.5 Flash) es capaz de razonar, pedir los datos faltantes al usuario y ejecutar código Python de forma autónoma (`calcular_costos`) para obtener cálculos matemáticos precisos en lugar de inventarlos.
- **Datos Regionales:** Utiliza una base de datos (`datos_ecuador.json`) con hospitales y seguros médicos comunes en Ecuador.

## Estructura del Proyecto
- `app.py`: Contiene la aplicación web de Streamlit y la lógica del Agente (LLM + Tools).
- `datos_ecuador.json`: Base de datos simulada (Mock DB).
- `requirements.txt`: Dependencias del proyecto.

## Cómo ejecutar localmente

1. Clona el repositorio.
2. Instala las dependencias:
   ```bash
   pip install -r requirements.txt
   ```
3. Crea un archivo `.env` basado en `.env.example` y agrega tu `GEMINI_API_KEY`.
4. Ejecuta la aplicación:
   ```bash
   streamlit run app.py
   ```

## Despliegue Público
Esta aplicación puede ser fácilmente desplegada en **Streamlit Community Cloud** subiendo este repositorio a GitHub y vinculándolo con una cuenta gratuita de Streamlit. No olvides configurar la variable `GEMINI_API_KEY` en los *Secrets* de Streamlit.
