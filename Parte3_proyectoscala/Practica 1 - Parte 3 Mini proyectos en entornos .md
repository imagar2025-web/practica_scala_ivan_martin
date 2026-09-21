# Practica 1 - Parte 3: Mini proyectos en entornos de desarrollo

## 1. Introducción

En esta tercera parte de la práctica aplicarás de forma integrada los contenidos trabajados en los capítulos 1, 2 y 3 del material del curso (Datacamp).

La Parte 3 se divide en dos mini proyectos:

- **Parte 3.1:** Visual Studio Code + Metals + Scala 2.12.21 + JDK 17 + sbt.
- **Parte 3.2:** IntelliJ IDEA Community + Scala 2.12.21 + JDK 17 + sbt.

# Parte 3.1 — Visual Studio Code + Metals + sbt

## 3.1.1 Entorno de trabajo

Este mini proyecto deberá realizarse utilizando:

- **Visual Studio Code**
    
    ![img/pS3_vscode.png](img/pS3_vscode.png)
    
- **Metals**
    
    ![image.png](img/image.png)
    
- **Scala 2.12.21**
    
    ![img/pS3_scalaVersion.png](img/pS3_scalaVersion.png)
    
- **JDK 17**
    
    ![img/pS3_javaVersion.png](img/pS3_javaVersion.png)
    
- **sbt**
    
    ![img/pS3_sbt.png](img/pS3_sbt.png)
    
- Scala 2.12.21 configurado en `build.sbt`.
    
    ![img/pS3_scalaBuilt.png](img/pS3_scalaBuilt.png)
    

El proyecto deberá ser una aplicación Scala organizada con una estructura sbt.

## 3.1.2 Mini proyecto — Clasificador de resultados de un torneo de Twenty-One

### Descripción

Vas a desarrollar un pequeño programa que analice los resultados de varias manos de un torneo de **Twenty-One**.

Cada jugador tendrá:

- Un nombre.
- Una puntuación.

El programa deberá determinar:

- Si cada jugador se ha pasado de 21.
- Qué jugadores tienen una puntuación válida.
- Cuál es la mejor puntuación válida de la ronda.
- Cuántos jugadores se han pasado.
- Cuántos jugadores siguen dentro de la partida.

El proyecto está inspirado en los ejemplos de Twenty-One utilizados en el material del curso (Datacamp), pero deberás construir una solución más completa combinando los conceptos aprendidos.

## 3.1.3 Estructura del proyecto

Crea un proyecto sbt con una estructura equivalente a:

```
torneo-twenty-one/
├── build.sbt
├── project/
└── src/
    └── main/
        └── scala/
            └── Main.scala
```

## 3.1.6 Datos iniciales

Utiliza las siguientes colecciones:

![img/pS3_datosIniciales.png](img/pS3_datosIniciales.png)

## 3.1.7 Función `bust`

![img/pS3_bust.png](img/pS3_bust.png)

## 3.1.8 Función `estadoMano`

![img/pS3_estadoMano.png](img/pS3_estadoMano.png)

## 3.1.9 Función `mejorMano`

![img/pS3_MejorMano.png](img/pS3_MejorMano.png)

## 3.1.10 Procesamiento de la primera ronda

![img/pS3_estadisticas.png](img/pS3_estadisticas.png)

## 3.1.12 Segunda ronda

![img/pS3_SegundaRonda.png](img/pS3_SegundaRonda.png)

## 3.1.13 Comparación de rondas

![img/pS3_comparacion.png](img/pS3_comparacion.png)

## 3.1.14 Uso de `foreach`

![img/pS3_versionALt.png](img/pS3_versionALt.png)

- Compilación correcta.

![img/pS3_primeraParte.png](img/pS3_primeraParte.png)

![img/pS3_segundaParteCompilacion.png](img/pS3_segundaParteCompilacion.png)

# Parte 3.2 — IntelliJ IDEA Community + sbt

## 3.2.1 Entorno de trabajo

- IntelliJ IDEA abierto.
- Plugin de Scala activo.
- JDK 17 seleccionado.
    
    ![img/pS3_javaVersion.png](img/pS3_javaVersion%201.png)
    
- Proyecto sbt cargado.
- Scala 2.12.21 configurado.
    
    ![img/pS3_scalaVersion.png](img/pS3_scalaVersion%201.png)
    

## 3.2.2 Mini proyecto — Analizador de calificaciones de un grupo

### Descripción

Vas a desarrollar una pequeña aplicación que analice las calificaciones de un grupo de estudiantes.

El programa deberá:

- Almacenar nombres.
- Almacenar notas.
- Determinar quién aprueba y quién suspende.
- Calcular estadísticas básicas.
- Identificar la mejor nota.
- Mostrar un resumen final.

El propósito del ejercicio es aplicar los conceptos estudiados en una aplicación Scala estructurada y ejecutada mediante `sbt`.

![img/pS3_2_proyecto.png](img/pS3_2_proyecto.png)

![image.png](image%201.png)

Primera parte de código con las variables y funciones a emplear al principio de la practica 

![img/pS3_2_primeraParte.png](img/pS3_2_primeraParte.png)

Segunda parte de las funciones planteadas y comienzo de las variables de las estadísticas a analizar

![img/pS3_2_segundaParte.png](img/pS3_2_segundaParte.png)

Bucle con las estadisticas y comienzo de las estadísticas detalladas 

![img/pS3_2_terceraParte.png](img/pS3_2_terceraParte.png)

Datos de la segunda evaluacion 

![img/pS3_2_cuartaParte.png](img/pS3_2_cuartaParte.png)

impresión de la información de la segunda evaluación 

![img/pS3_2_quintaParte.png](img/pS3_2_quintaParte.png)

Listas 

![img/pS3_2_listas.png](img/pS3_2_listas.png)

### 3. Explicación sobre la inmutabilidad de las listas (`::`)

- **¿Por qué la lista original no se modifica?** En Scala, las listas estándar (`List`) son **inmutables** por diseño. El operador de construcción de listas (`::`, conocido como *cons*) no muta ni altera el objeto subyacente existente en la memoria. En su lugar, crea y devuelve una **nueva** estructura de datos que apunta al nuevo elemento añadido en la cabeza y enlaza el resto con la lista original. Esto garantiza la seguridad frente a efectos secundarios indeseados en el código.

comprobacion de  sbt compile y run 

![img/pS3_2_compile.png](img/pS3_2_compile.png)

impresion de la consola

![img/pS3_2_consola.png](img/pS3_2_consola.png)