2024-09-10 martes

# Proyecto de Machine Learning: Evaluación 1  &hearts;

### Realizado por:
- **Katalina Escarlet Sepúlveda López**  
- **Tamara Soledad Larenas Escobar**

---

## Descripción del Proyecto

Este proyecto aborda diversos problemas de Machine Learning utilizando algoritmos y técnicas avanzadas para resolverlos. A continuación, se presentan los problemas trabajados, los datasets utilizados y los resultados obtenidos.

---

## Problema 1: Predicción de precios de casas en California 🏡

- **Objetivo**: Predecir el precio de una casa en California basado en sus características.
- **DataSet**: [California Housing Prices](https://www.kaggle.com/datasets/camnugent/california-housing-prices)
  
### Preguntas:
1. **¿Qué características influyen más en el valor de una casa?**  
- Haciendo un análisis de regresión lineal multiple podemos ver que las variables que más influyen en el valor de una casa son:

**1. median_income (ingreso medio)**
**2. housing_median_age (edad media de la vivienda)**
**3. households (grupo de personas que residen en una unidad de casa, para una cuadra)**
**4. total_bedrooms (total de habitaciones)**
   ![image](https://github.com/user-attachments/assets/e3960ade-0bf0-4df5-ad37-ccc8c0140153)

**Todas estas variables hacen que el valor de las viviendas sea mayor y están señaladas de mayor influencia a menor, siendo mayor influyente el 1 y menor el 4.**

b)	Resultados de las métricas de evaluación:
**•	R² (R al cuadrado): 0.5667428164413046**
**•	MSE (Error Cuadrático Medio): 5773039795.389613**
**•	RMSE (Raíz del Error Cuadrático Medio): 75980.52247378675**
**•	MAE (Error Absoluto Medio): 55840.90047785081**
![image](https://github.com/user-attachments/assets/eee3e69c-2949-48b9-b633-72a8d61d1803)

- **R²:** El modelo no es completamente preciso ya que casi un 43% de la variabilidad en los precios de las casas no está explicada por estas características. Esto sugiere que hay otras variables importantes que no estamos considerando.

- **MSE (Error Cuadrático Medio)** y **RMSE (Raíz del Error Cuadrático Medio):** El modelo tiene errores significativos al predecir el valor de las casas.

- **MAE (Error Absoluto Medio): **El error absoluto de las predicciones es de unos 55,840 dólares.

**Conclusión:** Se podría mejorar estas estadísticas tomando en cuenta las variables que no se utilizaron y/o utilizando otro tipo de análisis que no sea el de “Regresión lineal multiple”.

---

## Problema 2: Clasificación de correos electrónicos como Spam 📧

- **Objetivo**: Clasificar correos electrónicos en spam o no spam usando un modelo de clasificación.
- **DataSet**: [Spambase Dataset](https://archive.ics.uci.edu/dataset/94/spambase)

### Preguntas:
1. **Justificación del modelo utilizado**:  
   - **Modelo elegido es el Árbol de Decisión.** Es un modelo de clasificación que utiliza una estructura en forma de árbol para tomar decisiones basadas en las características de los datos.
- **Justificación** es el árbol de decisión es fácil de entender y de poder interpretar. lo que permite a entender que carastericica está fluyendo en la clasificación de un correo como spam o no spam.
![image](https://github.com/user-attachments/assets/1f78a9bf-13d5-4ce7-b9dc-09631c22d957)

2. **¿Qué características afectan más en que un correo sea Spam?**  
- **char_freq _$(0.3317251157144086):** la alta frecuencia de este símbolo en un correo es un fuerte indicador de que el correo puede ser spam, ya que muchos correos spam usan símbolos de dólar para llamar la atención sobre ofertas o promociones.

- **word_freq_remove (0.16402401643589978):** la presencia de esta palabra remove, que a menudo se utiliza para ofrecer la opción de desuscribirse de correos electrónicos, es común en correos spam.

- **char_freq_! (0.08511152217429538):** la alta frecuencia de signos ! de exclamación es característica de correos que intentan captar la atención de manera agresiva, lo que es típico en los mensajes de spam.

![image](https://github.com/user-attachments/assets/0b9cfa90-6f91-44d0-9cb6-e169d1e4b160)

**3.Usar las métricas: Tasa de Error, Exactitud, Matriz de confusión, tasa de positivos verdaderos, tasa de positivos falsos, Precisión, F1-Score. Investigar cuál(es) de estas métricas es más acertada para este caso y explicar su interpretación. **

###### 1.TASA DE ERROR:  0.1007

- La tasa de error mide la proporción de predicciones incorrectas sobre el total de predicciones. En este caso el 0.10 de las predicciones son incorrectas.

###### 2.EXACTITUD (ACCURACY): 0.8993

- Explicación: El modelo tiene una exactitud del 0.89 lo que indica que el 0.89 de las veces el modelo predice correctamente si un correo es spam o no.

###### 3.LA MATRIZ DE CONFUSIÓN TIENE 4 CATEGORÍA:

1. **Verdaderos Positivos (VP): 507 **Correos clasificados correctamente como spam.
2. **Falsos Positivos (FP):  69** Correos clasificados incorrectamente como spam.
3. **Verdaderos Negativos (VN): 735** Correos clasificados correctamente como no spam.
4. **Falsos Negativos (FN): 70** Correos clasificados incorrectamente como no spam.

###### 4.TASA DE POSITIVOS VERDADEROS (TRUE POSITIVE RATE): VALOR PARA SPAM 0.88

- La tasa de positivos verdaderos o recuperación para la clase spam indica la proporción de correos spam que fueron correctamente identificados como spam.

###### 5.TASA DE POSITIVOS FALSOS (FALSE POSITIVE RATE): PRECISIÓN PARA NO SPAM 0.09

-  La tasa de positivos falsos indica la proporción de correos no spam que fueron incorrectamente clasificados como spam. Un valor bajo es deseable para evitar que correos legítimos sean marcados erróneamente como spam.

**1. TN (Verdaderos Negativos) = 735**
**2. FP (Falsos Positivos) = 69**
**3. FN (Falsos Negativos) = 70**
**4. TP (Verdaderos Positivos) = 507**
**FPR= 69 + 735 / 69 = 0.09**

###### 6.PRECISIÓN: VALOR: 0.8802

- La precisión indica la proporción de verdaderos positivos sobre el total de positivos predichos. De todos los correos que el modelo clasificó como spam, el 0.88 realmente son spam.

###### 7.F1-SCORE: VALOR: 0.8794

-  el F1-Score del 0.87 sugiere que el modelo tiene un buen equilibrio entre identificar correctamente los correos spam y minimizar los falsos positivos.

###### 8.LA MÉTRICA MAS ACETADA PARA MI SERIA:

Seria el El F1-Score es una métrica que balancea la precisión y la tasa de verdaderos positivos. En el caso de un filtro de spam, los falsos positivos serian bloquear correos importantes y los falsos negativos serian permitir correos no deseados son igualmente problemáticos. El F1-Score es muy importante ya que combina precisión y la tasa de verdaderos positivos para ofrecer una visión más equilibrada del rendimiento del modelo, evitando priorizar una métrica sobre la otra.

**Interpretación:** Un buen valor de F1-Score indica que el modelo tiene un buen balance entre precisión y TPR, lo cual es útil en situaciones donde ambos errores deben ser minimizados.

![image](https://github.com/user-attachments/assets/472656d0-d36d-4d3d-9873-d800670201e7)

---

## Problema 3: Sistema de Recomendación de Películas 🎬

- **Objetivo**: Recomendar películas a un usuario basado en sus preferencias y las de otros usuarios.
- **DataSet**: [MovieLens 20M Dataset](https://www.kaggle.com/datasets/grouplens/movielens-20m-dataset?select=movie.csv)

### Preguntas:
1. **¿Cuál película recomendarían si se quiere ver una película de terror?**
   - Recomendaría las siguientes 3 películas de terror, que tienen las calificaciones más altas:
   
| Giorgino (1994)  | Adventure - Drama - Horror  | 5.0   |
| ------------ | ------------ | ------------ |
|  Dream Demon (1988)  |  Horror   |  5.0 |
| tales that witness madness (1973)  | Comedy - Horror - Mystery - Sci-Fi   | 5.0  |

![image](https://github.com/user-attachments/assets/a0a50dae-db80-4902-a0e7-624a31223ed8)

2. **¿Qué película recomendarían si mi última película fue Toy Story?**  

  - Recomendaría las películas que estén dentro de los géneros de Toy Story y que tengan una alta puntuación en su calificación.

| Shaolin Temple 2: Kids from Shaolin (Shao Lin xiao zi) (Kids from Shaolin) (1984)  | Action - Comedy   |  5.0 |
| ------------ | ------------ | ------------ |
|**The Encounter (2010)**     | **Children - Drama**   | 5.0  |
| **The great match (2007)**    |   **Comedy** | 5.0  |

![image](https://github.com/user-attachments/assets/5cc0d1bb-f6ea-4ed2-98fe-8d42a1023c33)


---

## Problema 4: Detección de Fraude en Transacciones Bancarias 💳

- **Objetivo**: Detectar si una transacción bancaria es fraudulenta utilizando un SVM (Support Vector Machine).
- **DataSet**: [Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

### Preguntas:
**1. ¿Qué kernel sería más educado para abordar este problema? Justifique su respuesta.**
###### - El kernel RBF (Radial Basis Function) sería una buena opción para detectar fraude en tarjetas de crédito usando un modelo SVM. Aquí te explico por qué:

**1. Relaciones no lineales: **Las variables del dataset (V1 a V28) no tienen una relación directa y simple con el fraude. El kernel RBF es excelente para captar patrones complejos y no lineales en los datos.

**2. Manejo de datos complejos:** El RBF transforma los datos en un espacio más amplio, lo que ayuda a separar mejor las transacciones fraudulentas de las legítimas.

**3. Desbalance de clases:** Dado que el fraude es mucho menos común que las transacciones normales, ajustar el modelo con el kernel RBF puede ayudar a identificar mejor estas transacciones raras pero críticas.

###### En resumen, el kernel RBF es ideal porque puede manejar la complejidad y los patrones no lineales en tus datos, lo que mejora la detección de fraudes.
![image](https://github.com/user-attachments/assets/b2d3dd16-607c-4726-90d4-5b2f7cf155f0)

![image](https://github.com/user-attachments/assets/dc7007ac-1232-4ea8-ad21-1fcc16ce68ba)
![image](https://github.com/user-attachments/assets/695578e4-0460-410d-b33c-65d1960b7a21)

**1. Comparar las métricas de: Precisión, Puntaje-F1, Puntaje Recall y Exactitud, explique cual se ajusta mejor para medir la calidad del modelo y porqué **

**Resultados de las métricas:**

- **Precisión: 0.95**
El 95% de las transacciones clasificadas como fraudulentas realmente son fraudulentas. El modelo es bueno evitando falsos positivos, pero no da información completa sobre la capacidad del modelo para detectar todos los fraudes reales.

- **Recall: 0.80**
El 80% de las transacciones fraudulentas han sido correctamente identificadas, el modelo es efectivo en identificar una gran parte de los fraudes reales.

- **Puntaje F1: 0.87**
es una buena métrica general cuando es importante tanto identificar la mayoría de los fraudes (recall) como asegurar que las transacciones identificadas como fraudulentas sean en realidad fraudulentas (precisión).

- **Exactitud: 1.00**
El modelo ha clasificado correctamente el 100% de las transacciones. Aunque parece excelente, la exactitud puede ser engañosa en conjuntos de datos desbalanceados como el de detección de fraude, donde las transacciones fraudulentas son mucho menos frecuentes que las transacciones legítimas.

![image](https://github.com/user-attachments/assets/a69da6d9-1162-4af3-8cc6-161d0fe5e4c3)


**En conclusión** la métrica que seria mas precisa o se ajustaría mejor a este modelo sería la de puntaje F1 por que en problemas de detección de fraude, la mayoría de las transacciones son legítimas, lo que significa que un modelo podría tener una precisión alta solo porque clasifica casi todo como no fraudulento. Pero eso no garantiza que sea bueno detectando fraudes reales.

Por eso, el puntaje F1 es útil, ya que combina tanto la precisión como el recall. Detectar la mayor cantidad de fraudes (recall) es importante, pero también lo es evitar marcar transacciones legítimas como fraudulentas (precisión). El F1 ayuda a equilibrar amb

---

## Problema 5: Clasificación de flores utilizando un Perceptrón 🌸

- **Objetivo**: Clasificar dos tipos de flores usando un Perceptrón simple con el conjunto de datos Iris, simplificado para dos clases y dos características.
- **DataSet**: Iris Dataset (scikit-learn)

![image](https://github.com/user-attachments/assets/00331da9-8839-40e5-aa3a-d5ffc4f00ab1)
![image](https://github.com/user-attachments/assets/235cbbbd-aa8a-4dd4-8348-254384992297)
![image](https://github.com/user-attachments/assets/6bd6ada8-53d1-46d9-b4a9-713d1156e902)

---

## Conclusión ✨

A lo largo de este proyecto, abordamos una variedad de problemas utilizando diferentes técnicas de Machine Learning, desde regresión hasta clasificación y sistemas de recomendación. Evaluamos los modelos utilizando diversas métricas, y ajustamos los algoritmos para obtener el mejor rendimiento posible.

---
