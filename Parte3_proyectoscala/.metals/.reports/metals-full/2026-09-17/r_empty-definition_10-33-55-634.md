error id: file:///C:/Users/AlumnoM_AI/Desktop/Clases/17-09-2026/borradores/Parte3_proyectoscala/torneo-twenty-one/src/main/scala/Main.scala:scala/Predef.println(+1).
file:///C:/Users/AlumnoM_AI/Desktop/Clases/17-09-2026/borradores/Parte3_proyectoscala/torneo-twenty-one/src/main/scala/Main.scala
empty definition using pc, found symbol in pc: 
empty definition using semanticdb
empty definition using fallback
non-local guesses:
	 -println.
	 -println#
	 -println().
	 -scala/Predef.println.
	 -scala/Predef.println#
	 -scala/Predef.println().
offset: 1054
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
}
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
object Main extends App{
    // casos de prueba
println(s"${mejorMano(22,22)}")
println(s"${mejorMano(22,20)}")
pri@@ntln(s"${mejorMano(20,22)}")
println(s"${mejorMano(19,12)}")
}
```


#### Short summary: 

empty definition using pc, found symbol in pc: 