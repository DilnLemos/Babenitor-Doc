# EDT – Babenitor

**Proyecto:** Babenitor – Sistema Inteligente de Monitoreo y Seguridad para Bebés
**Materia:** Gestión de Proyectos de Software
**Base:** Acta de Constitución (22/09/2026)
**Estado del documento:** Borrador – Pasos 1, 2 y 3 (Niveles 1 y 2 + Diccionario de la EDT)

---

## Decisiones del equipo

| Decisión | Resultado | Efecto en la EDT |
| -------- | --------- | ---------------- |
| Bloque de hardware | **Se mantiene como bloque propio (2.0)** | Sin cambio |
| Procesamiento del llanto | **En el ESP32 #1** | La detección de llanto queda en 3.0 |
| Generación de la alerta | **La genera la app** | Los ESP32 envían datos y eventos; las reglas de alerta están en 6.0 |
| Dónde llegan los datos | **Los ESP32 envían los datos a un servidor, que los retorna al teléfono y a la app para dar la alerta** | Nuevo paquete 5.8 (servidor intermediario); 5.3 y 5.4 pasan a ser "envío al servidor"; 5.1 baja de horas porque la decisión principal ya está tomada |
| Funcionamiento de la app | **Debe funcionar en segundo plano** | Queda como criterio de aceptación en 5.8, 6.2 y 6.6 |
| Carga del ESP32 #1 | **Se deja como está** | Sin cambio; sigue siendo el riesgo técnico principal |
| Horas estimadas | **Confirmadas por el equipo** | Total: 682 h (670 h + 16 h del servidor − 4 h de 5.1) |
| Fecha de entrega final | **Por confirmar** | Los paquetes de cierre (7.7 y 7.8) quedan sin fecha hasta confirmarla |

---

## Paso 1 – Nivel 1

**Criterio de partición:** mixta (componentes del producto + bloque de gestión).

```
0. BABENITOR
├── 1.0 Gestión del proyecto
├── 2.0 Adquisición y montaje del hardware
├── 3.0 ESP32 #1: cámara y micrófono (ubicación, llanto y sonidos fuertes)
├── 4.0 ESP32 #2: temperatura corporal
├── 5.0 Comunicación entre dispositivos, servidor y app
├── 6.0 Aplicación móvil Android (incluye la generación de alertas)
└── 7.0 Integración, pruebas y entrega final
```

---

## Paso 2 – Nivel 2: paquetes de trabajo

**Ola:** 1 = detallado ahora; 2 = grueso, se detalla cuando llegue el momento; R = esfuerzo recurrente.
**Horas:** estimación del equipo completo para cada paquete (confirmadas).

