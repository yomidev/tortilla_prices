# Evolución del precio de la tortilla en México (2007-2026)

Proyecto de visualización de datos (Maestría en Inteligencia Artificial, ITA).

## Datos

- Dataset: _Tortilla Prices in Mexico_, R. Chavelas, Kaggle: [https://www.kaggle.com/datasets/richave/tortilla-prices-in-mexico]
- Fuente primaria: SNIIM, Secretaría de Economía: [http://www.economia-sniim.gob.mx/Tortilla.asp]
- Licencia: CC0. Fecha de descarga: [03 de Octubre de 2026]
- Limpieza: documentada en el notebook (sección 3).

## Cómo reproducirlo

1. Clonar el repositorio y crear un entorno: `python -m venv .venv`
2. Instalar dependencias: `pip install -r requirements.txt`
3. Colocar `tortilla_prices.csv` en `data/` (ya incluido o descargarlo de Kaggle).
4. Abrir `notebooks/proyecto_tortilla.ipynb` y ejecutar _Run All_.

## Resultados

- Notebook: `notebooks/proyecto_tortilla.ipynb`
- Gráfica interactiva: [https://yomidev.github.io/tortilla_prices/html/precio_por_entidad.html]
- Dashboard en Tableau Public: [https://public.tableau.com/views/DashboardPreciodelatortillade2007a2026/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link]
