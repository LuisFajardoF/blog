---
title: Lenguajes compilados e interpretados
author: Luis E. Fajardo
date: 27-07-2022
edited: 28-07-2022
category: env
layout: post
---

La diferencia entre un lenguaje compilado y uno interpretado es que un lenguaje compilado necesita de un paso adicional antes de ser ejecutado, ese paso adicional se conoce como **compilación**; la compilación traduce el código que usted ha escrito a lenguaje que el procesador puede entender[^1].

Un lenguaje interpretado, es convertido a _lenguaje máquina_[^2] a medida el código vá siendo ejecutado.

Algunos ejemplos de lenguajes compilados son: C/C++, Java[^3], Go entre otros.
Como ejemplos de lenguajes interpretados tenemos: Python, Ruby, JavaScript y muchos más.

# Ejemplo de un lenguaje interpretado

Python es un lenguaje interpretado, por lo tanto usted puede crear un archivo llamado `test.py` y ejecutar el siguiente código:

```py
number1 = 20
number2 = 30

sum = number1 + number2

print "suma: ", sum
```

El fragmento de código anterior puede ser ejecutado _(desde CMD o Terminal)_ de la siguiente manera:
```
C:\> python test.py
```
El resultado de ejecutar el archivo `test.py` debería ser la sumatoria de las variables `number1` y `number2`.

# Ejemplo de un lenguaje compilado

En un lenguaje compilado necesita de un paso adicional; para este ejemplo se utilizará C++. Usted puede crear un archivo llamado `test.cpp` y ejecutar el siguiente código:

```c++
#include <iostream>

int main(int argc, char *argv[]) 
{
    int number1 = 20;
    int number2 = 30;

    int sum = number1 + number2;

    std::cout << "suma: " << sum << std::endl;
    
    return 0;
}
```
El fragmento de código anterior puede ser ejecutado _(desde CMD o Terminal)_ de la siguiente manera:

```
C:\> g++ <source code>.cpp -o <output program>
```
> Donde `<source code>` y `<output program>` puede ser un nombre de su elección.

Al ejecutar el comando anterior usted está **compilando** el archivo `test.cpp`. :eyes:

#### Para recordar...
> - **g++**: compilador de C++. En sistemas Windows viene dentro del paquete MinGW.
> - **\<source code\>.cpp**: contiene el código fuente a ejecutar.
> - **-o**: indica que se deberá producir un archivo de salida. Este _flag_ espera que a la derecha se agregue el nombre del programa.
> - **\<output program\>**: el nombre del programa que se ha de ejecutar. 

Usted puede ejecutar el programa de la siguiente manera:
```
C:\> ./<output program>.exe
```
> <i class="fas fa-info-circle fa-1x"></i> En Windows generalmente el sistema se encarga de agregar la extensión `.exe`.

El resultado de ejecutar `<output program>.exe` debería ser la sumatoria de las variables `number1` y `number2`.

## Diferencias entre lenguajes compilados e interpretados

- El ciclo de desarrollo en los _lenguajes interpretados_ consiste en escribir el código fuente y ejecutarlo, mientras que en los _lenguajes compilados_ se necesita realizar el proceso de **compilación** cada vez que se modifica el código fuente.
- Un lenguaje interpretado se ejecuta con menor rápidez que un lenguaje compilado.
- En un lenguaje compilado, las optimizaciones a bajo nivel se le facilitan al compilador; mientras que en un lenguaje interpretado estas optimizaciones pueden ser limitadas.
- Los lenguajes compilados están optimizados para que la ejecución del programa sea rápida aunque esto represente mayor esfuerzo de parte del programador. Los lenguajes interpretados están optimizados para _"ahorrarle"_ esfuerzos al programador aunque esto represente una ligera demora en la ejecución del programa.

# Acerca de Java

Java es un lenguaje compilado, pero esa compilación se hace a un lenguaje intermedio llamado _bytecode_ que luego es interpretado por la máquina virtual de Java _(Java Virtual Machine)_. La idea de compilar a un lenguaje intermedio es para facilitar la **portabilidad**, esto quiere decir que un programa escrito en Java puede ser ejecutado en cualquier sistema operativo _(Windows, macOS, Linux)_ que tenga instalado el JRE _(Java Runtime Environment)_.

# Conclusión

La brecha entre los lenguajes compilados e interpretados se está reduciendo. Los lenguajes compilados están modificando su sintaxis para facilitarle la escritura de _código fuente_ al programador; mientras que los lenguajes interpretados están mejorando en cuanto a velocidad de ejecución. 


<hr style="border-top: 3px solid #bbb;">

[^1]: Esto es _lenguaje máquina_.
[^2]: Ceros y unos (0s, 1s); donde 0 significa que no hay flujo eléctrico y 1 significa un impulso eléctrico. 
[^3]: Antes de ser compilado pasa por un proceso intermedio llamado _traducción a bytecode_.
