---
layout: post
title:  "A Survey of Point-of-Interest Recommendation in Location-Based Social Networks "
categories: recommender system
published: true
---

Source: <https://www.aaai.org/ocs/index.php/WS/AAAIW15/paper/viewFile/10132/10253>

En este paper se hace un resumen de los tipos de recomendación para puntos de interés en redes sociales basadas en localización, recopilando las técnicas más comunes usadas y las distintas implementaciones utilizando distintos aspectos de estos puntos de interés además de ciertas suposiciones con respecto a ellos como por ejemplo que la distancia entre dos puntos de interés afecta en si un usuario hará check-in en ambos, dentro de lo que se habla en el paper están:
* Influencia geográfica
* Influencia social
* Influencia temporal

En el trabajo se logra mostrar de manera clara las formas existentes para hacer recomendación sobre esta área, mostrando los algoritmos utilizados junto con sus ecuaciones, aunque cuando se trata de hablar de resultados no incluyen nada más que las citas correspondientes a los trabajos originales, lo cual aunque es correcto, dificulta ver de manera fácil qué tan bueno es el desempeño comparado de todos estos algoritmos, a pesar de que se enuncie que algún algoritmo obtiene mejores resultados que otro, esto no es una medida cuantitativa para que el lector aprecie, incluso no se sabe que tan comparables puedan ser estos algoritmos dependiendo de cómo se realizaron los experimentos de cada uno, pero la noción que se muestra sobre todos igual es buena para hacerse una idea preliminar.

En la parte recopilatoria de información este trabajo sirve mucho para entender el problema y cómo se están abordando las soluciones, aunque por la extensión del paper y la cantidad de información que se entrega, la parte técnica de los distintos algoritmos, si no se posee un conocimiento previo puede llegar a costar de entender todo sin tener que recurrir a los trabajos originales, ya que se hablan de muchos algoritmos como Matrix factorization, regularized matrix factorization, probabilistic matrix factorization, naive bayes, entre otros y por ende se espera que el lector los conozca o tenga alguna noción de estos.

Para finalizar, es un paper interesante aunque creo que sirve más como una investigación de lo que se ha hecho en el área hasta el momento, ya que tampoco se plantea nada nuevo, aunque tampoco es uno de los objetivos del trabajo, pero si logran llegar a conclusiones interesantes de como al agregar nueva información ya sea de contexto o suposiciones sobre los datos que se tienen, en todos los casos esto implica una mejora en las recomendaciones sobre puntos de interes.
