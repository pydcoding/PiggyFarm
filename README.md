# Instrucciones

Vamoh a simuláh una granja. La idea es tener una clase 'Granja' que se encargue de añadir y gestionar los distintos animales. También contendrá trabajadores que podrán hacer determinadas acciones sobre los animales. La parte guay es que nuestra método main será una simulación de una granja, crearemos un bucle infinito en el que cada segundo que pase, pasará una hora en la granja. Los animales tendrán hambre, sueño, y los trabajadores tendrán que cuidarles y mantenerles contentos. Tonces:

1. Abre el proyecto con Netbeans.
2. Crea las siguientes clases:
   - Granja: contiene una lista de animales y trabajadores.
   - Animal: (clase padre, guiño guiño)
     - Cerdo
     - Vaca
     - Caballo
   - Trabajador: (clase padre, codo codo)
     - Cuidador
     - Entrenador
   - Producto: (clase padre, codo codo, guiño guiño)
     - Bellota
     - Leche

## Animales

Todos los animales tienen nombre, un nivel de hambre, de sueño y de felicidad. Por tanto, todos los animales deben ser capaz de comer una cantidad de comida y dormir una cantidad de horas. Pero cada animal es diferente, un cerdo come y duerme más que una vaca y un caballo. Sin embargo son felices más fácilmente. Por ejemplo: si un animal tiene un nivel de sueño de 32, si está por debajo de ese nivel, tendrá sueño. Cada hora decrementará el sueño y aumentará el hambre.

| Animal  | Nivel de hambre | Nivel de sueño | Nivel de felicidad | Nivel de cansancio |
|---------|:---------------:|:--------------:|:------------------:|:------------------:|
| Cerdo   |      25-35      |     35-45      |       15-25        |         -          |
| Vaca    |      55-65      |     45-65      |       35-45        |         -          |
| Caballo |      65-85      |     75-85      |       65-75        |       50-80        |

Los rangos son para dar aleatoriedad entre animales del mismo tipo.

- Si tienen sueño bostezarán y se irán a dormir.
- Si tienen hambre se quejarán y su felicidad decrementará hasta que le den de comer.

Los cerdos y las vacas están obligados a producir (*ejem* interfaces *ejem*) y los caballos a entrenar (*ejem* más interfaces *ejem*).

- Los caballos cuando entrenan se cansan y les aumenta el hambre.

- Los cerdos producen encontrando bellotas.
- Las vacas producen leche, y por tanto necesitan ser ordeñadas por algún trabajador.

## Trabajadores

Todos los trabajadores tienen un horario, la hora de entrada y salida serán constantes:

- Los cuidadores trabajan de 06:00 a 16:00
  - Deben ser capaz de dar de comer a todos los animales y de ordeñar vacas.
- Los entrenadores trabajan de 10:00 a 18:00
  - Deben ser capaz de entrenar a los caballos.
