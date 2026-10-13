# 📝 Acta de Constitución — Checklist del proyecto

## BLOQUE 1 — Definición básica del proyecto

- [x] **Nombre del proyecto**
  - **Necesitan:** decidir un nombre corto y representativo del monitor inteligente.

- [x] **Fecha del acta**
  - **Necesitan:** definir la fecha oficial en que elaboran/aprueban el acta.

- [x] **Equipo del proyecto**
  - **Necesitan:** nombres de los 5 integrantes y, asignar roles iniciales.


## BLOQUE 2 — Justificación

- [x] **Problema que quieren resolver**
  - **Necesitan:** explicar brevemente la dificultad de supervisar a un bebé cuando está solo en una habitación.

- [x] **Por qué vale la pena resolverlo**
  - **Necesitan:** conectar el problema con la utilidad del sistema: ubicación, sonidos, temperatura y alertas.

- [x] **Beneficio esperado**
  - **Necesitan:** explicar qué obtiene el cuidador con el prototipo.

## BLOQUE 3 — Objetivo

- [x] **Objetivo general**
  - **Necesitan:** una sola oración que diga qué van a desarrollar + qué hará + cómo se comprobará.

- [x] **Que sea medible**
  - **Necesitan:** que al final puedan responder sí/no a si el objetivo se cumplió.


## BLOQUE 4 — Alcance

### 4.1 Lo que SÍ incluye

- [x] **ESP32 #1**
  - **Necesitan:** cámara + micrófono.

- [x] **ESP32 #2**
  - **Necesitan:** sensores para temperatura corporal.

- [ ] **Detección de ubicación**
  - **Necesitan:** definir cómo determinarán dónde está el bebé dentro de la habitación.

- [ ] **Zonas seguras/riesgo**
  - **Necesitan:** establecer cómo se configuran y qué ocurre cuando el bebé sale de una zona permitida.

- [ ] **Detección de llanto**
  - **Necesitan:** definir cómo distinguir llanto de otros sonidos.

- [ ] **Detección de sonidos fuertes/anormales**
  - **Necesitan:** establecer qué consideran "sonido inusual".

- [ ] **Temperatura corporal**
  - **Necesitan:** definir sensor, ubicación de medición y qué rango consideran normal/anormal para el prototipo.

- [ ] **Comunicación entre los dos ESP32**
  - **Necesitan:** decidir tecnología/protocolo de comunicación.

- [ ] **Aplicación móvil**
  - **Necesitan:** definir qué información mostrará y cómo recibirá los datos.

- [ ] **Sistema de alertas**
  - **Necesitan:** definir qué eventos generan alertas y cómo se muestran/notifican.


### 4.2 Lo que NO incluye

- [x] **Diagnóstico médico**
  - **Necesitan:** dejar explícito que el sistema no diagnostica enfermedades.

- [x] **Intervención física sobre el bebé**
  - **Necesitan:** aclarar que únicamente monitorea y alerta.

- [ ] **Reemplazar la supervisión de un adulto**
  - **Necesitan:** establecerlo como limitación del prototipo.

- [ ] **Monitoreo fuera de la habitación configurada**
  - **Necesitan:** delimitar físicamente el entorno del proyecto.

- [x] **Certificación como dispositivo médico**
  - **Necesitan:** dejar claro que es un prototipo académico.

## BLOQUE 5 — Criterios de éxito

- [ ] **Éxito del cuidador/usuario**
  - **Necesitan:** definir qué tendría que funcionar para que el cuidador considere útil el sistema.

- [ ] **Éxito del equipo**
  - **Necesitan:** definir qué debe estar funcionando al finalizar el prototipo.

- [ ] **Éxito de los profesores/proyecto académico**
  - **Necesitan:** definir qué esperan demostrar técnicamente.

- [ ] **Criterios verificables**
  - **Necesitan:** convertirlos en condiciones comprobables, no frases generales.


## BLOQUE 6 — Stakeholders

- [ ] **Identificar stakeholders**
  - **Necesitan:** entre 6 y 10 personas/grupos relevantes.

- [ ] **Quién financia**
  - **Necesitan:** determinar si existe alguien que aporte dinero/recursos.

- [ ] **Quién utiliza**
  - **Necesitan:** determinar quién utilizará principalmente el sistema, por ejemplo, cuidador/padre/madre.

- [ ] **Quién opera/mantiene**
  - **Necesitan:** definir quién configura y mantiene el sistema.

