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

**TODO**

git commit -m "Doc: Acta de Constitución agregada." -m "Se creó el acta de consitución para el proyecto y se definieron los primeros puntos preliminares (Descripción, Problema, Justificación, Objetivo, Alcance)"