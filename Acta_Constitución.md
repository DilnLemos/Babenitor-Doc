# BABENITOR - Sistema Inteligente de Monitoreo y Seguridad para Bebés

## Información Relevante

**Fecha de Acta**: 22/09/2026

## Descripción General

Sistema prototipo de monitoreo inteligente para bebés, compuesto por dos dispositivos basados en ESP32. El primero contará con cámara y micrófono para detectar el movimiento y ubicación del bebé dentro de la habitación, transmitir audio y generar alertas ante llanto o sonidos fuertes inusuales. El segundo dispositivo contará con sensores destinados a medir la temperatura corporal del bebé. La información será comunicada y presentada mediante una aplicación móvil, permitiendo al cuidador consultar el estado reciente del bebé y recibir alertas cuando se detecten condiciones consideradas anormales o inseguras.

| Función             | Qué hará                                            |
| ------------------- | --------------------------------------------------- |
|  **Ubicación**      | Detectar dónde está el bebé dentro de la habitación |
|  **Audio**          | Transmitir audio y detectar llanto/sonidos fuertes  |
|  **Temperatura**    | Medir temperatura corporal                          |
|  **Alertas**        | Avisar sobre situaciones potencialmente inseguras   |

---

## Problema

La dificultad de supervisar continuamente las condiciones de seguridad de un bebé cuando permanece solo en una habitación, particularmente su ubicación dentro del espacio, la presencia de sonidos que puedan indicar una situación de alerta y posibles variaciones anormales de su temperatura corporal.

---

## Justificación

La supervisión constante de un bebé puede resultar difícil para sus cuidadores cuando este permanece solo en una habitación. En estas situaciones, puede ser necesario conocer su ubicación dentro del espacio, identificar sonidos que puedan requerir atención y detectar variaciones anormales en su temperatura corporal. Por esta razón, se propone desarrollar un prototipo de monitoreo basado en dispositivos ESP32 que permita recopilar y comunicar esta información, generar alertas ante determinadas condiciones y facilitar al cuidador el seguimiento remoto mediante una aplicación móvil.

--- 

## Objetivo

Desarrollar un prototipo de monitoreo para bebés basado en dispositivos ESP32 que permita detectar la ubicación del bebé dentro de zonas predefinidas de una habitación, monitorear su temperatura corporal y sonidos del entorno, y generar alertas ante condiciones previamente establecidas por medio de sonidos inusuales o areas definidas como no seguras, presentando la información mediante una aplicación móvil.

## Alcance

El prototipo podra decir si el infante se ubica en el lugar predispuesto por el usuario, podra identificar el llanto basado en la frecuencia de la voz, podra medir la temperatura de infante y alertar cualquier temperatura anomala y en general el dispositivo basado en todas la medidas anteriores podra decidir si enviar alertas para los padres del infante
### Lo que NO incluye

El prototipo se limita a monitorear y alertar, por lo que no realiza ningún tipo de diagnóstico médico ni interpreta las mediciones como indicadores de enfermedad; tampoco ejecuta acciones físicas sobre el bebé ni sobre su entorno (mecer la cuna, regular la temperatura de la habitación, etc.). Babenitor no reemplaza la supervisión de un adulto responsable, sino que funciona como un apoyo para el cuidador, quien sigue siendo el encargado de verificar y atender cualquier situación. El monitoreo se restringe a una única habitación previamente configurada para el prototipo, de modo que no se contempla el seguimiento del bebé fuera de ese espacio ni en exteriores. Finalmente, al tratarse de un prototipo académico, el sistema no cuenta ni busca obtener certificación como dispositivo médico o comercial.

---

## Criterios de Éxito

Para el cuidador, el proyecto será exitoso si puede consultar desde la aplicación móvil el estado reciente del bebé (ubicación, temperatura y sonido) y recibe alertas oportunas y comprensibles cuando ocurre una situación de riesgo, sin verse saturado por falsas alarmas. Para el equipo, el éxito consiste en entregar al final del semestre los dos ESP32 funcionando e integrados, comunicándose entre sí y con la aplicación. Para los profesores, el proyecto deberá demostrar técnicamente la captura de datos de sensores, su procesamiento para detectar eventos y la comunicación entre dispositivos y la aplicación en tiempo cercano al real. Estos criterios se consideran cumplidos si en las pruebas dentro de la habitación configurada se verifican las siguientes condiciones:

