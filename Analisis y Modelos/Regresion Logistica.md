## Particion Aleatoria 
---
Consiste en particionar aleatoriamente el Dataset en datos para **Training** (70%) y **Test** (30%).

## Regresion Logistica
---
Modelo de Clasificacion (*linea que separa dos clases*) basada en una funcion conocida como escalon, hiperbolica, sigmoide, paso o heaviside .

![img](https://ml4a.github.io/images/figures/sigmoid.png)

### Ecuacion de Regresion Logistica
---

$\LARGE{E(y)= \dfrac{e^{\beta_{0}+ \beta_{1}x_{1} + ... + \beta_{p} x_{p}}}{1 + e^{\beta_{0}+ \beta_{1}x_{1} + ... + \beta_{p} x_{p}}}} = P(y=1 | x_1, x_2, ... x_p)$

### Ecuacion de Regresion Estimada
--- 
$\LARGE{\hat{y}= \dfrac{e^{b_{0}+ b_{1}x_{1} + ... + b_{p} x_{p}}}{1 + e^{b_{0}+ b_{1}x_{1} + ... + b_{p} x_{p}}}} = P(y=1 | x_1, x_2, ... x_p)$

Donde: Existe una variale yuxtapuesta (contraria a la otra "dia - noche; 0 - 1").

## Interpretacion Ecuacion de Regresion Logistica
---
Se la interpreta por medio del **cociente de posibilidades** (odds ratio).
- **ODDS Ratio**: Son las posibilidades a favor de que ocurra un evento.
$\LARGE{odds = \dfrac{P(y = 1 | x_1, ... x_p)}{P(y = 0 | x_1, ... x_p}}=\dfrac{P(y = 1 | x_1, ... x_p)}{1-P(y = 1 | x_1, ... x_p)}$
- **Cociente de Posibilidades (ODDS Ratio)**: Calcula el efecto que tiene sobre la probabilidad el aumento de variables
$\LARGE{CP = \dfrac{odds_1}{odds_0}}$
- **Cociente de posibilidades**
$\LARGE{e^{\beta_i}}$ : $\LARGE{e^{b_1}}, \LARGE{e^{b_2}}$ "Cociente de posibilidades Estimados"

## Transformacion LOGIT
---
Logaritmo natural nos da una funcion lineal de las variables independiente

$\LARGE{\hat{y}= \dfrac{e^{b_{0}+ b_{1}x_{1} + ... + b_{p} x_{p}}}{1 + e^{b_{0}+ b_{1}x_{1} + ... + b_{p} x_{p}}}} = \dfrac{e^{\hat{g}(x_1,...,x_p)}}{1 + e^{\hat{g}(x_1,...,x_p)}}$

## Analisis de Regresion Logistica
---
- **Treshold**: $\LARGE{\bar{x}}=\frac{Value_{min} + Value_{max}}{n}$
- **Accuracy**: $\LARGE{\sum_{i=n}^{m}\dfrac{error_i}{m}}$
## Codigo R
--- 
```
#Regresion Logistica
x = c(3.17,3.58,1.49,2.91,0.76,3.70,5.08,2.11,2.20,4.76,7.05,3.36,3.22,6.55,0.70,1.06,4.66,0.70,1.21)
y = c(1,1,0,1,0,1,1,1,0,1,1,0,0,1,0,1,1,0,0)

regL = glm(y~x, family = binomial()) # logit o provid
summary(regL)

yest = (exp(regL$coefficients[1] + regL$coefficients[2] * x)/(1+(exp(regL$coefficients[1] + regL$coefficients[2] * x))))

treshold = mean(range(yest))
yest_r = round(yest)

#Z (Distribucion Normal)
#Divergencias ¨Cuando no es igual¨

error = (yest_r == y)

#Exactitud (Acquarice)
acc = sum(error*1)/length(error) # Bondad de ajuste

#Ciencas sociales no hay treshold >> Exactitud depende del contexto que se aplica
#Cardinalidad, deben existir misma cantidad de clases "Clases desvalanceadas"

```