```
1.0 Gestión del proyecto (92 h)
├── 1.1 Plan del proyecto ........................ 16 h  [1]
├── 1.2 Actas de seguimiento semanal ............. 40 h  [R]
├── 1.3 Registro de riesgos y presupuesto ........ 12 h  [R]
└── 1.4 Informes de entregas parciales ........... 24 h  [2]

2.0 Adquisición y montaje del hardware (48 h)
├── 2.1 Lista de componentes cotizada ............  8 h  [1]
├── 2.2 Componentes recibidos ....................  8 h  [1]
├── 2.3 Componentes verificados ..................  8 h  [1]
├── 2.4 Prototipo físico armado .................. 16 h  [1]
└── 2.5 Habitación de pruebas ....................  8 h  [1]

3.0 ESP32 #1: cámara y micrófono (140 h)
├── 3.1 Firmware base del ESP32 #1 ............... 12 h  [1]
├── 3.2 Captura de imágenes ...................... 16 h  [1]
├── 3.3 Detección de la posición del bebé ........ 40 h  [1]
├── 3.4 Captura de audio ......................... 16 h  [1]
├── 3.5 Detección de llanto ..................... 32 h  [1]
├── 3.6 Detección de sonidos fuertes ............  8 h  [1]
└── 3.7 Calibración y pruebas del ESP32 #1 ...... 16 h  [2]

4.0 ESP32 #2: temperatura corporal (40 h)
├── 4.1 Firmware base y lectura del sensor ....... 12 h  [1]
├── 4.2 Calibración contra termómetro ............ 12 h  [1]
├── 4.3 Estabilización de lecturas ...............  8 h  [1]
└── 4.4 Pruebas del ESP32 #2 .....................  8 h  [2]

5.0 Comunicación entre dispositivos, servidor y app (102 h)
├── 5.1 Arquitectura de comunicación ............  8 h  [1]
├── 5.2 Formato de mensajes ......................  8 h  [1]
├── 5.3 Envío de datos del ESP32 #1 al servidor .. 20 h  [1]
├── 5.4 Envío de datos del ESP32 #2 al servidor .. 16 h  [1]
├── 5.5 Intercambio de datos entre los ESP32 ..... 12 h  [1]
├── 5.6 Reconexión automática .................... 10 h  [1]
├── 5.7 Privacidad y acceso autorizado ........... 12 h  [2]
└── 5.8 Servidor intermediario ................... 16 h  [1]

6.0 Aplicación móvil Android (132 h)
├── 6.1 Prototipo de interfaz .................... 16 h  [1]
├── 6.2 Base de la app y recepción en segundo plano 16 h [1]
├── 6.3 Pantalla de estado reciente .............. 20 h  [1]
├── 6.4 Configuración de zonas ................... 24 h  [1]
├── 6.5 Motor de alertas ......................... 32 h  [1]
├── 6.6 Notificaciones al cuidador ............... 12 h  [1]
└── 6.7 Historial de alertas ..................... 12 h  [2]

7.0 Integración, pruebas y entrega final (128 h)
├── 7.1 Plan de pruebas ..........................  8 h  [1]
├── 7.2 Sistema integrado ........................ 24 h  [1]
├── 7.3 Resultados de pruebas de zonas, llanto y sonidos fuertes 20 h [2]
├── 7.4 Resultados de la prueba de temperatura ...  8 h  [2]
├── 7.5 Resultados de tiempo de alerta y estabilidad 12 h [2]
├── 7.6 Sistema ajustado ........................ 24 h  [2]
├── 7.7 Documentación técnica y manual de uso .... 16 h  [2]
└── 7.8 Sustentación final ...................... 16 h  [2]
```

### Verificación del Paso 2

**Regla 8/80:** todos los paquetes están entre 8 y 80 horas (el mayor es 3.3, con 40 h). Excepción: 1.2 y 1.3 son esfuerzo recurrente y se reportan por semana o por mes en el cronograma.

**Regla del período de reporte (máximo dos períodos de seguimiento):** con reporte semanal y unas 10 h semanales por persona, un paquete no debería pasar de unas 20 h para una sola persona. Los que lo superan y conviene repartir entre dos personas: **3.3** (40 h), **3.5** (32 h) y **6.5** (32 h). En el límite: **6.4**, **7.2** y **7.6** (24 h).

**Regla del 100 %:**

| Requisito | Paquete(s) |
| --------- | ---------- |
| RF-01 | 3.2, 3.3 |
| RF-02 | 6.4 |
| RF-03 | 6.5, 6.6 |
| RF-04 | 3.4 |
| RF-05 | 3.5, 6.5 |
| RF-06 | 3.6, 6.5 |
| RF-07 | 4.1 |
| RF-08 | 6.5 |
| RF-09 | 5.3, 5.4, 5.5, 5.8 |
| RF-10 | 6.3 |
| RF-11 | 6.6 |
| RF-12 | 6.7 |
| RNF-01 | 5.1, 5.8, 7.5 |
| RNF-02 | 7.3, 7.6 |
| RNF-03 | 4.2, 7.4 |
| RNF-04 | 7.5 |
| RNF-05 | 5.6 |
| RNF-06 | 6.1 |
| RNF-07, RNF-08 | 5.7 |
| RNF-09 | 6.2 |
| RNF-10 | 1.3 |

**Esfuerzo total:**

| Bloque | Horas |
| ------ | ----- |
| 1.0 Gestión | 92 |
| 2.0 Hardware | 48 |
| 3.0 ESP32 #1 | 140 |
| 4.0 ESP32 #2 | 40 |
| 5.0 Comunicación | 102 |
| 6.0 App móvil | 132 |
| 7.0 Integración y pruebas | 128 |
| **Total** | **682 h** (unas 136 h por integrante) |

---

## Paso 3 – Diccionario de la EDT

