<img src="https://raw.githubusercontent.com/MumukiProject/mumuki-guia-gobstones-pruebas-contenido-mumuki/master/assets/musculos_sf_v2_1623623551075.png" alt="musculos_sf_v2_1623623551075.png" width="auto" height="auto">

_En estos tiempos de aislamiento, donde muchos gimnasios están cerrados, nos pidieron modelar una aplicación de ejercicios para poder entrenar en casa. Con esto en mente decidimos crear PdeGym._

**Parte A** 

Tenemos personas que tienen un nombre, una cantidad de calorías, un índice de hidratación que va de 0-100, una cantidad de tiempo disponible para entrenar y un conjunto de equipamientos. Al entrenar, las personas pueden realizar los siguientes ejercicios:

1. **_abdominales_**: dada una cantidad de repeticiones, la persona pierde 8 calorías por cada repetición.
2. **_flexiones_**: dada una cantidad de repeticiones, la persona pierde 16 calorías por cada repetición y 2 de hidratación cada 10 repeticiones. _Ejemplo: si hace 40 repeticiones su índice de hidratación disminuirá en 8._
3. **_levantarPesas_**: dada una cantidad de repeticiones y un peso, la persona pierde 32 calorías por cada repetición y además cada 10 repeticiones su índice de hidratación baja lo que pesa la pesa (cuak). Para hacer este ejercicio, dicha persona debe tener al menos una "pesa" dentro de su equipamiento. _Ejemplo: si una persona hace 30 repeticiones con una pesa de 5 kilogramos su índice de hidratación disminuirá en 15._
4. **_laGranHomeroSimpson_**: no hace nada, la persona sigue exactamente igual.

**Nota**: Vamos a considerar que ninguno de los ejercicios hacen que las calorías o el índice de hidratación sean negativos. Es por esto que no vamos a preocuparnos por validarlo.

Más allá de los ejercicios, las personas pueden registrar otras acciones:

1. **_renovarEquipo_**: cuando una persona renueva su equipo, a cada equipamiento que tenga se le agrega “Nuevo” adelante.
2. **_volverseYoguista_**: cuando una persona se vuelve yoguista su cantidad de calorías se reduce a la mitad y su índice de hidratación se duplica (manteniendo un máximo de 100). Como equipamiento solo tendrá una “colchoneta” y vende todo lo demás que tenía hasta ese momento.
3. **_volverseBodyBuilder_**: al volverse body builder, en su nombre se agrega un “BB” al final, sus calorías se triplican y su índice de hidratación queda igual. Una persona solo se puede volver body builder si todos sus equipamientos son pesas. Por ejemplo, ["pesa", "pesa", "pesa", "pesa"].
4. **_comerUnSandwich_**: de vez en cuando hay que descansar y comer algo, al hacer esto, dicha persona aumenta sus calorías en 500 y su índice de hidratación sube hasta 100 gracias al rico refresco que acompaña el sandwich.

**Parte B**

Tenemos rutinas, las cuales tienen un tiempo aproximado de duración y un listado de ejercicios. Lo primero que tenemos que tener en cuenta es que una persona no puede hacer rutinas cuya duración aproximada sea mayor que su tiempo libre. De cada rutina queremos saber si:

1. **_esPeligrosa_**: una rutina es peligrosa cuando deja a la persona agotada. Esto sucede cuando sus calorías son menores a 50 y su índice de hidratación es menor a 10.
2. **_esBalanceada_**: una rutina es balanceada cuando al terminarla, el índice de hidratación de la persona es mayor a 80 y las calorías son menos de la mitad de cuando empezó.

Modelar la rutina **_elAbominableAbdominal_**, dicha rutina dura aproximadamente 1 hora y consiste en hacer 1 abdominal, 2 abdominales, 3 abdominales... hasta el infinito.

**Parte C**

Para finalizar vamos a agregar dos funcionalidades más, relacionadas a los ejercicios grupales:

1. **_seleccionarGrupoDeEjercicio_**: una persona quiere seleccionar quienes pueden hacer rutina con ella a partir de un grupo de personas. Las personas que pueden ser grupo de ejercicio de otra son aquellas que tengan el mismo tiempo disponible.
2. **_promedioDeRutina_**: dada una rutina y un grupo de personas, devolver el promedio de calorías **y** el índice de hidratación final del grupo tras haber hecho la rutina.

**Aclaraciones**

* Todas las funciones deberán estar tipadas.
* NO repetir lógica.
* Usar composición siempre que sea posible.
* Enviar la solución a Mumuki cada ~30 minutos o a medida que vayas resolviendo cada punto.

**También podés ver el examen desde [acá](https://docs.google.com/document/d/1l38tmiE4Qu9kvJv3Ns1qsS_tnh5GOAziAliMLccXkP8/edit).**


