# Estadística
## Descriptiva
Parametros: 
1. Medidas de posición
   1. Medidas de tendencia central o centralización
      1. Media muestral o media aritmetica
      2. Moda
      3. Mediana
   2. Medidas de posición no central
      1. Cuantiles
      2. Cuartiles
      3. Percentiles
2. Medidas de dispersión
   1. Medidas de dispersion absolutas
      1. Recorrido o rango
      2. Desviaciones medias
      3. Varianza
      4. Desviacion estandar
      5. Media
   2. Medidas de dispersion relativa
      1. Coeficiente de variacion de Pearson
      2. Coeficiente de apertura
      3. Recorridos relativos
      4. Indice de desviacion respecto a la mediana
3. Medidas de forma
## Probabilidad
### Teorema de Bayes

### Distribución normal
Está caracterizada por dos parámetros: la media $\mu$ y la desviación estándar $\sigma$

#### La funcion de densidad de probabilidad de la distribución normal: 
> $N(\mu,\sigma) = P(x)=\frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{(x-\sigma)^{2}}{2\sigma^{2}}}$
* La probabilidad de que la variable aleatoria caiga en una región específica del espacio de posibilidades
* Podemos obtener la funcion de distribución $F(x)$ integrando la funcion de densidad de probabilidad, de modo que la probabilidad de una variable aleatoria normal X en un intervalo $a\leq x \leq b$ es: 
  > $P(a\leq x \leq b)=F(b)-F(a)=\frac{1}{\sigma\sqrt{2\pi}}\int_{-\infty}^{x} e^{-\frac{(v-\sigma)^{2}}{2\sigma^{2}}}\,dv$
#### Interpretación probabilistica
* Entre la media y dos desviaciones estandar, existe el 95% de la población. 

#### Tipificación (Standardization)
Dada una variable de media $\mu$ y desviacion estandar $\sigma$, se denomina valor tipificado $z$, de una observacion $x$, a la distancia (con signo) con respecto a la media, medido en seviaciones estandar, es decir:
  > $z = \frac{x-\mu}{\sigma}$ -- En ingles: Standard Score

* En el caso de la variable X normal, la interpretación es clara: asigna a todo valor de $N(\mu,\sigma)$, un valor $N(0,1)$ que deja exactamente la misma probabilidad por debajo. 
* Nos permite asi comparar entre dos valores de dos distribuciones normales diferentes, para saber cual de los dos es mas extremo. 
* Distribuciones diferentes, con diferentes escalas
* Lo que queremos hacer es tomar el rango de valores que queremos encontrar la probabilidad, y encontrar la unidad tipificada (Standard Score) del limite de este rango, luego buscamos la probabilidad de este valor usando una tala de probabilidad normal. 
* Lo que se hace aca es mover la media a que sea 0, y que la desviacion estandar sea 1. 

## Estadística Inferencial
### Distribución Muestral
#### Muestreo probabilístico
1. Muestreo aleatorio simple
   * Todos los elementos de la muestra tienene la misma probabilidad de aparición. 
2. Muestreo estratificado
   * Se divide la poblacion en difeerentes subpoblaciones, en funcion de cierta caracteristica relevante, y despues es un muestreo aleatorio simple de cada estrato. 
   * Cada individuo solo puede pertenecer a un estrato, y cada individuo del estrato debe tener la misma probabilidad de ser elegido. 

#### Teorema del Límite Central
Dada una poblacion de media $\mu$ y desviacion estandar $\sigma$, no necesariamente normal, la distribucion de las media de las muestras de tamaño $n$:
* Tienen la misma media $\mu$ que la población
* Su desviacion estandar es $\frac{\sigma}{\sqrt{n}}$ y, por consiguiente, disminye al aumentar $n$
* Cuando $n\geq 30$ es practicamente normal


Condiciones
* Es importante señalar que este teorema es valido cualquiera que sea la distribucioon de la poblacion
* El grado de aproximacion de la distribucion de las medias muestrales a la correspondiente normal depende del tipo de poblacion de partida y del valor de $n$
* Si la poblacion de partida es normal, tambien lo sera la distribucion de las medias muestrales, cualquiera que sea el valor de $n$
* Auqnue la poblacion de partida no sea normal, la distribucion de las medias muestrales puede ser muy parecida a la normal, incluso para valores pequeños de $n$, pero para $n\geq 30$ es seguro que se consigue una gran aproximacion a la normal cualquiera que sea la distribucion de partida

Consecuencias / Ventajas
* Control de las medias muestrales
  * En una población de media $\mu$ y desviación típica $\sigma$, nos disponemos a extraer una muestra de tamaño $n$. Antes de hacerlo, sabemos que la distribución de las medias $x$, de todas las posibles muestras es normal, con media $\mu$ y desviación típica $\frac{\sigma}{\sqrt{n}}$, por tanto, podemos averiguar la probabilidad de que la media de una muestra concreta esté en un cierto intervalo