Una fila por paquete de trabajo. Reglas de uso:

- **Criterio de aceptación:** se escribe **antes** de empezar el paquete. Si durante el trabajo se descubre que está mal, se cambia en equipo y queda anotado, no se ajusta al final a lo que alcanzamos a hacer.
- **Responsable:** una sola persona. Queda **por asignar** hasta construir la OBS (Paso 4).
- **Cifras de los criterios:** las que vienen del acta (8 de 10, ±0,5 °C, 10 s, 30 min) son obligatorias. Las que no están en el acta (por ejemplo "1 cuadro por segundo" o "5 s") son **propuestas mías para que el equipo las confirme o cambie**.
- **Depende de:** paquetes que deben estar terminados antes (o al menos avanzados) para poder empezar.

### 1.0 Gestión del proyecto

| Código | Nombre | Descripción | Criterio de aceptación | Responsable | Horas | Depende de |
| ------ | ------ | ----------- | ---------------------- | ----------- | ----- | ---------- |
| 1.1 | Plan del proyecto | Elaborar la EDT con su diccionario, la OBS, el cronograma y la matriz de roles del equipo. | EDT, OBS y cronograma entregados al profesor; el cronograma incluye los 43 paquetes con responsable y fechas hasta el hito del 01/12; el profesor los aprueba. | Por asignar | 16 | — |
| 1.2 | Actas de seguimiento semanal | Reunión semanal del equipo para revisar el avance, los bloqueos y los acuerdos. | Existe un acta por cada semana con el avance de cada paquete, los acuerdos y los pendientes; no queda ningún paquete sin reportar. | Por asignar | 40 | 1.1 |
| 1.3 | Registro de riesgos y presupuesto | Mantener actualizados los riesgos del acta y el gasto acumulado. | Registro actualizado al cierre de cada mes con estado de cada riesgo y gasto acumulado con sus facturas; el gasto total no supera los $300.000 COP. | Por asignar | 12 | 1.1 |
| 1.4 | Informes de entregas parciales | Redactar los informes que el profesor pida en cada entrega parcial. | Un informe por entrega parcial, enviado antes de la fecha límite, con el avance frente al cronograma. | Por asignar | 24 | 1.1 |

### 2.0 Adquisición y montaje del hardware

| Código | Nombre | Descripción | Criterio de aceptación | Responsable | Horas | Depende de |
| ------ | ------ | ----------- | ---------------------- | ----------- | ----- | ---------- |
| 2.1 | Lista de componentes cotizada | Elegir y cotizar el ESP32-CAM, el segundo ESP32, el micrófono y el sensor de temperatura. | Lista con proveedor y precio de cada componente, total dentro del presupuesto, aprobada por el equipo; el sensor de temperatura declara una precisión compatible con ±0,5 °C. | Por asignar | 8 | — |
| 2.2 | Componentes recibidos | Comprar los componentes de la lista y recibirlos. | Todos los ítems de la lista están en poder del equipo, cotejados uno a uno, y las facturas quedan registradas en 1.3. | Por asignar | 8 | 2.1 |
| 2.3 | Componentes verificados | Probar cada componente por separado antes de armar el prototipo. | Cada ESP32 enciende y se puede programar; el micrófono entrega señal; el sensor entrega una lectura; las piezas defectuosas quedan reportadas con su reemplazo pedido. | Por asignar | 8 | 2.2 |
| 2.4 | Prototipo físico armado | Conectar los componentes y fijarlos en soportes para los dos dispositivos. | Ambos dispositivos conectados, alimentados y fijos, encendidos 30 minutos seguidos sin reinicios por fallas de conexión física. | Por asignar | 16 | 2.3 |
| 2.5 | Habitación de pruebas | Preparar el espacio donde se harán todas las pruebas. | Espacio con Wi-Fi estable, muñeco de prueba, zona segura y zonas de riesgo marcadas, y posición de la cámara registrada con una foto. | Por asignar | 8 | — |

### 3.0 ESP32 #1: cámara y micrófono

