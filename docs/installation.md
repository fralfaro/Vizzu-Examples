Instalación
============

`ipyvizzu` requiere los paquetes `IPython` y `jsonschema`.

!!! info

    `ipyvizzu` requiere y descarga la [biblioteca](https://www.jsdelivr.com/package/npm/vizzu) `JavaScript`/`C++` de [Vizzu](https://github.com/vizzuhq/vizzu-lib) desde `jsDelivr CDN`, pero también puedes utilizar una versión diferente o autohospedada. Consulta el [capítulo de Configuración de gráficos](https://ipyvizzu.vizzuhq.com/latest/tutorial/chart_settings/) para obtener más detalles.




pypi
----

Ejecuta el siguiente comando para instalar `ipyvizzu` desde [pypi](https://pypi.org/project/ipyvizzu/)

`pip install ipyvizzu`

y así es como se actualiza.

`pip install -U ipyvizzu`

!!! note
    `ipyvizzu` se puede usar con algunas dependencias adicionales como `pandas`, `pyspark`, `numpy` y `fugue`.

    Por ejemplo, si deseas trabajar con `pandas` y `DataFrame` junto con `ipyvizzu`, debes instalar `pandas` como un extra:

    `pip install ipyvizzu[pandas]`

Puedes utilizar `ipyvizzu` en `Jupyter/IPython`, `Streamlit` o `Panel` (consulta el [capítulo de Entornos](https://ipyvizzu.vizzuhq.com/latest/environments/) para más detalles).

### Jupyter/IPython

Puedes instalar `ipyvizzu` en tu cuaderno sin utilizar la línea de comandos ingresando el siguiente código en una celda.

`!pip install ipyvizzu`

conda / mamba
-------------

La instalación de `ipyvizzu` desde `conda-forge` se puede lograr agregando `conda-forge` a tus canales con:

`conda config --add channels conda-forge conda config --set channel_priority strict`

Una vez habilitado el canal `conda-forge`, ejecuta el siguiente comando para instalar `ipyvizzu` desde [conda](https://anaconda.org/conda-forge/ipyvizzu/)

`conda install ipyvizzu  # o con mamba:  mamba install ipyvizzu`

y así es como se actualiza.