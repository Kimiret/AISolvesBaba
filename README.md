# AISolvesBaba
Proyecto de algoritmos de busqueda que intentan resolver niveles del juego baba is you


La idea a seguir es evaluar el rendimiento de algoritmos de busqueda en un ambiente de estados de gran volumen, donde las reglas a seguir pueden cambiar segun el jugador requiera, aunque tambien dan la posibilidad a mayor numero de posibles bloqueos.
Para esto se utilizará el framework de Keke AI, que fue utilizado para una competencia de agentes que resolvian niveles creados para la iniciativa Baba is Y'all, este almacena los siguientes de la sgte manera en un archivo json.
{"id":1,"name":"","author":"Demo","ascii":"__________\n_B12..F13_\n_........_\n_........_\n_........_\n_.b....f._\n_........_\n_........_\n_........_\n__________","solution":"rrrrr"}
donde en el ascii se tiene la estructura del estado inicial del nivel y es con lo que interactuan los agentes.

Estos agentes pueden elegir tomar como accion el moverse en cualquiera de las cuatro direcciones cardinales, o esperar en el mismo lugar, esta ultima accion existe ya que pueden existir elementos que se mueven de forma autonoma segun las reglas dsponibles en el nivel a resolver.
Estas acciones existen en el codigo de ejemplo de un agente bfs que viene el el repositorio de Keke AI, se ven de la forma
const possActions = ['space', 'right', 'up', 'left', 'down'];