| Criterio               | Condición verificable                                                                                  |
| ---------------------- | ------------------------------------------------------------------------------------------------------ |
| **Zonas de riesgo**    | Se genera una alerta en al menos 8 de 10 pruebas en que el bebé (o un objeto de prueba) entra en una zona no segura |
| **Llanto**             | Se detecta el llanto en al menos 8 de 10 reproducciones de llanto de bebé                               |
| **Sonidos anormales**  | Se genera alerta ante sonidos fuertes que superen el umbral definido en al menos 8 de 10 pruebas        |
| **Temperatura**        | La medición difiere en máximo ±0,5 °C respecto a un termómetro de referencia                            |
| **Tiempo de alerta**   | La alerta llega a la aplicación en menos de 10 segundos después de ocurrido el evento                   |
| **Comunicación**       | Los dos ESP32 y la aplicación intercambian datos de forma continua durante una prueba de 30 minutos     |

---

## Stakeholders

Los principales interesados en el proyecto son el equipo de desarrollo, conformado por los cinco integrantes, quienes diseñan, construyen, configuran y mantienen el prototipo durante el semestre; el profesor del curso, quien establece los requisitos, las reglas y los criterios de evaluación; y la Universidad del Valle, que enmarca el proyecto académico y sus lineamientos. Al no existir un patrocinador externo, el proyecto es financiado con recursos propios del equipo. Los usuarios principales del sistema son los padres o cuidadores, quienes consultarán la aplicación, configurarán las zonas seguras y recibirán las alertas. También se consideran afectados el bebé, cuya seguridad depende de que el sistema no omita eventos importantes; los demás habitantes del hogar, cuya privacidad puede verse comprometida por la cámara y el micrófono; y los cuidadores frente a posibles falsas alarmas. Por último, los proveedores de componentes electrónicos influyen en la disponibilidad de los ESP32 y sensores.

| Stakeholder                   | Rol en el proyecto                                   |
| ----------------------------- | ---------------------------------------------------- |
| **Equipo de desarrollo**      | Diseña, desarrolla, opera y mantiene el prototipo; lo financia |
| **Profesor del curso**        | Establece reglas y requisitos, evalúa y aprueba     |
| **Universidad del Valle**     | Institución que enmarca el proyecto académico        |
| **Padres / cuidadores**       | Usuarios principales: configuran zonas y reciben alertas |
| **Bebé**                      | Sujeto monitoreado; afectado por fallos o detecciones omitidas |
| **Otros habitantes del hogar**| Afectados por la privacidad de cámara y micrófono   |
| **Proveedores de componentes**| Suministran ESP32 y sensores                        |

---

## Matriz Poder/Interés

Para clasificar a los stakeholders se evaluó su poder, entendido como la capacidad de tomar decisiones o afectar el rumbo del proyecto, y su interés, entendido como qué tanto les importa directamente el resultado. El equipo de desarrollo y el profesor del curso tienen alto poder y alto interés: el equipo decide cómo se construye el prototipo y lo financia, mientras que el profesor define los requisitos y aprueba el proyecto, por lo que ambos se gestionan de cerca. La Universidad del Valle tiene alto poder por enmarcar el proyecto y sus lineamientos, pero bajo interés en sus detalles, así que basta con mantenerla satisfecha cumpliendo las normas académicas. Los padres o cuidadores, el bebé y los demás habitantes del hogar tienen bajo poder sobre las decisiones del proyecto, pero alto interés, porque son quienes usan el sistema o se ven afectados por su funcionamiento, sus fallos o la privacidad de la cámara y el micrófono; por ello se mantienen informados. Por último, los proveedores de componentes tienen bajo poder y bajo interés en el resultado, de modo que solo se monitorean para vigilar la disponibilidad y el precio de los componentes.

| Stakeholder                    | Poder | Interés | Cuadrante                     | Estrategia               |
| ------------------------------ | ----- | ------- | ----------------------------- | ------------------------ |
| **Equipo de desarrollo**       | Alto  | Alto    | Alto poder + alto interés     | Gestionar de cerca       |
| **Profesor del curso**         | Alto  | Alto    | Alto poder + alto interés     | Gestionar de cerca       |
| **Universidad del Valle**      | Alto  | Bajo    | Alto poder + bajo interés     | Mantener satisfecho      |
| **Padres / cuidadores**        | Bajo  | Alto    | Bajo poder + alto interés     | Mantener informado       |
| **Bebé**                       | Bajo  | Alto    | Bajo poder + alto interés     | Mantener informado (a través de sus cuidadores) |
| **Otros habitantes del hogar** | Bajo  | Alto    | Bajo poder + alto interés     | Mantener informado       |
| **Proveedores de componentes** | Bajo  | Bajo    | Bajo poder + bajo interés     | Monitorear               |