| Código | Nombre | Descripción | Criterio de aceptación | Responsable | Horas | Depende de |
| ------ | ------ | ----------- | ---------------------- | ----------- | ----- | ---------- |
| 3.1 | Firmware base del ESP32 #1 | Configurar el entorno de desarrollo y el programa mínimo del dispositivo. | El dispositivo arranca, se conecta al Wi-Fi y captura un cuadro de la cámara, verificable por el monitor serial; el código está en el repositorio. | Por asignar | 12 | 2.3 |
| 3.2 | Captura de imágenes | Capturar imágenes de forma continua para el análisis de posición. | Durante 5 minutos captura al menos 1 cuadro por segundo sin bloquearse. | Por asignar | 16 | 3.1 |
| 3.3 | Detección de la posición del bebé | Algoritmo que localiza al muñeco en la imagen y reporta su posición (coordenadas); la comparación con las zonas la hace la app. | En 10 pruebas con el muñeco en distintos puntos, la posición reportada corresponde a dónde está realmente (contra las zonas marcadas en 2.5) en al menos 8. | Por asignar | 40 | 3.2, 2.5 |
| 3.4 | Captura de audio | Capturar y muestrear el audio del micrófono. | Durante 5 minutos muestrea audio sin interrupciones y se obtiene el nivel de volumen y las frecuencias, verificable en el monitor serial. | Por asignar | 16 | 3.1, 2.3 |
| 3.5 | Detección de llanto | Analizar la frecuencia del audio en el propio ESP32 para identificar llanto. | Con 10 reproducciones de llanto de bebé genera el evento "llanto" en al menos 8; con 10 muestras de conversación normal no lo genera en al menos 8. | Por asignar | 32 | 3.4 |
| 3.6 | Detección de sonidos fuertes | Generar un evento cuando el volumen supere un umbral. | Con 10 sonidos que superan el umbral genera el evento en al menos 8; el umbral queda escrito en la documentación. | Por asignar | 8 | 3.4 |
| 3.7 | Calibración y pruebas del ESP32 #1 | Ajustar umbrales y probar el dispositivo por separado. | Reporte con los resultados de 3.3, 3.5 y 3.6 después del ajuste; el dispositivo funciona 30 minutos seguidos sin reiniciarse. | Por asignar | 16 | 3.3, 3.5, 3.6 |

### 4.0 ESP32 #2: temperatura corporal

| Código | Nombre | Descripción | Criterio de aceptación | Responsable | Horas | Depende de |
| ------ | ------ | ----------- | ---------------------- | ----------- | ----- | ---------- |
| 4.1 | Firmware base y lectura del sensor | Programa que lee el sensor de temperatura y entrega el valor. | El dispositivo arranca, se conecta al Wi-Fi y muestra la temperatura leída a la frecuencia definida por el equipo; el código está en el repositorio. | Por asignar | 12 | 2.3 |
| 4.2 | Calibración contra termómetro | Comparar el sensor con un termómetro de referencia y corregir el error. | En al menos 10 mediciones, ninguna difiere más de ±0,5 °C del termómetro de referencia; la tabla de comparación queda en la documentación. | Por asignar | 12 | 4.1 |
| 4.3 | Estabilización de lecturas | Filtrar el ruido para que la lectura no salte. | Con temperatura constante durante 2 minutos, las lecturas varían menos de ±0,2 °C. | Por asignar | 8 | 4.1 |
| 4.4 | Pruebas del ESP32 #2 | Probar el dispositivo por separado. | Reporte de pruebas; el dispositivo envía lecturas 30 minutos seguidos sin pérdidas ni reinicios. | Por asignar | 8 | 4.2, 4.3 |

### 5.0 Comunicación entre dispositivos, servidor y app

