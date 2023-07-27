- La biblioteca de Pandas se basa en NumPy y proporciona fácil de usar datos
Estructuras y herramientas de análisis de datos para Python
lenguaje de programación.
Utilice la siguiente convención de importación:
==importar pandas como pd==
***
<mark>Pandas Data Structures</mark>
==series==
Una matriz etiquetada unidimensional
capaz de contener cualquier tipo de datos
s = pd.Series([3, -5, 7, 4], index=[ , , , ])
![[Pasted image 20230726173324.png]]
==DataFrame==
Una etiqueta bidimensional estructura de datos con columnas
de tipos potencialmente diferentes.
![[Pasted image 20230726173435.png]]
data = { : [ , , ], : [ , , ], : [11190846, 1303171035, 207847528]} >>> df = pd.DataFrame(data, columns=[ , , ]) 'Country' 'Belgium' 'India' 'Brazil' 'Capital' 'Brussels' 'New Delhi' 'Brasília' 'Population
***
Para utilizar Pandas, primero debes instalar la biblioteca si aún no lo has hecho. Puedes instalarla utilizando el siguiente comando:

```
pip install pandas
```

Una vez que tienes Pandas instalado, puedes importarlo en tu script o notebook de Jupyter para empezar a trabajar con él:

```python
import pandas as pd
```
* * *
==EJEMPLOS==
1. Cargar datos desde un archivo CSV:

Supongamos que tienes un archivo llamado "datos.csv" que contiene datos tabulares con las columnas "Nombre", "Edad" y "Ciudad". Puedes cargar estos datos en un DataFrame de Pandas de la siguiente manera:

```python
import pandas as pd

# Cargar datos desde un archivo CSV
df = pd.read_csv('datos.csv')

# Mostrar las primeras filas del DataFrame
print(df.head())
```
***
2. Filtrar y seleccionar datos:

Puedes filtrar y seleccionar datos utilizando métodos como `loc` y `iloc`:

```python
# Seleccionar filas basadas en condiciones
filtro_edad = df['Edad'] > 30
datos_mayores_30 = df[filtro_edad]

# Seleccionar filas y columnas específicas
datos_ciudad_mayores_30 = df.loc[filtro_edad, ['Nombre', 'Ciudad']]
```
***
3. Agregar y agrupar datos:

Puedes agregar datos usando el método `groupby` y realizar operaciones de agregación como suma, promedio, etc.

```python
# Agrupar por ciudad y calcular la media de la edad en cada ciudad
datos_por_ciudad = df.groupby('Ciudad')['Edad'].mean()

# Contar el número de personas en cada ciudad
conteo_por_ciudad = df['Ciudad'].value_counts()
```
***
4. Limpieza de datos:

Pandas puede ayudarte a limpiar datos, como tratar con valores faltantes y duplicados:

```python
# Eliminar filas con valores faltantes
df_limpio = df.dropna()

# Rellenar valores faltantes con un valor específico
df_lleno = df.fillna(0)

# Eliminar duplicados
df_sin_duplicados = df.drop_duplicates()
```
***
5. Visualización de datos:

Pandas se integra con bibliotecas de visualización como Matplotlib para crear gráficos y visualizaciones:

```python
import matplotlib.pyplot as plt

# Crear un gráfico de barras para mostrar la cantidad de personas en cada ciudad
df['Ciudad'].value_counts().plot(kind='bar')
plt.xlabel('Ciudad')
plt.ylabel('Cantidad')
plt.title('Cantidad de personas por ciudad')
plt.show()
```