---

## Expectativas de Stakeholders

Cada uno de los stakeholders principales espera algo distinto del proyecto y, por tanto, mide su éxito de forma diferente. El equipo de desarrollo espera aprobar el curso con un prototipo funcional y aprender sobre sistemas embebidos y comunicación entre dispositivos, por lo que se coordina de forma continua por WhatsApp y en reuniones semanales de seguimiento. El profesor espera que el prototipo cumpla los requisitos del curso y demuestre técnicamente la captura, el procesamiento y la comunicación de datos; con él la comunicación se realiza en las clases, asesorías y entregas parciales, y por correo institucional cuando sea necesario. La Universidad del Valle espera que el proyecto se desarrolle conforme a sus lineamientos académicos, lo cual se canaliza a través del profesor en cada entrega. Los padres o cuidadores, representados en el prototipo por los propios integrantes durante las pruebas, esperan un sistema confiable y fácil de usar que les avise a tiempo sin generar falsas alarmas; su retroalimentación se recoge en las sesiones de prueba. Los demás habitantes del hogar esperan que la cámara y el micrófono no comprometan su privacidad, por lo que se les informa antes de cada prueba. Finalmente, con los proveedores de componentes el contacto se limita a sus tiendas físicas o en línea al momento de cotizar y comprar.

| Stakeholder              | Expectativa                                              | Criterio de éxito                                              | Forma de contacto                  | Frecuencia                      |
| ------------------------ | -------------------------------------------------------- | -------------------------------------------------------------- | ---------------------------------- | ------------------------------- |
| **Equipo de desarrollo** | Aprobar el curso y aprender sobre sistemas embebidos      | Prototipo integrado y entregado a tiempo                       | WhatsApp, reuniones del equipo     | Diaria (chat) / semanal (reunión) |
| **Profesor del curso**   | Prototipo que cumpla los requisitos y sea demostrable     | Aprobación de entregas parciales y de la presentación final    | Clases, asesorías, correo institucional | Semanal y en cada entrega    |
| **Universidad del Valle**| Proyecto alineado con los lineamientos académicos         | Proyecto evaluado y aprobado dentro del curso                  | A través del profesor              | En cada entrega                 |
| **Padres / cuidadores**  | Alertas oportunas y aplicación fácil de usar              | Se cumplen los criterios de éxito sin saturar de falsas alarmas | Sesiones de prueba del prototipo  | En cada fase de pruebas         |
| **Otros habitantes del hogar** | Que no se vulnere su privacidad                     | Grabaciones usadas solo para pruebas y no almacenadas sin consentimiento | Conversación directa      | Antes de cada prueba            |
| **Proveedores de componentes** | Venta de los componentes                            | Componentes disponibles a tiempo y dentro del presupuesto      | Tienda física o en línea           | Al momento de cada compra       |

---

## Supuestos

Para planear el proyecto se asume que el equipo contará con los dos ESP32 requeridos (uno con cámara, tipo ESP32-CAM, y otro para los sensores) y que podrá conseguir en el mercado local o en línea un micrófono y un sensor de temperatura adecuados para el prototipo. También se asume, de forma temporal hasta validarlo en las primeras pruebas, que ambos ESP32 podrán comunicarse entre sí de forma estable a través de la red Wi-Fi de la habitación, y que el equipo tiene los conocimientos necesarios para desarrollar una aplicación móvil capaz de recibir y mostrar la información. Por último, se asume que todas las pruebas se realizarán en un entorno controlado: una única habitación configurada para el prototipo, con conexión Wi-Fi y en la que se usará un objeto o muñeco de prueba en lugar de un bebé real.

| Supuesto                          | Descripción                                                                   |
| --------------------------------- | ----------------------------------------------------------------------------- |
| **Disponibilidad de ESP32**       | Se contará con los dos ESP32 (uno con cámara) durante todo el semestre         |
| **Disponibilidad de sensores**    | Se podrán conseguir el micrófono y el sensor de temperatura a tiempo           |
| **Comunicación entre dispositivos** | Ambos ESP32 podrán comunicarse por Wi-Fi entre sí y con la aplicación       |
| **Aplicación móvil**              | El equipo podrá desarrollar una app que reciba y muestre los datos y alertas  |
| **Entorno controlado**            | Las pruebas se harán en una habitación configurada, con muñeco u objeto de prueba |

---

## Restricciones

El proyecto debe desarrollarse dentro del semestre académico, iniciando con la fecha de esta acta (22/09/2026) y finalizando en la fecha de entrega final que establezca el profesor. Al ser financiado con recursos propios del equipo, el presupuesto es limitado, por lo que se priorizan componentes económicos y de fácil acceso. En cuanto al hardware, el sistema debe construirse principalmente sobre los dos ESP32 establecidos, sin incorporar computadores o servidores dedicados para el procesamiento. El equipo está conformado por cinco integrantes, quienes deben repartirse el desarrollo de hardware, firmware, aplicación móvil y documentación. Además, el resultado será un prototipo académico y no un producto comercial, por lo que no se exigen acabados, certificaciones ni pruebas con bebés reales. Respecto a las tecnologías, el uso de ESP32 es obligatorio, mientras que el entorno de programación de los dispositivos, el protocolo de comunicación y la tecnología de la aplicación móvil pueden ser elegidos libremente por el equipo.

| Restricción              | Descripción                                                                  |
| ------------------------ | ---------------------------------------------------------------------------- |
| **Tiempo**               | Desde el 22/09/2026 hasta la entrega final del semestre (fecha por confirmar) |
| **Presupuesto**          | Recursos propios del equipo; máximo estimado de $300.000 COP                 |
| **Hardware**             | Dos ESP32 como base del sistema, más los sensores necesarios                 |
| **Tamaño del equipo**    | 5 integrantes                                                                |
| **Nivel del prototipo**  | Prototipo académico, no producto comercial ni dispositivo médico             |
| **Tecnologías**          | ESP32 obligatorio; lenguaje, protocolo y tecnología de la app a elección del equipo |

---

## Riesgos Iniciales

Uno de los principales riesgos es que los dos ESP32 pierdan la conexión o presenten retrasos en la comunicación, ya sea entre ellos o con la aplicación, lo que impediría que las alertas lleguen a tiempo. También existe el riesgo de detecciones incorrectas: falsos positivos que saturen al cuidador con alarmas innecesarias, o falsos negativos que omitan un evento real, tanto en la ubicación como en la detección de llanto y de sonidos fuertes. Por otro lado, el sensor de temperatura elegido podría no ofrecer la precisión suficiente para el propósito del prototipo, especialmente si mide a distancia o se ve afectado por la temperatura ambiente. Finalmente, la integración de hardware, firmware y aplicación móvil puede tomar más tiempo del esperado, poniendo en riesgo la entrega dentro del semestre.

| Riesgo                              | Probabilidad | Impacto | Mitigación                                                                     |
| ----------------------------------- | ------------ | ------- | ------------------------------------------------------------------------------ |
| **Fallas de comunicación entre ESP32** | Media     | Alto    | Probar la comunicación desde el inicio y agregar reconexión automática         |
| **Detección incorrecta**            | Alta         | Alto    | Calibrar umbrales con pruebas repetidas y ajustar según los resultados         |
| **Medición de temperatura imprecisa** | Media      | Medio   | Comparar con un termómetro de referencia y calibrar el sensor                  |
| **Tiempo insuficiente**             | Media        | Alto    | Integrar por etapas y priorizar las funciones principales sobre las adicionales |

---

## Hitos Principales

Las siguientes fechas son estimadas y podrán ajustarse según el calendario académico y las entregas definidas por el profesor.

| Hito                                 | Fecha estimada | Descripción                                                          |
| ------------------------------------ | -------------- | -------------------------------------------------------------------- |
| **Inicio del proyecto**              | 22/09/2026     | Aprobación del acta de constitución                                  |
| **Diseño del prototipo**             | 20/10/2026     | Selección de componentes, arquitectura y diseño de la aplicación     |
| **Integración de ESP32 + sensores**  | 10/11/2026     | Ambos ESP32 capturando datos y comunicándose entre sí                |
| **Primera versión funcional**        | 01/12/2026     | Sistema completo enviando datos y alertas a la aplicación            |
| **Pruebas y presentación final**     | Por confirmar  | Verificación de los criterios de éxito y entrega final al profesor   |

---

## Requisitos Funcionales

Los requisitos funcionales describen lo que el sistema debe hacer para cumplir el objetivo del proyecto. En términos generales, el prototipo debe detectar la ubicación del bebé y compararla con las zonas configuradas por el cuidador, analizar el audio de la habitación para identificar llanto y sonidos fuertes, medir la temperatura corporal, comunicar estos datos entre los dos ESP32 y la aplicación móvil, y generar alertas cuando alguna de estas condiciones se considere anormal o insegura.

