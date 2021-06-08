# scala
## Scala en la historia
Es compatible con JVM, es facil de emprender, nació de la academia.
Creado por Martin Odersky, en suiza en el año 2003 se poplarizo en 2006. 
Escala se compila, generá un bytecode que corre sobre JVM.

## Instalación 
Para la instalación necesitamos:

- [instalacion](https://platzi.com/clases/1793-scala/26009-instalacion-de-las-herramientas/)
- [scala-lang](https://www.scala-lang.org/download/)
### JDK 8
Java developer Kit, en la versión 8

[JDK](https://openjdk.java.net/)
### SBT 
SBT es el equivalente NPM en javascrip 

[SBT](https://www.scala-sbt.org/download.html)

### Editores 
#### REPL:en consola
#### ScalaFidddle: código online 
[ScalaFidddle](https://scalafiddle.io/)
#### Matals: integración con VSC, Atom, SublimeText
[Matals](https://scalameta.org/metals/)
#### IntelliJ IDEA: Editor mas potente de scala
[IntelliJ](https://www.jetbrains.com/idea/)

## Tipos de datos 
![Tipos de datos](https://static.platzi.com/media/user_upload/unified-types-diagram-4aa16b7f-4b45-435c-96b4-496ebb371e1e.jpg "Tipos de datos")

## Mutabilidad
Algo que puede cambiar en el tiempo, algo inmutable no cambia en el tiempo. La mutabilidad ayuda a razonar de manera correcta, las variables generan mas carga cognitiva, ayuda a siplificar el código

ir a la terminar y entrar en el interprete.

```
scala
```

Para declarar una variable, las varibles son mutables.


```
var x = 1
> var x: Int = 1
var x: Int = 1 
> var x: Int = 1
```

Para declarar un valor, los valores son inmutables. 

```
val y = 1 
> val y: Int = 1
```
```
scala> y=9
        ^
       error: reassignment to val
```

Para escribir definiciones, las definiciones no se pueden mutar.

```
def z = 1
> def z: Int
```
```
scala> z =2
       ^
       error: value z_= is not a member of 
```

## Expresiones
Las expresiones son el lenguaje básico de programación en Escala, Escala es un lenjuaje orientado a expresiones.
Los bloques de código siempre retonar un valor 

```
def x = (3)
def x = 3
def x = {3}
``` 

```
def z = {1; 1+2}
```
El parentesis indica que solo puede haber una expresión

```
def z = (1; 1+2)
```

```
if(x != 3 )"No es tres" else "es tres"
> val res2: String = es tres
```

```
if (x != 3 ) "No es tres" 
> val res3: Any = ()
```
## Funciones 
Una función tiene un dominio y un rango f: D -> R.
Una función de orden superior, es tratar a la función como un valor mas.

- Funciones anónimas 
- Funciones como objetos 
- Funciones como métodos

```
def f(x: Int) = x * x
f(2)
```

*Funciones anónimas*
 ```
 (x: Int) => x*x
 > val res8: Int => Int = $Lambda$1069/13233472@394880
```
Las funciones anónimas se puede guardar en un valor para tener las disponibles
```
 val a = (x: Int) => x*x
 > val a: Int => Int = $Lambda$1070/24017028@e4aad3
 a(a)
 ``` 
*Funciones como objetos*
 ```
 scala> f.apply(8)
       ^
       error: missing argument list for method f
       Unapplied methods are only converted to functions when a function type is expected.
       You can make this conversion explicit by writing `f _` or `f(_)` instead of `f`.
 ```
 Lo anterior falla por que las funciones no son objetos.
 ```
 scala> a.apply(4)
 val res13: Int = 16
 ```
 Lo anterior no falló porque a si es un objeto. Pero se pueden convertir las funciones en objetos, usando:
 ```
 scala> val c = f _
 val c: Int => Int = $Lambda$1176/21561793@1a3ffe6
 ```

 **_** Se usa como comodín.  
*Funciones de orden superior*
 Las funciones pueden recivir funciones como entrada
 ```
 scala> def g(z: Int => Int) = z(4)
 def g(z: Int => Int): Int
 ```

 ```
 def s(x: Int => Int)(y: Int) = x(y)
 ```

*Funciones como métodos*
 ```
 object Util {
     def metodo(x: Int) = x+x
     val a = metodo _
 }
 ```
 Funcion que genere una función 

 def sGreater(int1: Int)={
        (int2: Int) => int2 > int1
 }