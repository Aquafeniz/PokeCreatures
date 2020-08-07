# PokeCreatures

#Readme

#Creadores
1. Daniel Giraldo
2. Juan Pablo Restrepo

Se implementó la clase Battle para poder tener  crear un ambiente de pruebas controlado donde pudiéramos revisar los casos que sólo se pueden revisar durante una pelea de Critters y no durante la construcción de Critters o Skills. teniendo metodos practicos para la prueba de modelos como la batalla entre habilidades tipo fuego contra creatures tipo tiera, o la prueba de debuff de speed y la prueba de que no se puedan usar mas de los defubos.
La clase tiene elementos como contadores de turno y referencias a los jugadores para realizar las peleas desde ella misma para realizar las pruebas requeridas.

*Pruebas Realizadas:
1. Un AttackSkill NO puede crearse con poder 0, ni con un valor fuera del rango. (Creacion)
2. Un SupportSkill NO puede crearse con poder superior a 0 (Creacion)
3. Tras aplicar por una única ocasión el skill SpdDown a un critter, el valor de su velocidad base se mantiene; pero sí hay un decremento en la velocidad del critter durante la pelea. (Test 3)
4. Tras aplicar 4 veces DefUp a un critter, la defensa del critter no puede reflejar un valor diferente al que tuviera tras la tercera aplicación del Skill. (Test 4)
5. El daño recibido por un critter con afinidad Earth al ser atacado con un Skill de afinidad Fire debe ser 0 a través la fórmula especificada (Test 1)
6. El daño recibido por un critter con afinidad Wind al ser atacado con un Skill de afinidad Water debe ser calculado por la fórmula especificada. ( Test 2)
7. Cuando un critter pierde todos sus HP, debe ser removido de su dueño y otorgado al dueño del critter ganador. (Todas)
8. Fuera de los casos de prueba, su código debe soportar las restricciones mencionadas.*


*AttackSkill y SuportSkill
Se creo una clase para attackskill y otra para support que estan heredadas de una clase padre de skill, ambas tiene funciones diferentes. donde se cumplen las funcionalidades impuestas desde el principio haciendo que se cumplan con las condiciones del rango de las habilidades

*Critter
Se añadio la clase critter con sus propias verificaciones de rango ademas de la funcion para recibir daño

*Player
se creo la clase player para referencial al jugador que era el que tenia las criaturas 

- Principal - Program - MAIN
Se realizo la creacion de las skills asignadolas de un grupo de skills (MoveSet) ademas de invocar las llamadas