| ID        | Requisito                                                                                         |
| --------- | ------------------------------------------------------------------------------------------------- |
| **RF-01** | El sistema debe detectar la ubicación del bebé dentro de la habitación mediante la cámara del ESP32 #1 |
| **RF-02** | El cuidador debe poder configurar desde la aplicación las zonas seguras y las zonas de riesgo     |
| **RF-03** | El sistema debe generar una alerta cuando el bebé entre en una zona de riesgo o salga de la zona segura |
| **RF-04** | El sistema debe capturar el audio de la habitación mediante el micrófono del ESP32 #1             |
| **RF-05** | El sistema debe detectar el llanto del bebé y generar la alerta correspondiente                    |
| **RF-06** | El sistema debe generar una alerta ante sonidos fuertes que superen el umbral definido             |
| **RF-07** | El sistema debe medir la temperatura corporal del bebé mediante el sensor del ESP32 #2             |
| **RF-08** | El sistema debe generar una alerta cuando la temperatura esté fuera del rango normal definido     |
| **RF-09** | Los dos ESP32 deben intercambiar datos entre sí y enviarlos a la aplicación móvil                 |
| **RF-10** | La aplicación debe mostrar el estado reciente del bebé: ubicación, temperatura y sonido           |
| **RF-11** | La aplicación debe notificar al cuidador cada alerta, indicando su tipo y la hora del evento       |
| **RF-12** | La aplicación debe permitir consultar el historial reciente de alertas                             |

---

## Requisitos No Funcionales

Los requisitos no funcionales establecen las condiciones de calidad con las que el sistema debe operar. Estos se relacionan directamente con los criterios de éxito: las alertas deben llegar rápido, las detecciones deben ser confiables, la comunicación debe mantenerse estable y la aplicación debe ser fácil de usar para cualquier cuidador. Además, por el uso de cámara y micrófono, el sistema debe proteger la privacidad de las personas del hogar.

| ID         | Categoría          | Requisito                                                                                    |
| ---------- | ------------------ | -------------------------------------------------------------------------------------------- |
| **RNF-01** | Rendimiento        | Las alertas deben llegar a la aplicación en menos de 10 segundos después de ocurrido el evento |
| **RNF-02** | Confiabilidad      | Las detecciones de zona, llanto y sonidos fuertes deben acertar en al menos 8 de cada 10 pruebas |
| **RNF-03** | Precisión          | La temperatura medida debe diferir máximo ±0,5 °C respecto a un termómetro de referencia      |
| **RNF-04** | Disponibilidad     | El sistema debe funcionar de forma continua durante al menos 30 minutos sin perder comunicación |
| **RNF-05** | Disponibilidad     | Si un ESP32 pierde la conexión, debe intentar reconectarse automáticamente                   |
| **RNF-06** | Usabilidad         | La aplicación debe ser comprensible para un cuidador sin conocimientos técnicos              |
| **RNF-07** | Privacidad         | El audio y video solo deben transmitirse dentro de la red local y no almacenarse sin consentimiento |
| **RNF-08** | Seguridad          | Solo los dispositivos y la aplicación autorizados deben poder acceder a los datos del sistema |
| **RNF-09** | Portabilidad       | La aplicación debe funcionar en teléfonos Android                                            |
| **RNF-10** | Costo              | El costo total de los componentes no debe superar el presupuesto definido en las restricciones |

---

## Aprobación

Con la firma de esta acta se da inicio formal al proyecto Babenitor y se aprueban el objetivo, el alcance, los stakeholders, los supuestos, las restricciones y los hitos aquí descritos.

| Nombre                          | Cargo / Rol                  | Fecha de aprobación | Firma |
| ------------------------------- | ---------------------------- | ------------------- | ----- |
| Alvaro Salazar Victoria                          | Profesor del curso           | xx/2026          |       |
| Dilan Mauricio Lemos López      | Integrante del equipo        | xx/xx/2026          |       |
| Diego Fernando Lenis Delgado    | Integrante del equipo        | xx/xx/2026          |       |
| Jaime Andrés Noreña Córdoba     | Integrante del equipo        | xx/xx/2026          |       |
| Juan José Restrepo Ávalo        | Integrante del equipo        | xx/xx/2026          |       |
| Daniel Hernández Ramírez        | Integrante del equipo        | xx/xx/2026          |       |


