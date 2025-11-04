# Examen Parcial - DaniArroyo07

**Usuario GitHub:** DaniArroyo07
**Fecha:** 4 de noviembre de 2025
**Retos tenidos en cuenta:** Reto 003

---

## Instrucciones

A continuación encontrarás fragmentos de código extraídos de tus entregas. Cada fragmento contiene una o más situaciones relacionadas con los conceptos vistos en clase.

Para cada pregunta debes:
1) Identificar a qué se refiere la observación
2) Explicar si es o no un error y por qué
3) Proponer la corrección

Nota: Responde 5 de las 10 preguntas (en función a lo indicado en el examen).


---

## Pregunta 1

Archivo: `HotelLuces.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/0940bca38a3852dfc71939340aea56c2d6eddd4b/entregas/arroyosanchezdaniel/HotelLuces.java) (Reto 003)

```java
final String VENTANA_CERRADA = ":[ ]:";
final String LUZ_APAGADA = ":[º]:";
final String LUZ_ENCENDIDA = ":[*]:";
```

¿Qué observas en este código?
---

## Pregunta 2

Archivo: `HotelLuces.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/0940bca38a3852dfc71939340aea56c2d6eddd4b/entregas/arroyosanchezdaniel/HotelLuces.java) (Reto 003)

```java
for (dia = 1; dia <= 6; dia++) {
    int consumoPorDía = 0;
    for (horas = 0; horas < 24; horas++) {
        // ...
    }
}
```

¿Qué observas en este código?
---

En este fragmento de código, encontramos dos bucles del tipo for, donde vemos tanto el bucle del entero "día" (int dia = 1;) y la de int horas.
Vemos además declarado otra variable del tipo entero llamado "consumoPorDía" escrito en PascalCase. Sin embargo esta variable no es utilizada en ningún momento por lo que esta variable sería mejor si fuera quitada del código para liberar espacio y hacer más legible el código.

---
## Pregunta 3

Archivo: `HotelLuces.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/0940bca38a3852dfc71939340aea56c2d6eddd4b/entregas/arroyosanchezdaniel/HotelLuces.java) (Reto 003)

```java
if (probVentanaAbierta >= 0.7) {
    if (numeroHabitaciones != 4) {
        System.out.print(VENTANA_CERRADA);
    }
} else if (probVentanaAbierta < 0.7 && probLuzEncendida >= 0.6) {
    if (numeroHabitaciones != 4) {
        System.out.print(LUZ_APAGADA);
    }
} else if (probVentanaAbierta < 0.7 && probLuzEncendida < 0.6) {
    if (numeroHabitaciones != 4) {
        System.out.print(LUZ_ENCENDIDA);
    }
}
```

¿Qué observas en este código?

Nos encontramos ante un fragmento de código, donde como podemos ver declara una condición para saber si una ventana esté abierta o cerrada. En este código nos encontramos con varios fallos, o aspectos a mejorar. 
Para empezar vemos que se declara la condición de que si la probabilidad de que las ventanas estén abiertas ocurra algo, sin embargo, a pesar de que la ventana o la persiana esté abierta o arriba, puede ocurrir que la luz de la habitación esté encendida, teniendo que añadir a esta parte la posibilidad de que la luz esté encendida o apagada.
Por otra parte, encontramos una forma de poder resumir el código. En vez de poner los "else if", tenemos la capacidad de sustituirlos por "else" sin necesidad de indicar las dos opciones de la luz, y dentro de este else, añadir una condicional más donde encontramos tanto la opción de luz encendida como de apagada.

---

## Pregunta 4

Archivo: `HotelLuces.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/0940bca38a3852dfc71939340aea56c2d6eddd4b/entregas/arroyosanchezdaniel/HotelLuces.java) (Reto 003)

```java
for (plantas = 7; plantas >= PLANTA_BAJA; plantas--) {
    for (numeroHabitaciones = 1; numeroHabitaciones <= 7; numeroHabitaciones++) {
        // ...
    }
    System.out.print(SEPARADOR + "P" + plantas);
}
```

