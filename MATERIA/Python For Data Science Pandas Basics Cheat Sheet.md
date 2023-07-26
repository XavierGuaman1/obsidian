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