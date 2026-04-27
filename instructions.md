# Laboratorio 8. Máquinas Vectoriales de Soporte (SVM)

**Universidad del Valle de Guatemala**  
Facultad de Ingeniería  
Departamento de Ciencias de la Computación  
CC3074 – Minería de Datos  
Semestre I – 2026

---

## Introducción

La empresa **SmartStay Advisors** es una firma intermediaria que facilita la búsqueda y selección de propiedades en Airbnb para clientes corporativos y particulares.

El modelo operativo es el siguiente:

- El cliente proporciona requerimientos específicos (ciudad, presupuesto, tipo de propiedad, capacidad, duración de estancia).
- SmartStay analiza la oferta disponible y propone propiedades que optimicen precio, calidad y disponibilidad.
- Airbnb ofrece incentivos económicos a SmartStay cuando logra incrementar el nivel de ocupación de propiedades con bajo desempeño.

La empresa desea implementar modelos de minería de datos que le permitan:

1. Estimar precios competitivos.
2. Identificar propiedades con baja ocupación.
3. Comprender qué factores influyen en la ocupación y los ingresos.
4. Diseñar estrategias basadas en datos para aumentar la rentabilidad.

**Conjunto de datos a utilizar:** `listings.RData`

---

## Resultados Esperados en la Sexta Entrega

Se espera la entrega de un informe detallado donde incluya:

- Los modelos de **SVM (Support Vector Machine)** para clasificación usando la variable categórica de los precios que creó.
- Los modelos de **SVR (Support Vector Regressor)** para predicción de los precios de las casas.
- Una **comparación para estimar los precios** de las viviendas donde determine qué algoritmo funcionó mejor (Árboles de regresión, Random Forest, Bayes Ingenuo, KNN, Regresión Lineal, SVR). Compare los resultados del mejor modelo de cada uno de los algoritmos. Recuerde que, para establecer una comparación válida, es necesario comparar bajo las mismas condiciones. Mismo conjunto de datos de entrenamiento y de prueba.
- Una **comparación para estimar la categoría** de los precios de las viviendas donde determine qué algoritmo funcionó mejor (Árboles de decisión, Random Forest, Bayes Ingenuo, KNN, Regresión Logística, SVM). Compare los resultados del mejor modelo de cada uno de los algoritmos. Recuerde que para establecer una comparación válida, es necesario comparar bajo las mismas condiciones. Mismo conjunto de datos de entrenamiento y de prueba.
- Haga un **análisis para determinar si cada uno de los modelos presenta sobreajuste o no**. ¿Qué debe comparar para determinar si está sobreajustado o no?
- Como la vez anterior, le han pedido un **informe formal**, que enlace los temas usando subtítulos explicativos que mantenga al lector en un hilo conductual de los temas que aborda la consultoría. **No incluya los enunciados de las actividades de esta guía como subtítulos.**

---

## Notas

- La consultoría es en grupo, por lo que solo se tendrán en cuenta los grupos conformados por más de un especialista.
- Cada individuo será evaluado de forma individual basado en sus aportes al trabajo grupal, por lo que deben versionar el código para poder revisar las contribuciones de cada uno.

---

## Actividades

1. Use los mismos conjuntos de entrenamiento y prueba de las hojas de trabajo pasadas para probar el algoritmo.
2. Explore los datos y explique las transformaciones que debe hacerle para generar un modelo de máquinas vectoriales de soporte.
3. Use como variable respuesta la variable categórica que especifica si la casa es **barata, media o cara**.
4. Genere varios (más de 2) modelos de SVM con diferentes kernels y distintos valores en los parámetros `c`, `gamma` (circular) y `d` (en caso de que utilice el polinomial). Puede tunear el modelo de forma automática siempre que explique los resultados.
5. Use los modelos para predecir el valor de la variable respuesta.
6. Haga las matrices de confusión respectivas.
7. Analice si los modelos están sobre ajustados o desajustados. ¿Qué puede hacer para manejar el sobreajuste o desajuste?
8. Compare los resultados obtenidos con los diferentes modelos que hizo en cuanto a efectividad, tiempo de procesamiento y equivocaciones (donde el algoritmo se equivocó más, donde se equivocó menos y la importancia que tienen los errores).
9. Compare la eficiencia del mejor modelo de SVM con los resultados obtenidos en los algoritmos de las hojas de trabajo anteriores que usen la misma variable respuesta (árbol de decisión y random forest, naive bayes, KNN, regresión logística). ¿Cuál es mejor para predecir? ¿Cuál se demoró más en procesar?
10. Genere una tabla comparativa que permita determinar el sobreajuste de todos los modelos hasta el momento (árbol de decisión y random forest, naive bayes, KNN, regresión logística). ¿Qué parámetros debe comparar para determinar si un modelo está sobreajustado o no en tareas de clasificación?
11. Genere un buen modelo de regresión, use para esto la variable del precio de la casa directamente. Tunee el modelo.
12. Compare los resultados del modelo de regresión generado con los de hojas anteriores que utilicen la misma variable, como la de regresión lineal, el árbol de regresión, naive bayes, KNN.
13. Genere un informe de los resultados y las explicaciones.

---

## Evaluación

> **Nota:** Tiene que poderse comprobar su aporte al trabajo grupal a través de commits. Si no existen al menos 3 commits con su aporte significativo no va a tener nota de la hoja de trabajo. Utilice una herramienta que permita registrar los aportes de cada uno.  
> Debe entregar los avances durante el período de clase para poder tener derecho a la calificación de la entrega.

| Puntos | Criterio |
|--------|----------|
| 20 pts | Análisis de los modelos generados. Explique todos los razonamientos. Uso de las métricas correctas. |
| 20 pts | Comparación del modelo de regresión con los modelos de regresión de las entregas pasadas. Elección del mejor modelo hasta el momento basado en métricas adecuadas. |
| 10 pts | Tuneo de parámetros. Se probó con varios valores para los hiperparámetros. Se explican los resultados. |
| 20 pts | Matriz de confusión de cada modelo de clasificación. Explicación de los resultados obtenidos. Selección del mejor modelo usando las métricas adecuadas. Análisis de otras métricas además del accuracy para los modelos generados. |
| 10 pts | Comparación del modelo de clasificación de SVM con el mejor modelo de clasificación de todas las entregas pasadas. Elección del mejor modelo de clasificación basado en las métricas adecuadas. |
| 10 pts | Comparación del ajuste del modelo de clasificación de SVM con el ajuste del mejor modelo de clasificación de todas las entregas pasadas. ¿Cuál modelo tiende a sobreajustarse? |
| 10 pts | El informe de resultados está bien redactado, se establece una continuidad lógica en las explicaciones y el análisis de los modelos. Tiene un hilo conductor claro que no pierde al lector y no tiene las actividades de esta guía como subtítulos. |

---

## Material a Entregar

- Archivo `.r` o `.py` con el código y hallazgos comentados.
- Link de Google Docs con las conclusiones y hallazgos encontrados. Puede usar también Jupyter Notebooks o `.rmd`.
- Vínculo del repositorio usado para trabajar la hoja de trabajo.

---

## Fechas de Entrega

- **PASAPORTE:** Puntos del 1 al 7 de la sección de actividades — viernes, 24 de abril a las 17:20.
- **ENTREGA FINAL:** domingo, 26 de abril a las 23:59.