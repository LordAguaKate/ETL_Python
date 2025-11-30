# ETL_Python

Proyecto educativo orientado a demostrar operaciones esenciales de ETL con Python utilizando NumPy y visualización con Matplotlib dentro de un Jupyter Notebook.

El notebook principal, `Numpy.ipynb`, cubre:
- Transformaciones con arrays de NumPy (creación, transposición, slicing y selección).
- Manejo de valores faltantes (`NaN`).
- Comparaciones y métricas básicas.
- Visualización de series de tiempo con Matplotlib.
- Carga de datos desde una URL pública (CSV) para ejercicios prácticos.

## Requisitos
- Python 3.9 o superior.
- Dependencias del archivo `requirements.txt`:
  - numpy
  - matplotlib
  - jupyterlab
  - ipykernel

Para instalar dependencias:
```
pip install -r requirements.txt
```

## Configuración recomendada (Windows/PowerShell)
1. Crear y activar entorno virtual:
   ```
   py -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```
2. Instalar dependencias:
   ```
   pip install -r requirements.txt
   ```

## Ejecutar el proyecto
- Opción 1: JupyterLab
  ```
  jupyter lab
  ```
  Luego abre `Numpy.ipynb`.

- Opción 2: Jupyter Notebook
  ```
  jupyter notebook
  ```

## Estructura del repositorio
- `Numpy.ipynb`: Notebook con ejemplos prácticos de ETL con NumPy y visualización.
- `requirements.txt`: Dependencias del proyecto.
- `README.md`: Este documento.

## Datos utilizados
El notebook carga un CSV desde una URL pública:

```
https://gist.githubusercontent.com/ahcamachod/41b8a65c5e5b58125401deafb68af460/raw/f84320f69efa1cc3e86e1db054422cfa4869c63e/manzanas.csv
```

Notas:
- Se requiere conexión a Internet para cargar el archivo directamente con `np.loadtxt`.
- El dataset contiene series temporales de precios para distintas ciudades (por ejemplo: `Moscu`, `Kaliningrado`, `Petesburgo`, `Krasnodar`, `Ekaterimburgo`).
- Hay valores faltantes (`NaN`) para practicar estrategias de limpieza.

## Contenidos del notebook
- Creación de secuencias con `np.arange` y carga de datos con `np.loadtxt`.
- Exploración de dimensiones (`ndim`) y formas (`shape`).
- Transposición de matrices (`datos.T`) y separación de columnas (`fechas`, `precios`).
- Indexación y slicing 2D con notación `[:, :]`.
- Visualización básica con `plt.plot` para múltiples series.
- Comparación de arrays (`np.array_equal`, `np.allclose`).
- Cálculo de estadísticas y manejo de `NaN`.

## Ejecución rápida
1. Clona el repositorio y entra a la carpeta del proyecto.
2. (Opcional) Crea y activa un entorno virtual.
3. Instala dependencias: `pip install -r requirements.txt`.
4. Inicia Jupyter: `jupyter lab`.
5. Abre `Numpy.ipynb` y ejecuta las celdas en orden.

## Problemas comunes
- Error al cargar el CSV: verifica tu conexión a Internet o reemplaza la URL por una copia local del archivo.
- Gráficas vacías o errores de Matplotlib: asegúrate de ejecutar las celdas que definen `fechas` y `precios` antes de graficar.
- `NaN` afectando promedios: utiliza funciones que ignoren `NaN` (por ejemplo, `np.nanmean`).

## Licencia
Este proyecto es para fines educativos. 