| Código | Nombre | Descripción | Criterio de aceptación | Responsable | Horas | Depende de |
| ------ | ------ | ----------- | ---------------------- | ----------- | ----- | ---------- |
| 5.1 | Arquitectura de comunicación | Definir el flujo ESP32 → servidor → app, el protocolo, qué datos viajan y dónde se aloja el servidor. | Documento con diagrama del flujo, protocolo elegido, lista de datos que viajan (sin audio ni video crudos) y su justificación, aprobado por el equipo. | Por asignar | 8 | — |
| 5.2 | Formato de mensajes | Especificar los mensajes que intercambian los dispositivos, el servidor y la app. | Especificación con los campos de temperatura, posición, eventos de llanto y sonido y estado de conexión, con ejemplos; ESP32 #1, ESP32 #2 y app la usan sin cambiarla. | Por asignar | 8 | 5.1 |
| 5.3 | Envío de datos del ESP32 #1 al servidor | Enviar posición y eventos de audio del ESP32 #1 al servidor. | Durante 5 minutos el servidor recibe y registra la posición y los eventos de audio, sin mensajes perdidos. | Por asignar | 20 | 5.2, 5.8, 3.1 |
| 5.4 | Envío de datos del ESP32 #2 al servidor | Enviar la temperatura del ESP32 #2 al servidor. | Durante 5 minutos el servidor recibe y registra la temperatura de forma continua, sin mensajes perdidos. | Por asignar | 16 | 5.2, 5.8, 4.1 |
| 5.5 | Intercambio de datos entre los ESP32 | Los dos dispositivos se comunican entre sí (estado de conexión y última lectura). | Cada ESP32 recibe el estado del otro y detecta si el otro se desconectó. | Por asignar | 12 | 5.2, 3.1, 4.1 |
| 5.6 | Reconexión automática | Cada ESP32 recupera la conexión sin ayuda. | Tras apagar el Wi-Fi 1 minuto y volver a encenderlo, cada dispositivo vuelve a enviar datos sin intervención manual. | Por asignar | 10 | 5.3, 5.4 |
| 5.7 | Privacidad y acceso autorizado | Proteger los datos y limitar quién puede leer o enviar. | El audio y el video crudos no salen de la red local ni se guardan; un dispositivo o app sin credenciales no puede leer ni enviar datos al servidor (probado). | Por asignar | 12 | 5.3, 5.4, 5.8 |
| 5.8 | Servidor intermediario | Servicio que recibe lecturas y eventos de los ESP32 y los reenvía al teléfono, incluso con la app en segundo plano (por ejemplo con notificaciones push). Solo retransmite; no procesa. | Un dato enviado por un ESP32 llega al teléfono con la app cerrada o en segundo plano en menos de 5 s. | Por asignar | 16 | 5.1, 5.2 |

### 6.0 Aplicación móvil Android

| Código | Nombre | Descripción | Criterio de aceptación | Responsable | Horas | Depende de |
| ------ | ------ | ----------- | ---------------------- | ----------- | ----- | ---------- |
| 6.1 | Prototipo de interfaz | Dibujar las pantallas de estado, zonas, alertas e historial. | Pantallas aprobadas por el equipo; una persona ajena al proyecto encuentra el estado del bebé y una alerta sin explicación (RNF-06). | Por asignar | 16 | — |
| 6.2 | Base de la app y recepción en segundo plano | Proyecto Android que se conecta al servidor y sigue recibiendo datos con la app en segundo plano. | App instalada en un teléfono Android que recibe datos del servidor durante 10 minutos con la pantalla bloqueada o la app en segundo plano. | Por asignar | 16 | 6.1, 5.8 |
| 6.3 | Pantalla de estado reciente | Mostrar ubicación, temperatura y sonido más recientes del bebé. | La pantalla muestra los tres datos y se actualiza sin que el usuario la refresque; los datos vienen del servidor, no están escritos en el código. | Por asignar | 20 | 6.2, 5.3, 5.4 |
| 6.4 | Configuración de zonas | Permitir al cuidador definir zonas seguras y de riesgo. | El cuidador crea, edita y borra zonas seguras y de riesgo sobre la vista de la habitación, y las zonas siguen ahí al cerrar y abrir la app. | Por asignar | 24 | 6.1, 6.2 |
| 6.5 | Motor de alertas | Reglas que deciden cuándo hay alerta a partir de los datos recibidos y las zonas configuradas. | Genera la alerta correcta ante entrada a zona de riesgo o salida de zona segura, llanto, sonido fuerte y temperatura fuera de rango; cada caso probado con los casos de 7.1; no repite la misma alerta más de una vez por evento. | Por asignar | 32 | 6.3, 6.4 |
| 6.6 | Notificaciones al cuidador | Avisar cada alerta como notificación del teléfono. | Cada alerta llega como notificación con tipo y hora del evento, incluso con la app en segundo plano. | Por asignar | 12 | 6.5 |
| 6.7 | Historial de alertas | Guardar y mostrar las alertas recientes. | Lista de alertas ordenadas por hora con su tipo, que se mantiene después de cerrar y abrir la app. | Por asignar | 12 | 6.5 |

