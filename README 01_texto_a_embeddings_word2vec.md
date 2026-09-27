# Transformacion de texto en embeddings con Word2Vec

Ejercicio de procesamiento de Lenguaje Natural, se convierte texto en español
en representaciones numericas densas embeddings usando Word2Vec, implementado con
TensorFlow y Keras segun el esquema skip-gram con muestreo negativo.

## Abrir en Colab

Sube `01_texto_a_embeddings_word2vec.ipynb` a Google Colab y ejecuta todas las celdas.
No hace falta descargar datos: el corpus se genera dentro del propio cuaderno. El
entrenamiento tarda alrededor de medio minuto.

## objetivo

Word2Vec parte de que las palabras que aparecen rodeadas de las mismas palabras tienden a
significar cosas parecidas, el modelo aprende a distinguir pares de palabras que si
aparecen juntas en el texto de pares inventados al azar, y para resolver esa tarea acaba
asignando vectores parecidos a las palabras intercambiables.

El corpus se genera con plantillas y ranuras de sinonimos, de modo que se sabe de antemano
que palabras deberian parecerse. Eso da un criterio objetivo para evaluar el resultado.

## Contenido del notebook

| Seccion | Tema |
|---|---|
| 1 | Librerias y semilla |
| 2 | Corpus generado con plantillas y sinonimos |
| 3 | Preprocesamiento |
| 4 | TF-IDF como punto de partida |
| 5 | Word2Vec con Keras: skipgrams y las dos capas Embedding |
| 6 | Entrenamiento y consulta de los vectores |
| 7 | Similitud entre terminos |
| 8 | Vectores de documento y busqueda |
| 9 | Conclusiones |

## Datos del ejercicio

- 900 documentos, 111 palabras distintas
- 162.096 pares de entrenamiento generados con skipgrams
- Red de 11.100 parametros: 111 palabras x 50 dimensiones x 2 capas
- 20 epocas, lotes de 256, optimizador Adam
- Perdida de 0,4260 a 0,1226

## Resultado

Los vecinos mas proximos que aprende el modelo reproducen los grupos de sinonimos del
generador, sin que ninguna etiqueta se lo haya indicado:
