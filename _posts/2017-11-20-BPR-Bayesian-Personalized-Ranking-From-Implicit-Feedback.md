---
layout: post
title:  "BPR: Bayesian Personalized Ranking from Implicit Feedback"
categories: recommender system
published: true
---

Source: <https://arxiv.org/pdf/1205.2618>

En este paper se explica el metodo de rankeo personalizado usando inferencia Bayesiana, donde los autores primero hablan de trabajos relacionados para información implícita en el tiempo de publicación del trabajo, con respecto a recomendación están collaborative filtering mediante k-nearest-neighbors o Matrix Factorization, y en el área de rankeo mencionan el trabajo de Burges et al. en el que entrenan una red neuronal para rankear usando descenso del gradiente.

En la explicación de como funciona el algoritmo además agregan que este puede ser utilizado en conjunto a las técnicas state-of-the-art de recomendación para aprender los parámetros de cada modelo para obtener mejores resultados, en el caso de KNN, la medida de similaridad sería agregada a los parámetros del modelo, y en Matrix factorization se hace lo mismo, al usar LearnBPR para aprender el estimador del modelo.

La metodología de evaluación encuentro que se podría mejorar, al usar leave-one-out por usuario y de acuerdo a lo que entendí, se realizó 10 veces esto, lo cual puede ser un poco sesgado, mucho mejor hubiera sido haber hecho cross-validation ya que llevar a cabo leave-one-out para todos los items de los usuarios es muy demandante en cómputo.

Se puede concluir que el sistema propuesto por los autores es una buena forma para poder incluir en modelos donde no hay aprendizaje de parámetros y así poder mejorarlos redefiniendo la función a optimizar, lo que se pudo ver claramente en la comparación de los modelos sin uso de BPR versus la inclusión de este, especialmente al aumentar las dimensiones utilizadas.