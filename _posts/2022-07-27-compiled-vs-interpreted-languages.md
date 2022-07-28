---
title: Lenguajes compilados e interpretados
author: Luis E. Fajardo
date: 27-07-2022
edited: 27-07-2022
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
C:\> g++ test.cpp -o test
```
Al ejecutar el comando anterior usted está **compilando** el archivo `test.cpp`. :eyes:

#### Para recordar...
- **g++**: compilador de C++. En sistemas Windows viene dentro del paquete MinGW.
- **test.cpp**: contiene el código fuente a ejecutar.
- **-o**: indica que se deberá producir un archivo de salida. Este _flag_ espera que a la derecha se agregue el nombre del programa.
- **test**: el nombre del programa que se ha de ejecutar. 

Usted puede ejecutar el programa de la siguiente manera:
```
C:\> ./test.exe
```
> <i class="fas fa-info-circle fa-1x"></i> En Windows generalmente el sistema se encarga de agregar la extensión `.exe`.

El resultado de ejecutar el programa `test.exe` debería ser la sumatoria de las variables `number1` y `number2`.

[^1]: Esto es _lenguaje máquina_.
[^2]: Ceros y unos (0s, 1s); donde 0 significa que no hay flujo eléctrico y 1 significa un impulso eléctrico. 
[^3]: Antes de ser compilado pasa por un proceso intermedio llamado _traducción a bytecode_.