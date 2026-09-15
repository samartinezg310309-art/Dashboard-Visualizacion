# 🌤️ Tablero de Calidad del Aire — Bogotá 2025

Tablero interactivo construido con **Streamlit + Pandas + Plotly** para explorar los datos horarios de PM10 y PM2.5 de la Red de Monitoreo de Calidad del Aire de Bogotá (RMCAB), incluyendo NowCast e IBOCA por estación.

## 🚀 Ejecutar en 3 pasos

```bash
# 1. Clonar el repositorio
git clone https://github.com/TU-USUARIO/tablero-calidad-aire-bogota.git
cd tablero-calidad-aire-bogota

# 2. Crear entorno virtual e instalar dependencias
python -m venv venv
source venv/bin/activate      # En Windows: venv\Scripts\activate
pip install -r requirements.txt

# 3. Ejecutar el tablero
streamlit run app.py
```

Streamlit abrirá automáticamente `http://localhost:8501` en tu navegador.

> El archivo `datos_calidad_aire_bogota_2025.csv` debe estar en la misma carpeta que `app.py` (ya viene incluido en este repositorio). Si no lo encuentra, el tablero te permitirá subirlo manualmente desde la barra lateral.

## 📁 Estructura del proyecto

```
tablero-calidad-aire-bogota/
├── app.py                                  # Aplicación Streamlit
├── requirements.txt                        # Dependencias de Python
├── datos_calidad_aire_bogota_2025.csv       # Datos RMCAB 2025
└── README.md
```

## 📊 Qué muestra el tablero

- KPIs: promedio, máximo, estación más contaminada y % de datos válidos
- Evolución temporal por estación (con bandas de referencia IBOCA)
- Comparativo entre estaciones y distribución de valores
- Patrones por hora del día y día de la semana
- Mapa de calor Estación × Mes
- Distribución por categoría IBOCA (Buena, Aceptable, Regular, Mala, Muy mala, Peligrosa)
- Tabla detallada con descarga en CSV

Filtros disponibles en la barra lateral: rango de fechas, estaciones, contaminante (PM10/PM2.5) y métrica (Concentración, NowCast, IBOCA).

## ☁️ Publicarlo en la web (sin instalar nada localmente)

La forma más sencilla de compartir el tablero con otras personas (por ejemplo, la Secretaría de Ambiente) es con **[Streamlit Community Cloud](https://streamlit.io/cloud)**, que es gratuito:

1. Sube este repositorio a tu cuenta de GitHub (ver instrucciones abajo).
2. Entra a [share.streamlit.io](https://share.streamlit.io) e inicia sesión con GitHub.
3. Haz clic en **"New app"**, elige este repositorio, la rama `main` y el archivo `app.py`.
4. Streamlit Cloud instalará las dependencias de `requirements.txt` automáticamente y te dará un enlace público (`https://tu-app.streamlit.app`) para compartir.

## 📦 Requisitos

- Python 3.9 o superior
- Ver `requirements.txt` para las versiones de librerías

## 📄 Fuente de datos

Red de Monitoreo de Calidad del Aire de Bogotá (RMCAB). Datos horarios de PM10 y PM2.5, año 2025.
