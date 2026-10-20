Paso 4 — La OBS y la Matriz RACI
La EDT dice qué hay que hacer. Falta la otra mitad: quién.

La OBS —Estructura de Desglose de la Organización— es la estructura del equipo: los roles y las personas, organizados como una jerarquía. En un proyecto de curso suele ser corta: un líder técnico, desarrollo, diseño, y el cliente o interesado principal.

Lo interesante pasa cuando cruzas las dos.

La EDT da las columnas
La OBS
da las filas
Catálogo
Carrito
Pagos
Panel
Líder técnico
Desarrollo
Diseño
Cliente
A
A
C
A
R
R
R
R
C
C
I
R
I
C
A
C
R
Realiza el trabajo
A
Aprueba y responde
C
Se le consulta
I
Se le informa
Cada paquete de trabajo tiene exactamente una A. Si tiene dos, nadie responde por él.

Las cuatro letras
R — Realiza. Quien hace el trabajo. Puede haber varios.
A — Aprueba y responde. Quien responde por el resultado ante los demás. Exactamente uno.
C — Se le consulta. Se le pregunta antes de decidir, en las dos direcciones.
I — Se le informa. Se le avisa después. Comunicación en una sola dirección.
La regla que importa
Cada paquete de trabajo tiene exactamente una A.

Si tiene dos, en la práctica no tiene ninguna: cuando algo sale mal, cada uno supone que respondía el otro. Y si no tiene ninguna, el paquete no tiene dueño y va a ser el que se quede sin hacer.

💡 Diferencia que confunde a todo el mundo: R hace, A responde. Pueden ser la misma persona, y en equipos pequeños casi siempre lo son. Lo que no puede pasar es que haya dos A.

Cómo llenarla sin que tome una hora
Ve columna por columna, no fila por fila. Para cada paquete de trabajo, pregunta en este orden: quién responde por esto (una A), quién lo va a hacer (una o varias R), a quién hay que preguntarle antes (C) y a quién hay que avisarle después (I). Casi siempre quedan varias celdas vacías, y está bien: no todo el mundo tiene que ver con todo.

Paso 5 — Para Qué Sirve Todo Esto
Vale la pena ver por qué la EDT va antes que el resto de la planificación, y no después.

EDT
cada paquete
de trabajo
Cronograma
cada paquete se vuelve una tarea con fecha
Costo
cada paquete recibe su parte del presupuesto
Riesgos
cada paquete se pregunta qué puede salir mal
Por eso la EDT va antes que estimar, antes que planear fechas y antes que analizar riesgos.

El cronograma se construye tomando cada paquete de trabajo como una tarea con duración y dependencias. Sin EDT no hay lista de tareas: hay una lluvia de ideas.
El presupuesto se construye asignando a cada paquete su porción del costo. Estimar el proyecto completo de una sola vez es adivinar; estimar veinte paquetes y sumar tiene un margen de error mucho menor.
El registro de riesgos se construye recorriendo la EDT y preguntando, paquete por paquete, qué puede salir mal aquí. Es la forma más confiable de no dejar zonas del proyecto sin analizar.
Y cuando llegue el seguimiento, el porcentaje de avance del proyecto será la suma ponderada del avance de cada paquete. Ahí es donde «¿cuánto falta?» deja de ser una sensación.

📌 Por eso una EDT floja se paga tarde y caro. En la semana cuatro nadie nota que está incompleta; en la semana doce, cuando el seguimiento dice que vas al 70 % y en realidad falta la mitad, ya no hay margen para corregir.

Aplícalo a Tu Proyecto
Ahora sobre tu propio proyecto. Trabaja con tu equipo.

1. El nivel 1
Escribe entre cuatro y siete entregables y asígnale a cada uno un porcentaje del esfuerzo total. No busques precisión: usa tu criterio de qué parte es más grande. Verifica que sumen 100 %.

Acuérdate del bloque de gestión del proyecto.

2. Descompón hasta paquetes de trabajo
Baja un nivel, o dos donde haga falta. Para cada hoja, verifica las cuatro condiciones del Paso 2 y la regla 8/80. Vuelve a comprobar la regla del 100 % en cada nivel.

@startwbs
* <Tu proyecto> (100 %)
** 1. <Entregable> (__ %)
*** 1.1 <Paquete de trabajo>
*** 1.2 <Paquete de trabajo>
** 2. <Entregable> (__ %)
** 5. Gestión del proyecto (__ %)
@endwbs
3. El diccionario
Llena la tabla para todos los paquetes del primer entregable que van a construir, y para al menos dos paquetes de cada uno de los demás. El campo importante es el criterio de aceptación.

4. La OBS y la RACI
Escribe tu OBS —los roles reales del equipo, con nombres— y arma la matriz. Recorre columna por columna y verifica que cada paquete tenga exactamente una A.

5. Guárdalo donde se pueda versionar
En el repositorio del proyecto, junto al código. Si la EDT vive en un archivo suelto en el computador de alguien, en tres semanas va a haber cuatro versiones distintas y ninguna va a ser la buena.

Validación
Antes de dar la EDT por terminada, revísala contra estas siete preguntas. Son las mismas que se usan para evaluarla.

¿Los hijos suman exactamente el padre, en todos los niveles?
¿Todos los nodos son entregables (sustantivos) y no actividades (verbos)?
¿Cada paquete de trabajo cae entre 8 y 80 horas?
¿Cada paquete tiene un criterio de aceptación que se puede verificar?
¿Cada paquete tiene exactamente una A en la matriz RACI?
¿Está el bloque de gestión del proyecto?
¿Está en el repositorio, en un formato que se pueda editar y versionar?
Si alguna respuesta es «no», corrígela ahora. Cada una de las siete se paga después con intereses.

Errores Comunes
Descomponer por actividades. Ya lo vimos, y es el más frecuente. La señal de alarma son los verbos en los nombres de los nodos.

Descomponer hasta el infinito. Una EDT con doscientos paquetes de dos horas no la mantiene nadie. A las tres semanas está desactualizada y el equipo deja de mirarla.

Olvidar la gestión del proyecto. Las reuniones, la documentación y las sustentaciones existen y consumen tiempo. Si no están en la EDT, ese tiempo se lo quitan al desarrollo sin que nadie lo haya decidido.

Confundir la EDT con el cronograma. La EDT dice qué; el cronograma dice cuándo. La EDT no tiene fechas ni flechas de secuencia. El orden de las cajas no significa nada.

Dos personas con la A. Suena a responsabilidad compartida y es lo contrario: cuando algo falla, cada uno supone que respondía el otro.

Hacerla una sola vez. El alcance cambia. La EDT se actualiza con él, y esa actualización es una decisión consciente que queda registrada. Una EDT que no cambió en todo el semestre no es una EDT estable: es una que nadie volvió a mirar.
