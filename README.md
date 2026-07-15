# Proyecto: Aprendizaje Máquina - Casos de Aplicación
Este repositorio contiene el desarrollo de tres casos prácticos de aprendizaje no supervisado y reducción de dimensionalidad, correspondientes a la evaluación del curso.
**Estudiante:** JUAN ARTEMIO LIPE MACHACA  

---
## 📹 Explicación en Video (Máx. 12 minutos)
Puedes ver la explicación detallada y el funcionamiento del código en el siguiente enlace:
👉 https://drive.google.com/file/d/1B0Qtm30WlCoZU9H4iGLYF1JHUUEEU1hw/view?usp=sharing
---
## 📋 Contenido del Proyecto
### 1. Clustering Jerárquico
*   **Caso Resuelto:** Agrupamiento de documentos de texto del dataset "20 Newsgroups" de scikit-learn (categorías *misc.forsale*, *sci.electronics* y *talk.religion.misc*), con el objetivo de identificar de forma no supervisada agrupaciones de artículos con contenido temático similar.
*   **Explicación:** Se vectorizaron los textos mediante TF-IDF y se aplicó clustering jerárquico aglomerativo probando al menos dos criterios de enlace (linkage) distintos —Ward y Average—, evaluando los resultados con métricas como el índice de Silueta y el ARI (Adjusted Rand Index) frente a las categorías reales. Se determinó el número de clusters mediante el análisis del dendrograma y se identificó qué criterio de enlace obtuvo mejor desempeño, analizando además las palabras más representativas de cada grupo resultante.

### 2. Análisis de Componentes Principales (PCA)
*   **Caso Resuelto:** Sistema de reconocimiento de rostros basado en Eigenfaces, utilizando el dataset "Olivetti Faces" de scikit-learn (400 imágenes de 40 personas distintas).
*   **Explicación:** Se aplicó PCA sobre las imágenes de los rostros (con whitening) para obtener las Eigenfaces, reduciendo la dimensionalidad de 4096 píxeles a un espacio de componentes principales que retiene más del 95% de la varianza total. Cada rostro se proyectó a este espacio reducido y se implementó un clasificador de vecino más cercano (1-NN) —el enfoque clásico de Eigenfaces— además de un SVM como comparación, sin utilizar redes neuronales. Se evaluó la precisión del reconocimiento y se analizó el efecto del número de componentes principales sobre el desempeño del sistema.

### 3. Factorización de Matrices No Negativas (NMF)
*   **Caso Resuelto:** Sistema de recomendación de artículos similares para un periódico en línea, a partir del dataset "20 Newsgroups" utilizado como conjunto de artículos de distintas secciones (ciencia, salud, deportes, autos, tecnología y política internacional).
*   **Explicación:** Se aplicó NMF para descomponer la matriz TF-IDF de los artículos en una matriz de temas latentes (W) y una matriz de palabras clave por tema (H), obteniendo 8 temas interpretables. Cada artículo quedó representado por su distribución de temas, y se construyó un motor de recomendación basado en similitud de coseno sobre este espacio reducido, capaz de sugerir artículos temáticamente similares tanto para artículos existentes como para artículos nuevos. Se validó el sistema comparando la precisión de las recomendaciones frente a las secciones reales de los artículos.

