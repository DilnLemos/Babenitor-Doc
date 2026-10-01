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

git commit -m "Doc: Acta de Constitución agregada." -m "Se creó el acta de consitución para el proyecto y se definieron los primeros puntos preliminares (Descripción, Problema, Justificación, Objetivo, Alcance)"
