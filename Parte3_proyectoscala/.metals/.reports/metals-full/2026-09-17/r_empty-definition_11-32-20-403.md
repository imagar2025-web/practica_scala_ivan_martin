error id: file:///C:/Users/AlumnoM_AI/Desktop/Clases/17-09-2026/borradores/Parte3_proyectoscala/torneo-twenty-one/src/main/scala/Main.scala:scala/collection/ArrayOps#foreach().
file:///C:/Users/AlumnoM_AI/Desktop/Clases/17-09-2026/borradores/Parte3_proyectoscala/torneo-twenty-one/src/main/scala/Main.scala
empty definition using pc, found symbol in pc: 
empty definition using semanticdb
empty definition using fallback
non-local guesses:
	 -puntos/foreach.
	 -puntos/foreach#
	 -puntos/foreach().
	 -scala/Predef.puntos.foreach.
	 -scala/Predef.puntos.foreach#
	 -scala/Predef.puntos.foreach().
offset: 2597
uri: file:///C:/Users/AlumnoM_AI/Desktop/Clases/17-09-2026/borradores/Parte3_proyectoscala/torneo-twenty-one/src/main/scala/Main.scala
text:
```scala


object Main extends App{
    val jugadores = List(
  "Alex",
  "Chen",
  "Marta",
  "Sindhu",
  "Luis"
)

val puntuaciones = Array(
  18,
  24,
  21,
  20,
  26
)
//3.1.7 Función `bust`
def bust(puntuacion: Int): Boolean = {
    if(puntuacion > 21){
        true
    }else{
        false
    }
}
// Demostración de la función
println(s"${bust(puntuaciones(0))}")

// Actualización con strings
def valida(puntuacion: Int): String = {
    if(puntuacion > 21){
        "VALIDA"
    }else{
        "BUST"
    }
}
//Demostración
print(s"${{valida(puntuaciones(2))}}")
//3.1.9 Función `mejorMano`
def mejorMano(handA: Int, handB: Int): Int ={
    if(handA > 21 && handB > 21){
        0
    }else if(handA >21){
        handB
    }else if(handB > 21){
        handA
    }else if(handA > handB){
        handA
    }else if(handA < handB){
        handB
    }else{
        1
    }

}
    // casos de prueba
println(s"${mejorMano(22,22)}")
println(s"${mejorMano(22,20)}")
println(s"${mejorMano(20,22)}")
println(s"${mejorMano(19,12)}")

//3.1.10 Procesamiento de la primera ronda
def rondas(jugadores : List[String], puntos: Array[Int]) : String = {
     var i = 0
     var cadenaSalida = "" 
    while(i < puntos.length){
        var jugadorActual= jugadores(i)
        var puntosActual = puntos(i)
        cadenaSalida += s"${jugadorActual} -> ${puntosActual}-> ${valida(puntosActual)}\n"
        i+=1
    }
    cadenaSalida
}
println(s"${{rondas(jugadores,puntuaciones)}}")

def resumenestadisticas(puntos: Array[Int]) : String ={
    var i = 0
    var cadenaSalida = ""
    var manValidas = 0
    var bust=0
    var bestMark = puntos(0)
    var numJugadores= puntos.length
    while(i < puntos.length){
        var numActual= puntos(i)
        
        if(bestMark < numActual){
            bestMark = numActual
        }
        //esperamos dos resultados en la funcion bust
        if(valida(numActual) == "VALIDA"){
            manValidas +=1
        }else{
            bust +=1 
        }
        i+=1
    }
    s""""--- Resumen de la ronda ---

        Jugadores: ${numJugadores}
        Manos validas: ${manValidas}
        Bust: ${bust}
        Mejor puntuacion valida: ${bestMark}
    """"
}

print(s"${resumenestadisticas(puntuaciones)}")

//3.1.12 Segunda ronda

val puntuacionesRonda2 = Array(
  22,
  19,
  20,
  21,
  17
)
print(s"${resumenestadisticas(puntuacionesRonda2)}")

//3.1.14 Uso de foreach

def validaForEach(puntos :Array[Int]) : String ={
    puntos.fo@@reach(p => if(p>21) println("Valida") else println("Bust"))
    ""
}
//demostracion
println(valida(puntuacionesRonda2))
}






```


#### Short summary: 

empty definition using pc, found symbol in pc: 