- [ ] **Quién establece reglas**
  - **Necesitan:** identificar quién define las condiciones y decisiones importantes del proyecto.

- [ ] **Quién podría verse afectado**
  - **Necesitan:** considerar aspectos como privacidad, seguridad y falsas alarmas.


## BLOQUE 7 — Matriz poder/interés

- [ ] **Asignar poder**
  - **Necesitan:** determinar quién puede tomar decisiones o afectar el proyecto.

- [ ] **Asignar interés**
  - **Necesitan:** determinar quién está directamente interesado en el resultado.

- [ ] **Clasificar cada stakeholder**
  - **Necesitan:** ubicarlo en uno de los 4 cuadrantes.

- [ ] **Definir estrategia**
  - **Necesitan:**
    - Alto poder + alto interés → gestionar de cerca.
    - Alto poder + bajo interés → mantener satisfecho.
    - Bajo poder + alto interés → mantener informado.
    - Bajo poder + bajo interés → monitorear.


## BLOQUE 8 — Expectativas de stakeholders

Para cada stakeholder importante:

- [ ] **Expectativa**
  - **Necesitan:** definir qué espera obtener de este proyecto.

- [ ] **Criterio de éxito**
  - **Necesitan:** definir cómo sabremos que para esa persona el proyecto salió bien.

- [ ] **Forma de contacto**
  - **Necesitan:** WhatsApp, correo, reunión, etc.

- [ ] **Frecuencia**
  - **Necesitan:** semanal, quincenal, reuniones de proyecto, etc.


## BLOQUE 9 — Supuestos

- [ ] **Disponibilidad de ESP32**
  - **Necesitan:** confirmar que tendrán los dos dispositivos.

- [ ] **Disponibilidad de sensores**
  - **Necesitan:** saber qué sensores pueden conseguir.

- [ ] **Comunicación entre dispositivos**
  - **Necesitan:** asumir temporalmente que podrán establecer comunicación entre ambos ESP32.

- [ ] **Aplicación móvil**
  - **Necesitan:** asumir que podrán desarrollar una app capaz de recibir/mostrar la información.

- [ ] **Entorno controlado**
  - **Necesitan:** asumir que las pruebas se realizarán dentro de una habitación configurada para el prototipo.


## BLOQUE 10 — Restricciones

- [ ] **Tiempo**
  - **Necesitan:** fechas de inicio y final del semestre.

- [ ] **Presupuesto**
  - **Necesitan:** determinar cuánto dinero pueden gastar.

- [ ] **Hardware**
  - **Necesitan:** trabajar principalmente con los dos ESP32 establecidos.

- [ ] **Tamaño del equipo**
  - **Necesitan:** 5 integrantes.

- [ ] **Nivel del prototipo**
  - **Necesitan:** dejar claro que es un prototipo académico y no un producto comercial.

- [ ] **Tecnologías**
  - **Necesitan:** identificar qué tecnologías son obligatorias y cuáles pueden elegir libremente.


## BLOQUE 11 — Riesgos iniciales

- [ ] **Problemas de comunicación entre ESP32**
  - **Necesitan:** considerar que los dispositivos podrían perder conexión o presentar retrasos.

- [ ] **Detección incorrecta**
  - **Necesitan:** considerar falsos positivos/negativos en ubicación, llanto o sonidos.

- [ ] **Medición de temperatura**
  - **Necesitan:** comprobar que el sensor permita una medición adecuada para el propósito del prototipo.

- [ ] **Tiempo insuficiente**
  - **Necesitan:** considerar la integración de hardware + software + aplicación.


## BLOQUE 12 — Hitos principales

- [ ] **Inicio del proyecto**
  - **Necesitan:** fecha oficial.

- [ ] **Diseño del prototipo**
  - **Necesitan:** fecha estimada.

- [ ] **Integración de ESP32 + sensores**
  - **Necesitan:** fecha estimada.

- [ ] **Primera versión funcional**
  - **Necesitan:** fecha estimada.

- [ ] **Pruebas y presentación final**
  - **Necesitan:** fecha oficial de entrega.


## BLOQUE 13 — Aprobación

- [ ] **Nombre del responsable que aprueba**
  - **Necesitan:** profesor/director correspondiente.

- [ ] **Cargo/rol**
  - **Necesitan:** especificarlo.

- [ ] **Fecha de aprobación**
  - **Necesitan:** fecha de firma.

- [ ] **Firma**
  - **Necesitan:** firma de los responsables.