* Inferir la media de la población a partir de una muestra
  * Esta es la aplicación más importante del Teorema del Límite Central.
  * A partir de una muestra se pueden extraer conclusiones válidas sobre la media de la población de partida

#### Distribucion muestral de un estadistico
Supongamos que tenemos una variable aleatoria, cuya distribucion es $f(x)$

Supongamos, que por simplicidad, que obtenemos una muestra aleatoria simple con tamaño $n$

Entonces, un estadistico es cualquier funcion h definida sobre ${x_1, x_2, x_3,..., x_n}$ y que no incluye parametro desconocido alguno

$Y=h({x_1, x_2, x_3,..., x_n})$

La distribucion de dicho estadistico $Y$ la vamos a denominar $g(y)$. 

Distribucion muestral de un estadistico
* $f(x)$ es la distribucion de la poblacion
* $g(y)$ es la distribucion del estadístico que tenemos

Es vital conocer la distribucion muestral del estadistico de interes para poder efectuar inferencias sobre el parametro correspondiente. Esto es par aefectuar inferencias sobre la media poblacional $\mu$, necesitamos conocer la distribucion muestral de $\bar{X}$

##### Distribucion muestral de la media
* Media
  > $\mu$
* Varianza
  > $\frac{\sigma^2}{n}$
* Desviacion estandar
  > $\frac{\sigma}{\sqrt{n}}$
### Estadistica Deductiva. Contrastes de hipotesis
Plantear hipotesis sobre la poblacion y el uso de los datos de una muestra para saber si son aceptables o no. 
### Estadistica Inductiva. Estimacion de parametros
Buscar estadisticos muestrales que puedan considerearse buenos estimadores de los parametros poblacionales. 
#### Estimación
Algunos parametros de interes:
* Media
* Varianza
* Proporción

Cualquier estadístico de la muestra que se utilice para estimar  un parámetro poblacional desconocido  se conoce como estimador.

Es decir, un estimador de un parámetro poblacional es una variable aleatoria que depende de la información de la muestra y cuyas realizaciones proporcionan aproximaciones al valor desconocido del parámetro.

La media de la muestra $\hat{X}$ puede ser un estimador de la media de la poblacion $X$, la propocion de la muestra $\hat{p}$ puede ser un estimador de la proporcion poblacional $p$. 

##### Estimación puntual
Un estimador puntual de un parametro poblacional es una funcion de la muestra que da como resultado un unico valor. 

Criterios para seleccionar estimadores:
* Insesgado: si la media de su distribución es igual al verdadero valor del parámetro.
* Eficiente: Si posee menor varianza
* Consistente: Si a medida que el tamaño de la muestra aumenta el estimador se aproxima a su valor verdadero
* Suficiente: Si reúne la máxima cantidad de información posible.

##### Estimación por Intervalos
Una Estimación por Intervalos especifica el rango dentro del cual está el parámetro desconocido.

Tal intervalo con frecuencia va acompañado de una afirmación sobre el nivel de confianza que se da en su exactitud

###### Intervalo de confianza
Rango de valores que probablemente incluyan un valor de población con cierto grado de confianza. 

Intervalo de Confianza para la media  de una distribución normal; variancia poblacional conocida. $n\geq 30$

Calculo de intervalo de confianza
* Estadístico +/- margen de error

Calculo de intervalo de confianza para distribucion normal
> $IC_\alpha = \bar{x}\pm Z_\frac{\alpha}{2} \frac{\sigma}{\sqrt{n}}$

Calculo de intervalo de confianza para distribución binomial
> $IC_\alpha = \bar{x}\pm Z_\frac{\alpha}{2} \sqrt{\frac{p_s q_s}{n}}$

###### Distribución t
Condiciones
1. La muestra es pequeña, menor de 30
2. $\sigma$ es desconocida
3. La población es normal o casi normal

Tipificación de una distribución T
> $t = \frac{\bar{X}-\mu}{\frac{s}{\sqrt{n}}}$

Calculo de intervalo de confianza para distribucion normal
> $IC_\alpha = \bar{x}\pm Z_\frac{\alpha}{2} \frac{s}{\sqrt{n}}$

#### Prueba de hipotesis
Una hipótesis estadística es una aseveración o conjetura respecto a una o más poblaciones.

Se asume que la hipotesis nula es verdad. Solo si hay suficientes pruebas en su contra, se rechaza y se acepta la hipotesis alterna. 

Pasos:
1. Decidir la hipotesis nula y alternativa
   * Igualdad
      > $H_0: \bar{X}=\mu$
      
      > $H_1: \bar{X}\neq\mu$
2. Elegir el nivel de significancia (0.05 o en su forma 5%)
3. Determinar la zona de aceptacion y rechazo
4. Determinar la funcion pivotal
5. Calculo de funcion pivotal

Nivel de significancia
* La probabilidad de rechazar la hipótesis nula cuando es verdadera.