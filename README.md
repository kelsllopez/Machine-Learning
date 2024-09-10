# Proyecto de Machine Learning: Evaluación 1

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
   - *Explicación*: Utilizamos técnicas de selección de características y análisis de correlación para identificar las variables más relevantes, como la ubicación y el tamaño de la vivienda.
   
2. **¿Cuál es la precisión del algoritmo generado?**  
   - *Explicación*: Se utilizó un modelo de regresión y la precisión obtenida fue `XX%`. Esto se evaluó utilizando un conjunto de prueba.

3. **Métricas de evaluación**:  
   - **Error Absoluto Medio (MAE)**: `XX`
   - **Error Cuadrático Medio (MSE)**: `XX`
   - **Raíz del Error Cuadrático Medio (RMSE)**: `XX`
   - **Puntaje R al Cuadrado (R²)**: `XX`

### Interpretación:
Las métricas anteriores muestran cómo el modelo de predicción se comporta en términos de error y ajuste a los datos. El valor de R² nos indica qué tan bien los datos de entrenamiento se ajustan al modelo.

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

1. **TASA DE ERROR:  0.1007**

- La tasa de error mide la proporción de predicciones incorrectas sobre el total de predicciones. En este caso el 0.10 de las predicciones son incorrectas.

**2.EXACTITUD (ACCURACY): 0.8993 **

- Explicación: El modelo tiene una exactitud del 0.89 lo que indica que el 0.89 de las veces el modelo predice correctamente si un correo es spam o no.

**3.LA MATRIZ DE CONFUSIÓN TIENE 4 CATEGORÍA:**
1. **Verdaderos Positivos (VP): 507 **Correos clasificados correctamente como spam.
2. **Falsos Positivos (FP):  69** Correos clasificados incorrectamente como spam.
3. **Verdaderos Negativos (VN): 735** Correos clasificados correctamente como no spam.
4. **Falsos Negativos (FN): 70** Correos clasificados incorrectamente como no spam.

**4.TASA DE POSITIVOS VERDADEROS (TRUE POSITIVE RATE): VALOR PARA SPAM 0.88**

- La tasa de positivos verdaderos o recuperación para la clase spam indica la proporción de correos spam que fueron correctamente identificados como spam.

**5.TASA DE POSITIVOS FALSOS (FALSE POSITIVE RATE): PRECISIÓN PARA NO SPAM 0.09 **

-  La tasa de positivos falsos indica la proporción de correos no spam que fueron incorrectamente clasificados como spam. Un valor bajo es deseable para evitar que correos legítimos sean marcados erróneamente como spam.

1. TN (Verdaderos Negativos) = 735
2. FP (Falsos Positivos) = 69
3. FN (Falsos Negativos) = 70
4. TP (Verdaderos Positivos) = 507

**FPR= 69 + 735 / 69 = 0.09**

**6.PRECISIÓN: VALOR: 0.8802**

- La precisión indica la proporción de verdaderos positivos sobre el total de positivos predichos. De todos los correos que el modelo clasificó como spam, el 0.88 realmente son spam.

**7.F1-SCORE: VALOR: 0.8794**

-  el F1-Score del 0.87 sugiere que el modelo tiene un buen equilibrio entre identificar correctamente los correos spam y minimizar los falsos positivos.

**8.LA MÉTRICA MAS ACETADA PARA MI SERIA:**

Seria el El F1-Score es una métrica que balancea la precisión y la tasa de verdaderos positivos. En el caso de un filtro de spam, los falsos positivos serian bloquear correos importantes y los falsos negativos serian permitir correos no deseados son igualmente problemáticos. El F1-Score es muy importante ya que combina precisión y la tasa de verdaderos positivos para ofrecer una visión más equilibrada del rendimiento del modelo, evitando priorizar una métrica sobre la otra.

Interpretación: Un buen valor de F1-Score indica que el modelo tiene un buen balance entre precisión y TPR, lo cual es útil en situaciones donde ambos errores deben ser minimizados.

![image](https://github.com/user-attachments/assets/343805d0-b474-454e-a73c-69ecea20c8de)

---

## Problema 3: Sistema de Recomendación de Películas 🎬

- **Objetivo**: Recomendar películas a un usuario basado en sus preferencias y las de otros usuarios.
- **DataSet**: [MovieLens 20M Dataset](https://www.kaggle.com/datasets/grouplens/movielens-20m-dataset?select=movie.csv)

### Preguntas:
1. **¿Cuál película recomendarían si se quiere ver una película de terror?**  
                           Giorgino (1994)           | Adventure|Drama|Horror             |     5.0
                   Dream Demon (1988)         |                  Horror                          |     5.0
           tales that witness madness (1973)| Comedy|Horror|Mystery|Sci-Fi   |     5.0
