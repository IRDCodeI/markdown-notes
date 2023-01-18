# ***Inteligencia Artificial***

## *Aprendizaje* 

**Paradigmas de Aprendizaje**: Mecanismos para procesar informacion nueva u entrante con el objetivo de generar nuevo conocimiento. (Aplicados en Machine Learnign)

***Agente Inteligente (caja negra)***: No se interesa conocer el interior solo la interaccion del sistema con el entorno (Saber que hace y no como lo hace)

### *Aprendizaje Supervisado*

Se busca conocer la relacion existente entre una vairiables de entrada con unas variables de salida (Aplicacion practica mas usada)

- Se busca dar a conocer al algoritmo el resulta que se desea obtener (Img de Gato, debe clasificar como clase Gato).

    - El conocimiento del algoritmo se da mediante la entrega de suficientes datos para que logre aprender o entrenar.
    
    - Supervisado viene de la entrega de resultados que esperamos que se generen "Supervicion de aprendizaje"

- Mediante observacion se genera el conocimiento: [1 = 2], [2 = 4], [3 = 6], [9 = ?] ***Observacion dice que se aplique una regla de multiplcar por 2***

### *Aprendizaje No Supervisado*

Produce conocimiento solamente de los datos que se le entregan de entrada sin necesidad de decirle los resultados esperados.

- Conjunto de datos para entrenar menos complicados de conseguir

- Busca patrones de similitud en los datos de entrada (Simbolos de lenguaje), llegan a detectar la estructura interta de los datos.

- Estrucutras conceptuales (Formas de la silla) son espacios latentes que permiten a la maquina conocer si una cosa es similar a la otra.

*Clusterizacion: Problema dentro aprendizaje no supervisado*

## ***Machine Learning***

Subdisicplina del campo de la Informatica, que busca la creacion de maquinas que puedan **imitar** (No siempre se trata de un comportamiento cognitivo) comportamientos inteligentes. (Conducir, Analizar Patrones, ...).

- *Inteligencia Artificial Debil*: Sistemas que solo pueden cumplir con un conjunto limitado de tareas.

- *Inteligencia Aritifical Furte*: Sistemas que pueden aplicarse a gran variedad de problemas y dominios diferentes.

### Categorias de Comportamientos Inteligentes

**Nota**: A veces la programacion la logica de alguna tarea se considera un ***comportamiento aparentemente inteligente***.

- **Robotica**: Capacidad de moverse y adaptarse al entorno
- **NLP** (Natural Lenguage Procesing): Capacidad de entender el lenguaje
- **Voz**: Capacidad de poder hablar y conversion de voz a texto y texto a voz

Capacidad que define a un agente inteligente es la de ***aprender o machine learning*** (Rama de IA que busca dotar a maquinas la capacidad de aprendizaje ya sea supervisado, no supervisado o reforzado). 

- Generalizacion de conocimiento a partir de un conjunto de experienzas.
- ML es un componente nuclear "Se programa para que aprenda".

`` ML != IA``

#### Tecnicas en Machine Learning:

- Arboles de descisiones
- Modelos de regresion
- Modelos de clasificacion
- Tecnicas de Clusterizacion
- Redes Neuronales (Aprende de forma gerarquica): 
    - Primeras capas aprenden conceptos concretos y las posteriores aprenden conceptos abstractos.
    - Pueden tener `n` capas de redes, lo cual a su vez dan mayor complejidad

## ***Deep Learnign***

Aprendizaje profundo, donde la complejidad de los algoritmos es mayor y complejos.

- Hace uso de la gran informacion para el entrenamiento (Big Data: Fenomeno de acumular grandes cantidades de datos).

*Tecnicas de Deep Learnign*: Version mas potente de la redes neuronales