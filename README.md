# scala
## Scala en la historia
Es compatible con JVM, es facil de emprender, nació de la academia.
Creado por Martin Odersky, en suiza en el año 2003 se poplarizo en 2006. 
Escala se compila, generá un bytecode que corre sobre JVM.

## Instalación 
Para la instalación necesitamos:

- [instalacion]:https://platzi.com/clases/1793-scala/26009-instalacion-de-las-herramientas/
- [scala-lang]:https://www.scala-lang.org/download/
### JDK 8
Java developer Kit, en la versión 8

[JDK]:https://openjdk.java.net/
### SBT 
SBT es el equivalente NPM en javascrip 

[SBT]:https://www.scala-sbt.org/download.html

### Editores 
#### REPL:en consola
#### ScalaFidddle: código online 
[ScalaFidddle]:https://scalafiddle.io/
#### Matals: integración con VSC, Atom, SublimeText
[Matals]:https://scalameta.org/metals/
#### IntelliJ IDEA: Editor mas potente de scala
[IntelliJ]:https://www.jetbrains.com/idea/


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
var x: Int = 1 
```

Para declarar un valor, los valores son inmutables. 

```
val y = 1 

```

Para escribir definiciones, las definiciones no se pueden mutar.

```
def z = 1

```