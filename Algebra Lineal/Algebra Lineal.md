*Base de muchas apilcaciones informaticas (Redes Neuronales, Big Data, ...) con ayuda de las matrices* 
- Rama de la matematicas que tiene como estudio los vectores, matrices y espacios vectoriales. 


## Vectores
---
**Concepto General**: Forma de asociacion a un ente especifico varias caracteristicas:  $x=[1, Stalin, 10.04]$. Pueden poseer numeros reales $1,2,3$ o numeros complejos $\sqrt{2}$ 

**Concepto Fisico y Matematico:** Ente matemático como la recta o el plano el cual se representa mediante un segmento de recta, orientado dentro del espacio euclidiano tridimensional.


## Vector Rn
---
$Rn$ es el conjunto de todos los vectores con $n$ componentes ($x1,x2,x3,...,xn$ ) donde cada $x_i$ pertenece a los reales.
- $Rn$ viene a ser considerado el numero de dimensiones de un vectores.

## Componentes de un Vector
- Vector Renglon: ($x1,x2,x3,...,xn$) 
- Vector Columna: $\begin{pmatrix} x1 \\ x2\\ x3\end{pmatrix}$

***Ejemplo*** 
- $(1,2) \epsilon \mathbb{R}^2$  "Vector de dos dimensiones"
- $(1,2,3) \epsilon  \mathbb{R}^3$  "Vector de tres dimensiones"


## Matriz (Arreglo)
---
Conjunto o combinacion de $n$ vectores ya sea **renglon** o **columna**.

***Ejemplo*** 
$V_1 = (1,2)$ 
$V_2 = (3,4)$ 

$$
V_1 + V_2 = \begin{pmatrix} 1 & 2\\  3 & 4 \end{pmatrix} \epsilon M_{(2x2)}
$$ 

## Espacios Vectoriales
---
Reglas aplicadas para los vectores agregados en una matriz.

$V (Campo Vectorial)$ sobre campo $F (Numeros Reales)$ se aplican dos operaciones **"suma y multiplicacion por escalares"** y cerrado bajo esas operaciones.
$\forall_{x,y} \epsilon V$ debe existir $x+y \epsilon V$ (Cerradura)
$a.x \epsilon V$ debe ser $\forall x \epsilon V$
- $\forall$ : Para todos los valores
*Cerradura*: 
- Si $x+y$ son numeros relaes la sumatoria continua siendo un real.
- Si $a.x$ se multiplica por los escales $x$ permanece dentro del espacio vectorial.

**Reglas para Espacio Vectoriales:**
$\forall_{x,y,z} \epsilon {V}$ (Para toda x,y,z que estan en el espacio Vectorial)

-  $x+y = y+x$ "Conmutativa"
- $(x+y)+z = x+(y+z)$ "Asociativa"
- $\exists 0 \epsilon V$ de manera que $x+0 = x$ "Neutro en la suma" ($1+0 =1$)
- $x \epsilon V \rightarrow \exists y \epsilon V$ tal que $x+y=0$  "Existen un inverso en los numero" ($5+(-5)=0$)
- $\forall x \epsilon V \rightarrow 1*x=x : (1 \epsilon F)$ "$1$ es el neutro de $F$ (Campo)"
- $(ab)x=a(bx) : a,b \epsilon F$ "Asociativa por multiplicacion por escalares"
- $a(x+y)=ax+ay$ "Distributiva"
- $(a+b)x = ax+bx$ "Distributiva sobre $F$"

**Operaciones con Vectores**
- Suma de 2 vectores componente a componente
$(1,2,3) + (4,5,6) = (5,7,9) \epsilon \mathbb{R}^3$
- Multiplica de un vector por un elemento o numero "Multiplicacion por escalares"
$5(1,2,3) = (5,10,15)$
- Producto escalar o Proudcto Interior $<u.v>$
$u = (a_1,b_1)$
$v=(a_2,b_2)$ 
$u.v=a_1a_2+b_1b_2$ 
## Subespacios Vectoriales
---
Subconjunto determinado de elementos elegidos del espacio vectorial que cumple con las reglas generales y cumplen la propiedad de **cerradura**.

## Norma de un Vector 
--- 
***Parte de un vector:*** Direccion, Magnitud, Sentido y angulo
![Vector](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c4/Vector_00.svg/1024px-Vector_00.svg.png)

Modulo o Magnitud: $|u| = \sqrt{a^2+b^2}$ 
- Espacios mas grandes (Norma del vector): $||u|| = \sqrt{<u,u>}$ 

***Traslacion de un vector:*** Mover el punto de aplicacion de un vector a otra ubicacion en el plano.

![Vector de Traslacion](https://economipedia.com/wp-content/uploads/Captura-de-pantalla-2022-01-08-a-les-12.50.35.png)

***Angulo de un vector***
![Angulo del vector](https://miprofe.com/wp-content/uploads/2016/03/angulo-entre-dos-vectores.png)
$cos \theta = \frac{u.v}{|u||v|}$

## Angulos entre vectores
---
***Ortogonales:*** Angulos entre vectores forman $90^{\circ}$ 
- Vectorial: $u.v=0=<u,v>$
- Funcion: $<f,g> = \int_{a}^{b} f(t)g(t)dt$
![Vectores Ortogonales](https://miprofe.com/wp-content/uploads/2016/03/vectoresortogonales.png)


## Combinaciones Lineales y Generado
---
