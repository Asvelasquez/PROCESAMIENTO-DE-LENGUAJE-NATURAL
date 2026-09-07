# Transformacion de texto a vectores con TFIDF

## Descripción

En el siguiente ejercicio se busca transformar textos en español en representaciones numéricas mediante TF IDF, calcular similitud del coseno y realizar una búsqueda sencilla de documentos similares.

---

## Objetivo

Implementar un proceso básico de procesamiento de lenguaje natural que permita:

Convertir textos en vectores TF-IDF, medir la similitud del coseno entre documentos y utilizar esa representación para realizar una búsqueda sencilla por contenido.

---

## Técnica utilizada

### TF-IDF

TF-IDF es una técnica que asigna un peso a cada palabra dependiendo de su importancia dentro de un documento y del conjunto de documentos.


---

## Corpus

El proyecto utiliza un corpus pequeño de 20 documentos sintéticos, relacionados con diferentes situaciones de ciberseguridad.

Las categorías utilizadas son:

* Phishing
* Malware
* Ransomware
* Vulnerabilidades
* Fuga de datos
* General

El corpus reducido permite comprender el funcionamiento del método sin la complejidad del laboratorio original.

---

## Preprocesamiento

Antes de aplicar TF-IDF se realiza un procesamiento básico:

* Conversión de texto a minúsculas.
* Eliminación de acentos.
* Tokenización mediante expresiones regulares.
* Eliminación de palabras comunes (stopwords).
* Eliminación de tokens demasiado pequeños.


## Funcionamiento

El flujo general del proyecto es:

```text
Textos
  ↓
Preprocesamiento
  ↓
Tokenización
  ↓
TF-IDF
  ↓
Vectores numéricos
  ↓
Similitud del coseno
  ↓
Búsqueda de documentos similares
```

---

## Similitud del coseno

Para comparar dos documentos se utiliza la similitud del coseno.

Un valor cercano a 1 indica una mayor similitud entre los documentos, mientras que un valor cercano a 0 indica poca similitud.

---

## Ejemplo de búsqueda

El notebook realiza una búsqueda utilizando la consulta:

```text
correo falso para robar contrasenas
```

TF IDF transforma la consulta en un vector y posteriormente calcula su similitud con los documentos del corpus.

Los documentos con mayor similitud son presentados como los resultados más relevantes.

---


## Requisitos

se puede ejecutar el notebook utilizando Google Colab

---
