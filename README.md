## LENGUAJES DE PROGRAMACION

![logo][logo1]

[logo1]:https://github.com/francisco1112/TRABAJO_LENGUAJES_ED/blob/main/Imagenes/Portada.jpg


### ¿Qué es un lenguaje de programacion?
Un lenguaje de programación es un lenguaje que los programadores utilizan para comunicarse y para desarrollar programas de software, aplicaciones, páginas webs, scripts …

### ¿Para qué sirve?
Un lenguaje de programación sirve para escribir programas que permiten la comunicación usuario-máquina.

### Categorías de los lenguajes de programación

#### NIVEL DE ABSTRACCIÓN

Un nivel de abstracción es una forma de ocultar los detalles de implementación de ciertas funcionalidades.

**Estos son sus tipos:**

**Alto nivel**: se caracteriza por expresar los algoritmos de una manera adecuada a la capacidad relacionado con el
procesamiento humano, en lugar de la capacidad con que se ejecutan las máquinas.

**Bajo Nivel**: ejercen un control directo sobre el hardware y por ello están condicionados por la estructura física de las computadoras que los soportan.

**Medio nivel**: permiten una mayor abstracción y mantiene algunas características del lenguaje de bajo nivel. El código se envía a un compilador que lo convierte al lenguaje máquina. 

### Ejemplos de nivel de Abstracción
Java, PHP, Python, Javascript, C

### FORMAS DE EJECUCIÓN

Los lenguajes se pueden diferenciar a partir de su forma de ejecutarse:

**Estos son sus tipos:**

**Compilados**: son aquellos que son convertidos directamente a lenguaje de maquina a la hora de ejecutarse, a raíz de esto son más rápidos y más eficientes.
Los lenguajes compilados necesitan de un paso de build, y cada vez que se realiza un cambio se necesita realizar los builds.

**Interpretativos**: estos lenguajes se ejecutan línea por línea cada vez que se tiene que ejecutar,son algo más lentos , pero esto con el tiempo se ha ido corrigiendo.

**Virtuales**:el código que se genera tras la compilación es un código intermedio o bytecode. Este código puede ser a su vez interpretado por una máquina virtual instalada en cualquier equipo. Tienen una ejecución lenta pero su versatilidad de poder ejecutarse en cualquier entorno los hace muy apreciados.

### Ejemplos de formas de Ejecución:
 C, C++, Erlang, Hskell, Rust, GO, PHP, Ruby, Python, JavaScript, Java y plataforma.net

#### PARADIGMA
Un paradigma es una manera o estilo de programación de software.

**Estos son sus tipos:**

**Imperativos**: Los programas consisten en una sucesión de instrucciones o conjunto de sentencias, como si el programador diera órdenes concretas. El desarrollador describe en el código paso por paso todo lo que hará su programa.

**Declarativos**: Consiste en decirle a un programa lo que tiene que hacer en lugar de decirle cómo debería hacerlo.

**Procedimentales**: Consiste en basarse en un número muy bajo de expresiones repetidas, englobarlas todas en un procedimiento o función y llamarlo cada vez que tenga que ejecutarse.

**Orientado a objetos**:es un modelo de programación que organiza el diseño en torno a datos u objetos, en lugar de funciones y lógica. Un objeto se puede definir como un campo de datos que tiene atributos y comportamiento únicos.

**Funcionales**:es aquel donde el programador especifica lo que quiere hacer, en lugar de lidiar con el estado de los objetos. Es decir, las funciones estarían en un primer lugar y nos centraremos en expresiones que pueden ser asignadas a cualquier variable.

**Logicos**: Es un Lenguaje de Programación diseñado para representar y utilizar el conocimiento que se tiene sobre un determinado dominio. Los programas en Prolog responden preguntas sobre el tema del cual tienes conocimiento.

### Ejemplos de Paradigmas
Pascal, COBOL, FORTRAN, C, C++

### EJEMPLOS DE CODIGOS

### NIVEL DE ABSTRACCIÓN

![logo][logo3]

[logo3]:https://github.com/francisco1112/TRABAJO_LENGUAJES_ED/blob/main/Imagenes/Java.png?raw=true

[java]:https://github.com/francisco1112/TRABAJO_LENGUAJES_ED/blob/main/Imagenes/Java.png

```
public class NumeroPrimos {
 
    public static void main(String[] args) {
 
        int[] numeros = {11, 19, 20, 50, 61, 100};
 
        for (int i = 0; i < numeros.length; i++) {
            if (esPrimo(numeros[i])) {
                System.out.println("El número " + numeros[i] + " es primo");
            } else {
                System.out.println("El número " + numeros[i] + " no es primo");
            }
        }
 
    }
 
    public static boolean esPrimo(int numero) {
 
        if (numero <= 1) {
            return false;
        }
 
        int contador = 0;
 
        for (int i = (int) Math.sqrt(numero); i > 1; i--) {
            if (numero % i == 0) {
                contador++;
            }
        }
 
        return contador < 1;
    }
 
}
```

![gifjava][gifjava]

[gifjava]:https://github.com/francisco1112/TRABAJO_LENGUAJES_ED/blob/main/Prueba%20de%20cadigo/java.gif

### FORMAS DE EJECUCION

![logo][logo4]

[logo4]:https://github.com/francisco1112/TRABAJO_LENGUAJES_ED/blob/main/Imagenes/PHP.jpg?raw=true

[php]:https://github.com/francisco1112/TRABAJO_LENGUAJES_ED/blob/main/Imagenes/Java.png

```
<?php

$numero = 13;

if(esPrimo($numero)){
    echo 'Es primo';
}else{
    echo 'No es primo';
}

function esPrimo($numero)
{
    if(!is_numeric($numero))
        //Comprobamos si es un número valido, ya que sino nos dara un error 500. 
        return false;
    
    for ($i = 2; $i < $numero; $i++) {
        
        if (($numero % $i) == 0) {
            
            // No es primo 
            return false;

        }

    }

    // Es primo 
    return true;
}
```
https://github.com/francisco1112/TRABAJO_LENGUAJES_ED/blob/main/Prueba%20de%20cadigo/php.mp4

### PARADIGMA

![logo][logo2]

[logo2]:https://github.com/francisco1112/TRABAJO_LENGUAJES_ED/blob/main/Imagenes/C.jpg?raw=true

[c]:https://github.com/francisco1112/TRABAJO_LENGUAJES_ED/blob/main/Imagenes/Java.png

```
#include <stdio.h>

int main() {
    int primos_por_mostrar, n, d;
    int es_primo;

    printf("Cuantos primos desea mostrar: ");
    scanf("%d", &primos_por_mostrar);

    n = 2;
    while (primos_por_mostrar > 0) {

        /* determinar si n es primo */
        es_primo = 1;
        for (d = 2; d < n; ++d) {
            if (n % d == 0) {
                es_primo = 0;
                break;
            }
        }

        /* mostrar el numero
         * y actualizar el contador */
        if (es_primo) {
            printf("%d ", n);
            primos_por_mostrar--;
        }
        n++;
    }

    printf("\n");
    return 0;
}
```
https://github.com/francisco1112/TRABAJO_LENGUAJES_ED/blob/main/Prueba%20de%20cadigo/c.mp4
