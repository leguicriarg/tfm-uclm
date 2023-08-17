# Introduccion al TFM - Cristian Leguisamon
TFM-UCLM
El trabajo parte de una serie de datos de FitBit y de un dataset de datos nutricionales de alimentos.
Mediante estimaciones, se calcula el requerimiento nutricional de cada persona.
Con ese requerimiento nutricional y teniendo el detalle del contenido nutricional de cada alimento, la idea es determinar cuáles son los alimentos mas apropiados para el usuario.

A tal fin, luego de estimar las necesidades de cada usuario en funcion de su actividad, se seleccionan los alimentos que pueden ser utilizados para cada comida.
Por ejemplo, del dataset, se seleccionan los alimentos que pueden estar asociados a desayuno, almuerzo, etc.
Luego de hacer ese filtro (con ayuda de OpenAI), utilizando distintos metodos de ML, determinamos la necesidad de nutrientes de un nuevo individuo, utilizando como parametros la edad, el peso y el consumo de calorias diario y un parametro de control (por ejemplo, Azúcar si se trata de alguien que considera necesario controlar mas detalladamente ese valor)

Posteriormente, habiendo determinado estos parametros, utilizando programacion lineal (debido a que se trata de una cuestion de restricciones), seleccionamos los alimentos que mejor se ajustan a las restricciones calculadas previamente por los modelos.
Finalmente, se obtiene una cesta de alimentos que cumplen con el valor nutricional de la persona y la cantidad de líquido que debe consumir.

En el futuro, esto puede conectarse con APIs de sitios web como Cookpad (para ver qué recetas pueden prepararse), con APIs de supermercados (para realizar pedidos) o con aplicaciones tipo Glovo.

Proximos pasos:
Mejorar los modelos
Ampliar la base de datos de comidas y nutrientes
Conexion con otras API
Deshabilitar la conexion con chat GPT y cargar los datos en la BD para mejorar la velocidad
Utilizar solo un modelo
Analizar la posibilidad de utilizar otra metodologia en lugar de programacion lineal
