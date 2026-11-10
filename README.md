# Framework Tekton

Metodología de Zuriel Sistemas para acompañar procesos de transformación organizacional, vocacional y espiritual.
Sirve para empresas y también para personas.

Toma la estructura modular de [Tekton](https://tekton.dev), el marco de pipelines de software que nació en Google:
lo que allí es un pipeline de tareas, aquí es un camino que recorre una organización o una persona.

Este repositorio guarda solo la metodología: el vocabulario, los niveles, los frentes y las reglas. No publica pasos
concretos, ni el catálogo de pasos tipo, ni plantillas de camino, y nunca datos de clientes.

## Filosofía

> «Cada transformación parte del reconocimiento de un llamado.»

Tekton une propósito, orden y entrega real: no solo instala sistemas, siembra estructura con sentido. El criterio que
manda es encontrar la mejor dirección al menor costo.

## La cadena: de la señal a los trabajos

**señal → activador → camino con su destino → tramos → pasos → dependencias → trabajos**

- Todo Tekton es estratégico: decide qué logra la organización (o la persona).
- Lo táctico va fuera de Tekton: cada proyecto tiene sus planes de trabajo, con sus trabajos, y ahí se decide quién,
  cuándo y con cuántos créditos. A lo táctico no se le llama camino, tramo ni paso.
- Un paso nunca genera una propuesta: la propuesta, con su precio, es de un proyecto, y un proyecto puede juntar pasos
  de varios caminos. Qué pasos activados necesitan una o varias propuestas se decide en una sesión con el cliente,
  mirando los pasos que faltan y sus créditos estimados.
- Una activación no le encarga trabajo a nadie: abre los tramos que el cliente decidió.
- Cada trabajo dice qué pasos hace avanzar (uno o varios) y reparte sus créditos entre ellos: en partes iguales,
  salvo que se indique otro reparto.
- Las sesiones y los formularios con el cliente son insumos de los pasos.

## Vocabulario

| Término | Qué es | Ejemplo |
|---|---|---|
| Señal | El hecho que dispara el trabajo, con su fecha, quién la trajo y qué tan urgente es | Un sistema del cliente que se corta esta semana |
| Frente | Una línea del cliente, con el nombre que usa el cliente. Se numeran desde 0, y el 0 es siempre la dirección del cliente. Cada frente guarda sus caminos y tiene su responsable del lado del cliente | 0 Dirección, 1 Tienda, 2 Administración |
| Activador | El llamado de un camino: hay uno por camino. Lleva la señal de origen, el destino y el documento que le propone el camino al cliente y lo anima a llegar al destino. Su documento va por versiones | AC-01 |
| Activación | Cada decisión del cliente sobre un camino, aceptada o rechazada, hasta el tramo que diga | Activar 1C-01 hasta el T1 |
| Camino | Una capacidad que gana la organización, con un destino. Va en un frente y puede cruzar los tres niveles | 1C-01 Atención con agentes |
| Destino | Cómo opera la organización cuando el camino termina. No cambia: si cambia, es otro camino | Cada unidad atiende a sus clientes con su agente |
| Tramo | Una etapa de progresión del camino que agrupa pasos, nombrada por su logro. El cliente activa el camino tramo a tramo | T1 Interesados atendidos por el agente |
| Paso | Un logro con su nivel, su función, sus créditos estimados y un solo resultado que se puede verificar. Su secuencia es una sugerencia | 1C-01.2 Citas agendadas por el agente |
| Nivel | El de cada paso: Gobierno, Orden o Ejecución | nivel Ejecución |
| Función | La función de negocio del paso (lista abajo) | Ventas |
| Dependencia | Lo que un paso necesita de otro paso, o de un tramo completo. Dura: bloquea. Blanda: deja avanzar con el riesgo de retrabajo escrito, si el cliente lo asume en una activación | 1C-01.2 depende (dura) de 0C-01.3 |
| Bloqueo | El estado de un paso con una dependencia dura sin cumplir. Muestra qué lo bloquea, aunque sea de otro frente. No se pone a mano: sale de las dependencias | 1C-01.2 bloqueado por 0C-01.3 |
| Insumo | Una sesión o un formulario con el cliente que alimenta uno o varios pasos | Sesión con el equipo directivo |
| Créditos estimados | El esfuerzo estimado de un paso, en créditos. El cliente los ve: con ellos compara pasos y caminos y decide la dirección. Son una estimación, no un precio ni un compromiso: lo que se consume sale de los trabajos. Al cerrar el paso se comparan con los reales | 6 créditos |
| Paso tipo | Un paso del catálogo de pasos tipo, ordenado por niveles y funciones. Su resultado no cambia y todo lo demás mejora por versiones: si cambia el resultado, es otro paso tipo | Proceso de cobranza documentado |
| Plantilla de camino | El recorrido guardado de un camino real que funcionó | — |

Equivalencias con Tekton, solo como referencia: señal = Trigger, camino = Pipeline, paso = Task.

## Los tres niveles

| Nivel | Qué cubre |
|---|---|
| Gobierno | El rumbo y la información |
| Orden | Los procesos y los recursos |
| Ejecución | Las iniciativas concretas |

El nivel es de cada paso: un camino puede cruzar los tres, y un tramo no es un nivel. Escribe siempre «nivel Orden»,
para no confundirlo con la secuencia de los pasos.

## Frentes

- Un frente es una línea del cliente, con el nombre que usa el cliente: 0 Dirección, 1 Tienda, 2 Administración.
- Se numeran desde 0, y el 0 es siempre la dirección del cliente: no se retira.
- Puede haber frentes compartidos (por ejemplo, Administración) para que el 0 no se vuelva un cajón.
- Cada frente guarda sus caminos y tiene su responsable del lado del cliente.
- Un frente con caminos propuestos o activos no se retira; los frentes no se borran.
- Para una persona, los frentes son las líneas de su vida que decide trabajar, y el 0 es su propia dirección.

## Códigos

Van por cliente: cada empresa o persona tiene los suyos.

| Pieza | Código | Ejemplo | Regla |
|---|---|---|---|
| Frente | Su número, desde 0 | 0, 1, 2 | El 0 es la dirección del cliente |
| Camino | El número de su frente, una C y su número dentro del frente | 1C-01 | Solo cambia de frente mientras está propuesto, y entonces cambian su código y el de sus pasos |
| Paso | El código de su camino y su número | 1C-01.2 | No cambia si el paso pasa a otro tramo |
| Tramo | T y su número | T1, T2, T3 | Es una etiqueta del paso: no va dentro de su código |
| Activador | AC y su número | AC-01 | Uno por camino |

## Estados

- **Activación:** aceptada o rechazada. No cambia: si el cliente decide otra cosa, es una activación nueva.
- **Camino:** propuesto, activo, finalizado, cancelado. Nace propuesto y pasa a activo solo con una activación
  aceptada. Un camino finalizado vuelve a activo con la activación «mejorar». Se cancela desde propuesto o activo.
- **Paso:** sugerido, activo, bloqueado, cumplido, omitido. Bloqueado no se pone a mano: sale de sus dependencias
  duras. Un paso queda cumplido cuando se confirma su resultado, no solo porque se cerraron sus trabajos, y desde ahí
  queda fijo.
- **Paso tipo:** borrador, vigente, archivado. Entra al catálogo como borrador cuando arranca el primer paso que lo usa
  y queda vigente (fijo, con su historia) cuando ese paso se cumple.

## Activaciones

Toda decisión del cliente sobre un camino es una activación. Registra la señal de ese momento, la versión del
activador que vio, quién decidió del lado del cliente, por dónde (reunión, mensaje, correo, llamada), cuándo y hasta
qué tramo llega.

| Motivo | Cuándo |
|---|---|
| Activar | Un camino propuesto, hasta un tramo |
| Continuar | Un camino activo, hasta un tramo después del último activado |
| Presentar de nuevo | Un camino propuesto, después de un rechazo |
| Asumir el riesgo | El de una dependencia blanda sin cumplir. En el camino del diagnóstico, en el frente 0, una sola activación puede asumir para todos los caminos del cliente el riesgo de avanzar sin él |
| Mejorar | Un camino finalizado: vuelve a activo, con el mismo destino y un tramo más |

- Aceptada, activa los tramos hasta el que dice (y el camino, si estaba propuesto o finalizado). Solo se activan los
  pasos de un tramo activado.
- Destrabar un paso bloqueado es activar el activador del camino que lo bloquea.
- La secuencia de los pasos es una sugerencia y no lleva activación.
- Lo que el cliente activó es lo que vio: a un tramo activado no entran pasos nuevos (van en un tramo nuevo, con
  continuar o mejorar), y el resultado y los créditos estimados de sus pasos no cambian.

## El activador

Hay uno por camino. Su documento le propone el camino al cliente, en este orden:

1. La señal, contada en el idioma del cliente.
2. El destino.
3. Los tramos, cada uno con su logro, y en cada tramo sus pasos: qué logra cada uno, su nivel, su función y sus
   créditos estimados, con el total de cada tramo.
4. Qué lo bloquea: los pasos de los que depende, aunque sean de otro frente, con sus créditos estimados, y en las
   dependencias blandas, el riesgo de avanzar sin ellos.
5. Lo que se necesita: plataformas y recursos.
6. Para activarlo: lo que pone el cliente (responsable, datos, momento de arranque) y hasta qué tramo se propone llegar
   ahora.

Sin precios: los créditos van como estimación y el precio va en la propuesta de un proyecto. Cada cambio es una
versión nueva, y cada versión se aprueba en Zuriel, créditos incluidos, antes de que la vea el cliente. El cliente solo
decide sobre una versión aprobada.

## Reglas

- **Tamaño:** un paso tiene un solo resultado verificable. Si tiene dos, son dos pasos. Por ejemplo, un agente que
  atiende interesados, agenda citas y envía recordatorios de pago son tres pasos, no uno.
- **Sentido:** el resultado de un paso tipo y el destino de un camino no cambian; lo demás mejora por versiones. Si
  cambia el destino, es otro camino; si cambia el resultado, es otro paso tipo.
- **Lo mínimo:** se proponen solo los pasos que destraban la señal, y lo mínimo de cada uno.
- **Primero el catálogo:** antes de proponer un paso se busca un paso tipo que sirva. Si sirve, el paso parte de él y
  se anota qué se adapta; si no, el paso es nuevo.
- **Dependencias:** cada una es dura o blanda, y nunca en círculo. La blanda lleva escrito el riesgo: qué habría que
  rehacer si se avanza sin lo otro. Un tramo está completo cuando todos sus pasos están cumplidos u omitidos.
- **Cierre de un paso:** al cumplirlo u omitirlo se anota de qué paso tipo partió (o si es nuevo), qué se adaptó, el
  resultado obtenido (o por qué se omitió), una lección corta y los créditos reales, que se comparan con los estimados.
- **Cierre de un camino:** cuando todos sus pasos están cumplidos u omitidos, con un resumen final y las lecciones
  aprendidas. Si el recorrido funcionó y puede servir a otros, puede guardarse como plantilla de camino.

## Lo que ve el cliente

Su matriz de niveles por frentes, que parte de la señal, con cada camino en su color y los créditos de cada paso,
estimados y consumidos. Ve solo lo aprobado: nunca borradores, hipótesis ni precios fuera de las propuestas aprobadas.
Cada responsable ve su frente y la dirección los ve todos.

## Funciones válidas de un paso

Dirección, Mercadeo, Ventas, Operaciones, Logística, Formación, Legal, Sistemas, Finanzas, Recursos Humanos.

## Contenido del repositorio

```
tekton-framework/
├── README.md              La metodología (este documento)
└── spec/
    ├── modelo.json        Las piezas, sus estados, los motivos de una activación y las reglas
    ├── nomenclatura.json  Los códigos
    └── funciones.json     Los niveles y las funciones válidas de un paso
```

No están aquí, a propósito: pasos concretos, el catálogo de pasos tipo, plantillas de camino ni datos de clientes.