### 7.0 Integración, pruebas y entrega final

| Código | Nombre | Descripción | Criterio de aceptación | Responsable | Horas | Depende de |
| ------ | ------ | ----------- | ---------------------- | ----------- | ----- | ---------- |
| 7.1 | Plan de pruebas | Definir cómo se comprobará cada criterio de éxito del acta. | Tabla con un caso por cada criterio de éxito (6), con pasos, resultado esperado y responsable, aprobada por el equipo antes de ejecutar pruebas. | Por asignar | 8 | 1.1 |
| 7.2 | Sistema integrado | Unir los dos ESP32, el servidor y la app en un solo sistema. | En una demostración, un evento de cada tipo (posición, llanto, sonido fuerte y temperatura) viaja desde el dispositivo hasta la app y genera su alerta. | Por asignar | 24 | 3.7, 4.4, 5.5, 5.6, 6.6 |
| 7.3 | Resultados de pruebas de zonas, llanto y sonidos fuertes | Ejecutar las pruebas del plan para estos tres criterios. | Tabla con 10 pruebas por criterio y al menos 8 aciertos en cada uno. | Por asignar | 20 | 7.1, 7.2 |
| 7.4 | Resultados de la prueba de temperatura | Ejecutar la prueba de precisión con el sistema completo. | Todas las mediciones registradas están dentro de ±0,5 °C del termómetro de referencia. | Por asignar | 8 | 7.1, 7.2 |
| 7.5 | Resultados de tiempo de alerta y estabilidad | Medir el tiempo de las alertas y la comunicación continua. | Tiempo medido en cada evento, con la alerta en la app en menos de 10 s, y 30 minutos de prueba continua sin pérdida de comunicación. | Por asignar | 12 | 7.1, 7.2 |
| 7.6 | Sistema ajustado | Corregir defectos y ajustar umbrales según los resultados. | Una pasada final de pruebas cumple todos los criterios del acta y no quedan defectos críticos abiertos. | Por asignar | 24 | 7.3, 7.4, 7.5 |
| 7.7 | Documentación técnica y manual de uso | Documentar arquitectura, conexiones, instalación y configuración. | Documento entregado; una persona ajena al equipo puede encender y configurar el sistema siguiendo el manual. | Por asignar | 16 | 7.6 |
| 7.8 | Sustentación final | Preparar y realizar la presentación y demostración al profesor. | Presentación y demostración realizadas mostrando el cumplimiento de los criterios de éxito (**fecha por confirmar**). | Por asignar | 16 | 7.6, 7.7 |

---

## Puntos a revisar antes del siguiente paso

1. **El servidor y el acta.** El acta dice que no se incorporan servidores dedicados *para el procesamiento* y que audio y video solo se transmiten dentro de la red local (RNF-07). El servidor intermediario es compatible si **solo retransmite** lecturas y eventos y **no recibe audio ni video crudos**. Así quedó escrito en 5.1, 5.7 y 5.8. Conviene confirmarlo con el profesor, y decidir dónde se aloja el servidor (servicio en la nube gratuito o equipo del grupo) y que no pase del presupuesto.
2. **Posición y zonas.** Asumí que el ESP32 #1 reporta solo la posición del bebé y que **la app compara con las zonas** (porque la app genera las alertas). Si prefieren que el ESP32 conozca las zonas, cambian 3.3, 5.2 y 6.4.
3. **Cifras no definidas en el acta.** Los valores propuestos (1 cuadro por segundo, 5 s del servidor al teléfono, variación de ±0,2 °C, 10 pruebas de falsos positivos) son míos y hay que confirmarlos.
4. **Responsables.** Todo está por asignar hasta que armemos la OBS.
5. **Fecha de entrega final** sigue por confirmar (afecta 7.7 y 7.8).

---

## Siguiente paso

**Paso 4:** OBS (estructura de la organización: asignar a los 5 integrantes), después la matriz de responsabilidades y la conversión a cronograma con las dependencias de este diccionario.

*Este documento se irá actualizando con cada paso.*