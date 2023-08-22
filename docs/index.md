[](https://github.com/vizzuhq/ipyvizzu/edit/main/README.md "Editar esta página")

[![Vizzu](https://lib.vizzuhq.com/0.8/readme/infinite-60.gif)](./)

**ipyvizzu** - Crea gráficos animados en Jupyter Notebook y entornos similares con una sintaxis simple en Python


ipyvizzu
========

Acerca del Proyecto
-------------------

`ipyvizzu` es una herramienta de creación de gráficos animados para cuadernos de [Jupyter](https://jupyter.org), [Google Colab](https://colab.research.google.com), [Databricks](https://docs.databricks.com/notebooks), [Kaggle](https://www.kaggle.com/code) y [Deepnote](https://deepnote.com), entre otras plataformas. `ipyvizzu` permite a científicos de datos y analistas utilizar la animación para contar historias con datos utilizando `Python`. Está construida sobre la librería de gráficos de código abierto [Vizzu](https://github.com/vizzuhq/vizzu-lib) en `JavaScript`/`C++`.

**Existe una nueva extensión de `ipyvizzu`, [ipyvizzu-story](https://vizzuhq.github.io/ipyvizzu-story/)** con la cual los gráficos animados se pueden presentar directamente desde los cuadernos. Dado que la sintaxis de `ipyvizzu-story` es un poco diferente de la de `ipyvizzu`, te recomendamos comenzar desde el [repositorio de ipyvizzu-story](https://github.com/vizzuhq/ipyvizzu-story) si estás interesado en utilizar gráficos animados para presentar tus hallazgos en vivo o compartir tu presentación como un archivo HTML.

Al igual que `Vizzu`, `ipyvizzu` utiliza un motor de visualización de datos genérico que genera varios tipos de gráficos y los anima de manera fluida. Está diseñada para construir historias de datos animadas, ya que permite mostrar diferentes perspectivas de los datos que los espectadores pueden seguir fácilmente.

Características principales:

*   Diseñada con enfoque en la animación;
*   Configuraciones basadas en pautas de visualización de datos;
*   Funciona con DataFrames de `Pandas`, y también admite entrada de datos en formato `JSON` y en línea;
*   Función de desplazamiento automático para mantener el gráfico actual en posición mientras se ejecutan varias celdas.

Instalación
-----------

`pip install ipyvizzu`

Visita el [capítulo de Instalación](./installation.md) para más opciones y detalles.

Uso
---

Puedes crear la animación a continuación con el siguiente fragmento de código.

![ipyvizzu](https://ipyvizzu.vizzuhq.com/latest/assets/ipyvizzu-promo.gif)

```python
import pandas as pd
from ipyvizzu import Chart, Data, Config

df = pd.read_csv(
    "https://ipyvizzu.vizzuhq.com/0.16/showcases/titanic/titanic.csv"
)
data = Data()
data.add_df(df)

chart = Chart(width="640px", height="360px")

chart.animate(data)

chart.animate(
    Config(
        {
            "x": "Count",
            "y": "Sex",
            "label": "Count",
            "title": "Passengers of the Titanic",
        }
    )
)
chart.animate(
    Config(
        {
            "x": ["Count", "Survived"],
            "label": ["Count", "Survived"],
            "color": "Survived",
        }
    )
)
chart.animate(Config({"x": "Count", "y": ["Sex", "Survived"]}))
```



