- Más que represental el proceso de software como una secuencia de actividades con retrospectiva de una actividad a otra, se representa como una espiral. Cada ciclo en la espiral representa una fase del proceso de software. Así, el ciclo más interno podría referirse a la viabilidad del sistema, el siguiente ciclo a la definición de requerimientos, el siguiente ciclo al diseño del sistema, y así sucesivamente.
- La diferencia principal entre el modelo de espiral y otros modelos es la **consideración explícita del riesgo** (algo puede ir mal).
- Por ejemplo: Si la intención es utilizar un nuevo lenguaje de programación, un riesgo es que los compiladores disponibles sean poco fiables o que no produzcan código objeto lo suficientemente eficiente.
- Los riesgos originan problemas en el proyecto, como por ejemplo:
	- Confección de agendas
	- Excesos en los costos
- La disminución de los riesgos es una actividad importante en la gestión del proyecto.
- Cada ciclo de la espiral se divide en cuatro sectores:
	- **Definición de objetivos**
	  logseq.order-list-type:: number
		- Se definen los objetivos específicos
		- Se identifican las restricciones del proceso y el producto
		- Se traza un plan detallado de gestión
		- Se identifican riesgos del proyecto
		- **Dependiendo de estos riesgos se planean estrategias alternativas**
	- **Evaluación y reducción de riesgos**
	  logseq.order-list-type:: number
		- Se realiza un análisis detallado para cada uno de los riesgos
		- Se definen los pasos para reducir dichos riesgos
		- *Por ejemplo, si existe el riesto de tener requerimientos inapropiados, se puede desarrollar un prototipo del sistema*
	- **Desarrollo y validación**
	  logseq.order-list-type:: number
		- Se elige un modelo para el desarrollo del sistema
			- **Ejemplo: Los riesgos en la interfaz de usuario son dominantes**, un modelo apropiado podría ser la construcción de prototipos evolutivos.
			- **Ejemplo: Los riesgos de seguridad son la principal consideración**, un desarrollo basado en transformaciones formales podría ser el más apropiado
			- El modelo en cascada puede ser el más apropiado si el riesgo mayor identificado es la    integración de los  subsistemas
	- **Planificación**
	  logseq.order-list-type:: number
		- Se revisa el proyecto
		- Se toma la decisión de si se debe continuar con un ciclo posterior de la espiral.
		- Se desarrollan los planes para la siguiente fase del proyecto
- Un ciclo espiral empieza con la elaboración de objetivos, como el rendimiento y la funcionalidad. Entonces se enumeran formas alternativas de alcanzar estos objetivos y las restricciones impuestas en cada una de ellas. Cada alternativa se evalúa contra cada objetivo y se identifican las fuentes de riesgo del proyecto. El siguiente paso es resolver estos riesgos mediante actividades de recopilación de información como
	- Detallar más en análisis
	- Construcción de prototipos
	- Simulación
- Una vez se han evaluado los riesgos, se lleva a cabo cierto desarrollo, seguido de una actividad de planificación para la siguiente fase del proceso.
-