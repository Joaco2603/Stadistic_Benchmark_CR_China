# Práctica 1: Comparación estadística y diagramas de caja

**Universidad CENFOTEC** · Escuela de Fundamentos  
**Curso:** Probabilidad y Estadística 2 · III Cuatrimestre 2026  
**Docente:** Kevin Eduardo Cervantes Melgar  
**Actividad:** Análisis descriptivo (10 % de la nota final) · Modalidad individual

## Objetivo

Aplicar medidas de **tendencia central**, **dispersión** y **posición** al dataset de [Gapminder](https://www.gapminder.org/), y contrastar dos países —**Costa Rica** y **China**— mediante diagramas de caja y reglas de detección de atípicos (Tukey).

Variables de trabajo:

| Variable     | Descripción |
|-------------|-------------|
| `gdpPercap` | PIB per cápita en USD (paridad de poder adquisitivo) |
| `lifeExp`   | Esperanza de vida al nacer (años) |
| `pop`       | Población (habitantes) |

## Contenido del repositorio

| Archivo | Descripción |
|---------|-------------|
| `Practica1_Analisis_Descriptivo.ipynb` | Notebook con todo el análisis, gráficos e interpretación |
| `gapminder_all.csv` | Datos en formato ancho (142 países, quinquenios 1952–2007) |
| `README.md` | Este archivo |

## Requisitos

- Python 3.10 o superior (desarrollado con 3.13)
- [Jupyter](https://jupyter.org/) (Notebook o Lab)
- Dependencias: `pandas`, `numpy`, `matplotlib`, `seaborn`

Si el entorno virtual está en el directorio padre del curso (`probabilidad-2/.venv`):

```bash
cd /ruta/a/probabilidad-2
python -m venv .venv
source .venv/bin/activate   # en Windows: .venv\Scripts\activate
pip install jupyter pandas numpy matplotlib seaborn
```

## Cómo ejecutar

1. Activar el entorno virtual (si aplica).
2. Entrar a esta carpeta (el CSV se carga con ruta relativa `gapminder_all.csv`).
3. Abrir el notebook:

```bash
cd practica-1
jupyter notebook Practica1_Analisis_Descriptivo.ipynb
```

Ejecutar las celdas en orden desde el inicio.

## Datos

- **Fuente:** Gapminder Foundation (`gapminder_all.csv`).
- **Formato original:** una fila por país, columnas por año (`gdpPercap_1952`, `lifeExp_1952`, `pop_1952`, …).
- **Formato de análisis:** panel largo con una observación por país y año (1 704 filas, 142 países, 12 cortes temporales).

## Estructura del notebook

1. **Carga y verificación** — Lectura del CSV ancho, transformación a panel largo y comprobaciones básicas.
2. **Estadísticas descriptivas del panel completo** — Media, mediana, cuartiles, IQR, desviación estándar, coeficiente de variación y asimetría (Fisher).
3. **Comparación Costa Rica y China** — Tablas y métricas por país y variable.
4. **Diagramas de caja** — Panel global, corte 2007 por continente y comparación bilateral (incluye escalas lineal y logarítmica cuando aplica).
5. **Interpretación analítica** — Simetría, atípicos (regla de Tukey), lectura de los boxplots de 2007 y conclusiones del contraste entre ambos países.

## Licencia y uso académico

Material elaborado en el marco del curso de Probabilidad y Estadística 2 en CENFOTEC. Los datos pertenecen a Gapminder Foundation; consultar sus condiciones de uso en su sitio oficial.