¿Qué observas en este código?

---

## Pregunta 5

Archivo: `HotelLuces.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/0940bca38a3852dfc71939340aea56c2d6eddd4b/entregas/arroyosanchezdaniel/HotelLuces.java) (Reto 003)

```java
System.out.println("Día: " + dia + ". Hora: " + horas);
```

¿Qué observas en este código?

En este código encontramos ante la impresión de una línea, la cual añade un salto de línea al finalizar esta. En esta línea de código no encontramos ningún fallo grande, sin embargo podemos modificarlo, para una mayor comprensión del código:

Este fallo se trata, de estar imprimiendo en todo momento el día en que nos encontramos, lo cual no es necesario, se puede hacer que cuando entremos en un día nuevo no haga falta estar imprimiendo todo el rato el día. La mejora para este código que podemos implementar es poner el día y las horas en fragmentos distintos, uno cuando empiece una nueva hora y el otro al empezar un nuevo día.

---

## Pregunta 6

Archivo: `edificio.java` — [PRs del alumno](https://github.com/mmasias/25-26-PRG1/pulls?q=is%3Apr+author%3ADaniArroyo07+is%3Aall) (Reto 003, línea 4)

```java
final double PERSIANA_CERRADA = 0.6;
```

¿Qué observas en este código?

---

## Pregunta 7

Archivo: `edificio.java` — [PRs del alumno](https://github.com/mmasias/25-26-PRG1/pulls?q=is%3Apr+author%3ADaniArroyo07+is%3Aall) (Reto 003, línea 10)

```java
final String separador = "[    ]";
```

En esta parte de código nos encontramos declarando una variable de tipo String, llamada "separador". Si hubiera sido un String sin ser declarado final, a pesar de ser funcional el código, hay un fallo de sintaxis. Una variable final provoca que el código no se pueda cambiar de forma posterior, y en estos casos al llamar la variable "separador" debería haber sido en SCREAMING_SNAKE_CASE, donde la palabra debería haberse encontrado en mayúsculas.

¿Qué observas en este código?

---

## Pregunta 8

Archivo: `edificio.java` — [PRs del alumno](https://github.com/mmasias/25-26-PRG1/pulls?q=is%3Apr+author%3ADaniArroyo07+is%3Aall) (Reto 003, línea 1)

```java
public class edificio {
```

¿Qué observas en este código?
---

En este fragmento de código, encontramos la creación de la clase "edificio", la cual se trata de una clase pública. A pesar de que el código es funcional, nos encontramos con un fallo y un aspecto a mejorar:

El fallo que encontramos en este código, es la parte de la asignación del nombre de la clase, es decir, "edificio". Este nombre a pesar de que el código funcione con él, su sintaxis está mal escrita, debido a que este debería haber sido escrito en CamelCase, la cual hace que todas las palabras empiecen por mayúscula, y las letras siguiente sean en minúscula --> Debería haber sido escrito como: "Edificio".

El aspecto que debemos cambiar, es la declaración de la clase pública. Este no provoca un fallo grande en el código, sin embargo no hay ninguna necesidad de declararlo público, por lo que podríamos directamente poner: "class Edificio {}"

---

## Pregunta 9

Archivo: `edificio.java` — [PRs del alumno](https://github.com/mmasias/25-26-PRG1/pulls?q=is%3Apr+author%3ADaniArroyo07+is%3Aall) (Reto 003, líneas 15-16)

```java
for (int fila = 1; fila <= 7; fila++) {
    for (int columna = 1; columna <= 6; columna++) {
```

¿Qué observas en este código?

---

## Pregunta 10

Archivo: `edificio.java` — [PRs del alumno](https://github.com/mmasias/25-26-PRG1/pulls?q=is%3Apr+author%3ADaniArroyo07+is%3Aall) (Reto 003, línea 19)

```java
System.out.print(!abierta ? VENTANA_CERRADA: encendida ? VENTANA_CON_LUZ_ENCENDIDA : VENTANA_CON_LUZ_APAGADA);
```

¿Qué observas en este código?

