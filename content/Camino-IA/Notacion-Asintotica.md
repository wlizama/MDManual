# Notación Asintótica

La notación asintotica nos permite representar la complejidad, y por ende la eficiencia de un algoritmo. Podemos tomar 3 formas de notación asintótica: notación Θ grande (Theta grande), notación O grande y notación Ω grande (Omega grande).

**Θ grande**
```js
    function sumaDeEnteros(n) {
        var sum = 0;
        for (var i = 1; i <= n; i++)
            sum += i;
        
        return sum;
    }
```

**Θ (1)**
```js
    function sumaDeEnteros(n) {
        return n * (n + 1) / 2;
    }
```


## Crecimiento de funciones

+ **Constante**: Una función tiene un crecimiento "constante" si su salida no cambia con base en la entrada, la _n_. La forma fácil de identificar funciones constantes es al encontrar aquellas que no tienen _n_ en su expresión en ningún lado, o que tienen _n_<sup>0</sup>.

+ **Lineal**: Si su salida aumenta linealmente con el tamaño de su entrada. La manera de identificar funciones lineales es al encontrar aquellas en donde _n_ nunca está elevada a una potencia (aunque _n_<sup>1</sup> esta bien) o usada como unba potencia.

+ **Polinomial**: Si su salida aumenta de acuerdo con una expresión polinomial. La manera de identificar funciones polinomiales es al encontrar aquellas en donde _n_ está elevada a una potencia constante.

+ **Exponencial**: Si su salida aumenta de acuerdo con una expresión exponencial. La manera de identificar funciones exponenciales es al encontrar aquellas en donde una constante está elevada a alguna expresión que involucra a _n_.


## Notación θ grande (Big-θ)


## Notación O grande (Big-O)
Un algoritmo dura como maximo _n_ tiempo en el peor de los casos, por ende puede llegar a ser mejor mientras el tiempo final sea lo mas menor posible a el _n_ tiempo máximo.


## Notación Omega grande (Big-Ω)