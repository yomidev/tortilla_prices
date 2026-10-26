# Evolución del precio de la tortilla en México (2007-2026)

Proyecto final de visualización de datos (Maestría en Inteligencia Artificial).

**Autora:** Yomira del Carmen Rosales Martínez

## Pregunta analítica

¿Cómo ha evolucionado, entre 2007 y 2026, el precio de la tortilla por entidad federativa y canal de venta (tortillerías y autoservicio), y cuánto tiempo de trabajo al salario mínimo se requiere para comprar un kilo?

**Audiencia:** organizaciones de la sociedad civil, investigadores, estudiantes y personal de dependencias públicas de política alimentaria y protección al consumidor.

## Hallazgo principal

Entre 2007 y 2025 el precio nominal por kilo se multiplicó por 2.8% en tortillerías y por 2.5% en autoservicio, pero el salario mínimo se multiplicó por 5.5. Comprar un kilo pasó de 85.1 a 43.4 minutos de trabajo en tortillerías (−49.0%) y de 54.5 a 25.0 minutos en autoservicio (−54.2%). La mejora se concentra después de 2019. La tortilla no se abarató: mejoró el poder de compra del salario mínimo.

## Resultados

- Dashboard interactivo (HTML + Plotly): [https://yomidev.github.io/tortilla_prices/dashboard/index.html](https://yomidev.github.io/tortilla_prices/dashboard/index.html)
- Notebook: `notebooks/proyecto_tortilla_final.ipynb`
- Video de presentación (5-7 min): [https://drive.google.com/file/d/1dKonxuYbhISuUoydyoqAZlOwkRN-H5La/view?usp=sharing](https://drive.google.com/file/d/1dKonxuYbhISuUoydyoqAZlOwkRN-H5La/view?usp=sharing)

## Datos

| Dato                                           | Fuente                                                                                                                                                                                   |
| ---------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Precios de la tortilla por ciudad, mes y canal | _Tortilla Prices in Mexico_, R. Chavelas, Kaggle: [https://www.kaggle.com/datasets/richave/tortilla-prices-in-mexico](https://www.kaggle.com/datasets/richave/tortilla-prices-in-mexico) |
| Fuente primaria de los precios                 | SNIIM, Secretaría de Economía: [http://www.economia-sniim.gob.mx/Tortilla.asp](http://www.economia-sniim.gob.mx/Tortilla.asp)                                                            |
| Salario mínimo general 2007-2026               | CONASAMI, Comisión Nacional de los Salarios Mínimos (tabla histórica, zona general). Capturado a mano en el notebook (sección de salarios).                                              |

- Licencia del dataset de precios: CC0. Fecha de descarga: 3 de octubre de 2026.
- Limpieza: documentada en el notebook (sección 3).

## Metodología

- **Precio anual:** promedio de los promedios por ciudad, por año, canal y entidad. Precios nominales (sin deflactar).
- **Minutos de trabajo:** `precio por kg ÷ salario mínimo diario × 480` (jornada de 8 horas).
- **Kilos por jornada:** `salario mínimo diario ÷ precio por kg`.
- **Salario:** mínimo general de CONASAMI. No se usa el de la Zona Libre de la Frontera Norte.

## Límites del análisis

- Precios nominales; no se ajustan por inflación.
- 2026 es parcial (enero a abril).
- Junio y julio de 2020 se omiten por baja cobertura (menos de 45 ciudades).
- 17 de las 32 entidades tienen una sola ciudad en la muestra, por lo que el ranking estatal es menos robusto.
- Los minutos describen el acceso con el salario mínimo, no los ingresos de todos los hogares ni la informalidad.

## Cómo reproducirlo

1. Clonar el repositorio y crear un entorno: `python -m venv .venv` y activarlo.
2. Instalar dependencias: `pip install -r requirements.txt`
3. Colocar `tortilla_prices.csv` en `data/` (ya incluido).
4. Abrir `notebooks/proyecto_tortilla_final.ipynb` y ejecutar _Run All_. Esto regenera `dashboard/index.html`.
5. Abrir `dashboard/index.html` en el navegador.

## Estructura del repositorio

```
├── data/                  # tortilla_prices.csv
├── notebooks/             # proyecto_tortilla_final.ipynb
├── dashboard/             # index.html (dashboard final)
├── html/                  # gráficas de avances anteriores
├── requirements.txt
└── README.md
```

## Avances anteriores

- Gráfica interactiva por entidad: [https://yomidev.github.io/tortilla_prices/html/precio_por_entidad.html](https://yomidev.github.io/tortilla_prices/html/precio_por_entidad.html)
- Dashboard en Tableau Public (versión previa): [https://public.tableau.com/views/DashboardPreciodelatortillade2007a2026/Dashboard1](https://public.tableau.com/views/DashboardPreciodelatortillade2007a2026/Dashboard1)
