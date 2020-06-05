# QMP5
--
## Como usuarie de QuéMePongo, quiero poder manejar varios guardarropas para separar mis prendas según diversos criterios (ropa de viaje, ropa de entrecasa, etc). 
Creo una clase Guardarropa que tiene una lista de prendas (esta podia ya estar creada desde la anterior iteracion), y agrego una clase Usuario que tiene como argumento una lista de los guardarropas que maneja.

## Como usuarie de QuéMePongo, quiero poder crear guardarropas compartidos con otros usuaries (ej, ropa que comparto con mi hermane). 
Para esto no hace falta agregar nada, simplemente varios usuarios pueden conocer al mismo guardarropa.

## Como usuarie de QuéMePongo, quiero que otro usuario me proponga tentativamente agregar/quitar una prenda al guardarropas.
A la clase usuario se le agregan los metodos de proponerAgregar(Guardarropa unGuardarropa, Prenda unaPrenda), 
proponerQuitar(Guardarropa unGuardarropa, Prenda unaPrenda). Estos simplemente agregaran un objeto Propuesta (Agregar o Quitar) a la lista 'propuestas' del guardarropa que corresponda.

## Como usuarie de QuéMePongo, necesito ver todas las propuestas de modificación (agregar o quitar prendas) del guardarropas y poder aceptarlas o rechazarlas.
Un guardarropa va a tener un metodo aceptarPropuesta(Propuesta unaPropuesta), que va a aplicar la propuesta y luego pasar este objeto propuesta a la lista 'propuestasAceptadas' y rechazarPropuesta(Propuesta unaPropuesta), que simplemente va a sacar el objeto propuesta de la lista 'propuestas'.
Las Propuestas van a tener un metodo aplicar(Guardarropa unGuardarropa), que va a agregar o quitar la prenda que tiene como argumento de la lista 'prendas' del guardarropa correspondiente.

## Como usuarie de QuéMePongo, quiero poder deshacer las propuestas de modificación que haya aceptado.
Todas las propuestas aceptadas estaran en la lista 'propuestasAceptadas', el metodo revertir propuesta va a ejecutar revertir de la propuesta pasando como paramentro 'this'. revertir va a hacer lo que hace el aplicar de la propuesta contraria, Quitar va a agregar y Agregar va a quitar.
