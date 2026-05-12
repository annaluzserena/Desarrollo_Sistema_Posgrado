<div align="center">

# 🎓 Sistema de Gestión Académica para Posgrado
### UTN FRLP · Desarrollo de Software · Metodología Ágil

[![UTN FRLP](https://img.shields.io/badge/UTN-FRLP-1a3a5c?style=for-the-badge&logo=graduation-cap&logoColor=white)](https://www.frlp.utn.edu.ar/)
[![Metodología](https://img.shields.io/badge/Metodología-Ágil%20%7C%20Scrum-0d7a5f?style=for-the-badge)](https://agilemanifesto.org/)
[![Estado](https://img.shields.io/badge/Estado-En%20Desarrollo-1e6b9e?style=for-the-badge)](.)

</div>

---

## 📋 Tabla de Contenidos

- [Integrantes del Equipo](#-integrantes-del-equipo)
- [Contexto del Dominio](#-contexto-del-dominio)
- [Actores del Sistema](#-actores-del-sistema)
- [Épicas](#-épicas)
- [Historias de Usuario](#-historias-de-usuario)
- [Criterios de Aceptación](#-criterios-de-aceptación)
- [Story Points](#-story-points)
- [Priorización MoSCoW](#-priorización-moscow)
- [Planificación de Sprints](#-planificación-de-sprints)
- [Product Backlog](#-product-backlog-completo)

---

<details>
<summary>## 👨‍💻 Integrantes del Equipo</summary>

| Nombre | GitHub |
|---|---|
| Facundo Fernandes 1 | [@Facu067](https://github.com/Facu067) |
| Aaron Gomez 2 | [@aarongomezgago](https://github.com/aarongomezgago) |
| Belén Marti 3 | [@martibelen99](https://github.com/martibelen99) |
| Ornela Nardulli  4 | [@nardulli03](https://github.com/nardulli03) |
| Solange Rodrigo 5 | [@SolangeRodrigo](https://github.com/SolangeRodrigo) |
| Anna Luz Serena 6 | [@annaluzserena](https://github.com/annaluzserena) |
</details>

<details>
<summary>## 🌐 Contexto del Dominio</summary>

> **Situación Actual (Problema)**
>
> La Facultad gestiona sus carreras de posgrado mediante correos electrónicos, planillas Excel y carpetas físicas. No existe un sistema centralizado que integre los procesos de inscripción, seguimiento académico y generación de reportes.

El sistema a desarrollar cubre cuatro módulos principales:

| Módulo | Descripción |
|---|---|
| 📥 **Inscripción** | Formularios digitales, carga de documentos y conformación del legajo del aspirante |
| 🎓 **Académico** | Perfil del estudiante, seminarios, asistencia y calificaciones |
| 👨‍🏫 **Docentes** | Planilla de carga online, registro de asistencia y notas por seminario |
| 📊 **Estadísticas** | Módulo de reportes por cohorte y situación de carreras |

---
</details>

<details>
<summary>## 👥 Actores del Sistema</summary>

### 🙋 Aspirante
Es el usuario externo interesado en una carrera. Su responsabilidad es acceder al sistema mediante un enlace para completar el formulario de inscripción web (datos personales, motivaciones, etc.) y cargar la documentación obligatoria en PDF (DNI, títulos, partida de nacimiento y formularios de beca si corresponde).

### 📚 Estudiante
Es el actor central del seguimiento académico una vez aceptada su inscripción. Interactúa indirectamente con el sistema al ser el sujeto del legajo digital, del indicador visual de avance ("semáforo") y de las alertas por vencimiento de seminarios.

### 👩‍🏫 Docente
Es el encargado de alimentar el sistema con los datos de cursada. Su función es ingresar a través de un enlace específico a una planilla de carga online para registrar la asistencia por fecha y las calificaciones finales de sus seminarios. Además, es el destinatario de los recordatorios automáticos en caso de incumplimiento de plazos.

### 🏛️ Equipo de Conducción y Autoridades del Área
Son los administradores principales del sistema. Tienen permisos para visualizar y revisar los datos de los aspirantes, realizar búsquedas individuales, listar inscriptos por cohorte y abrir o cerrar los períodos de inscripción. También son los únicos autorizados para acceder a los perfiles académicos y descargar informes de avance, así como acceder a estadísticas por cohorte y a nivel global de la carrera.

### 📜 Comisión de Posgrado Regional (CPR)
Actor con responsabilidad técnica crítica y diferenciada. Es el único rol encargado de cargar los datos específicos de las tesis (título, director, codirector, fecha de aprobación y número de resolución) para las carreras de maestría y doctorado.
</details>
---

<details>
<summary>## 🗂️ Épicas</summary>

### `EP-01` · Gestión de Inscripciones
**Alcance:** Cubre el proceso inicial desde que el aspirante accede al enlace web hasta que se conforma su legajo digital.

**Funcionalidades clave:** Formulario de preinscripción, carga de documentos obligatorios en PDF (DNI, títulos), selección de porcentajes de beca y el indicador visual de "estado de carga" del legajo.

---

### `EP-02` · Legajo y Perfil Académico
**Alcance:** Incluye el seguimiento de la trayectoria del estudiante una vez admitido.

**Funcionalidades clave:** Indicador visual de avance académico ("semáforo"), alertas de vencimiento de seminarios según la carrera, y el registro detallado de tutorías y trabajos finales (TFI para especializaciones o Tesis para maestrías/doctorados).

---

### `EP-03` · Gestión Docente
**Alcance:** Centraliza la interacción de los profesores con el sistema para alimentar los datos de cursada.

**Funcionalidades clave:** Acceso vía enlace a planillas de carga online, registro de asistencia por fecha, carga de calificaciones finales y envío de recordatorios automáticos por incumplimiento de plazos.

---

### `EP-04` · Estadísticas y Reportes
**Alcance:** Provee las herramientas de análisis de datos para el equipo de conducción.

**Funcionalidades clave:** Generación de balances globales y por cohorte sobre inscriptos, estado de acreditación de seminarios, estado de ralentización de carrera, situación de los trabajos finales (TFI o tesis), niveles de desgranamiento (deserción) y cantidad de graduados.

---

### `EP-05` · Administración del Sistema
**Alcance:** Agrupa las tareas de control administrativo y configuración.

**Funcionalidades clave:** Apertura y cierre de los períodos de inscripción a las carreras, búsqueda individual de estudiantes y gestión de accesos restringidos para autoridades y CPR.
</details>

---

<details>
<summary>## 📖 Historias de Usuario</summary>

### EP-01 · Gestión de Inscripciones

| ID | Historia de Usuario |
|---|---|
| **US-01** | Como aspirante, quiero acceder a un formulario web, para inscribirme sin enviar correos manuales. |
| **US-02** | Como aspirante, quiero adjuntar mis documentos en PDF (DNI, títulos), para completar mi legajo digital de forma remota. |
| **US-06** | Como aspirante, quiero seleccionar un porcentaje de beca (30% o 100%) y adjuntar el formulario PDF, para formalizar mi solicitud de ayuda económica. |
| **US-07** | Como aspirante, quiero ingresar mis motivaciones y forma de conocer la oferta, para que el equipo de conducción evalúe mi perfil. |
| **US-08** | Como equipo de conducción, quiero generar un enlace de inscripción único, para enviarlo por correo a los interesados y centralizar la carga de datos. |

### EP-02 · Legajo y Perfil Académico

| ID | Historia de Usuario |
|---|---|
| **US-03** | Como conducción, quiero ver el indicador visual ("semáforo") del legajo, para saber de forma rápida si el alumno tiene la documentación completa. |
| **US-04** | Como conducción, quiero registrar la asistencia y notas finales del estudiante, para mantener actualizado su perfil académico. |
| **US-09** | Como equipo de conducción, quiero recibir alertas de plazos de vencimiento de seminarios según el tipo de carrera, para notificar a los alumnos en riesgo de retraso. |
| **US-10** | Como integrante de la CPR, quiero cargar los datos de la tesis (director, resolución, fecha de aprobación), para oficializar el seguimiento de maestrías y doctorados. |
| **US-11** | Como equipo de conducción, quiero registrar el seguimiento del Trabajo Final Integrador (TFI), para controlar el avance de los alumnos de especializaciones. |
| **US-12** | Como equipo de conducción, quiero descargar el perfil académico de un estudiante o cohorte, para tener un reporte físico del avance. |

### EP-03 · Gestión Docente

| ID | Historia de Usuario |
|---|---|
| **US-05** | Como docente, quiero acceder a mi planilla vía enlace, para cargar asistencia y notas sin necesidad de usuario y contraseña. |
| **US-13** | Como docente, quiero registrar la asistencia por fecha de cursada, para para saber en todo momento quiénes están en riesgo de perder la regularidad y poder actuar antes de que sea tarde. |
| **US-14** | Como docente, quiero recibir recordatorios automáticos por correo, para cumplir con la carga de notas en los plazos estipulados. |
| **US-15** | Como docente, quiero descargar la planilla de mis alumnos en formato analógico, para utilizarla durante la cursada presencial. |

### EP-04 · Estadísticas y Reportes

| ID | Historia de Usuario |
|---|---|
| **US-16** | Como equipo de conducción, quiero generar un reporte de niveles de desgranamiento por cohorte, para identificar deserción temprana. |
| **US-17** | Como equipo de conducción, quiero ver el estado de situación de los trabajos finales (TFI o tesis) por cohorte y en general, para saber en qué etapa se encuentra cada estudiante y detectar cuellos de botella. |
| **US-20** | Como equipo de conducción, quiero ver el estado de acreditación de seminarios por cohorte, para identificar si hay grupos de estudiantes con dificultades en esta instancia. |
| **US-21** | Como equipo de conducción, quiero conocer la cantidad total de inscripciones por cohorte y a nivel general, para entender la evolución del volumen de estudiantes a lo largo del tiempo. |
| **US-22** | Como equipo de conducción, quiero conocer la cantidad de graduados por cohorte y el total acumulado, para evaluar la tasa de egreso y comparar el rendimiento entre promociones. |
| **US-23** | Como equipo de conducción, quiero conocer qué estudiantes o cohortes presentan ralentización en el avance de la carrera, para intervenir a tiempo con estrategias de acompañamiento. |

### EP-05 · Administración del Sistema

| ID | Historia de Usuario |
|---|---|
| **US-18** | Como autoridad del área, quiero abrir o cerrar el período de inscripción, para controlar cuándo los aspirantes pueden acceder al formulario web. |
| **US-19** | Como equipo de conducción, quiero realizar búsquedas individuales por estudiante, para consultar el avance de estudiantes específicos de forma ágil. |
</details>

---

<details>
<summary>## ✅ Criterios de Aceptación</summary>

> Los criterios de aceptación son condiciones específicas y verificables que una historia de usuario **DEBE** satisfacer para considerarse completa. Se expresan en formato **Dado / Cuando / Entonces** (Gherkin).

### EP-01 · Gestión de Inscripciones

<details>
<summary><strong>US-01 · Formulario web de inscripción</strong></summary>

**Criterio 1:**
- **Dado** que el aspirante ingresó al enlace de inscripción,
- **Cuando** completa todos los campos obligatorios (nombre, DNI, carrera, etc.),
- **Entonces** el sistema guarda los datos en la base de datos y muestra un mensaje de confirmación.

**Criterio 2:**
- **Dado** que un campo obligatorio quedó vacío,
- **Cuando** el usuario intenta enviar el formulario,
- **Entonces** el sistema resalta el error y bloquea el envío.
</details>

<details>
<summary><strong>US-02 · Adjuntar documentos en PDF</strong></summary>

**Criterio 1:**
- **Dado** que el aspirante selecciona sus archivos (DNI, títulos),
- **Cuando** los sube al sistema,
- **Entonces** el sistema los valida y los almacena vinculados a su legajo.

**Criterio 2:**
- **Dado** que el usuario intenta subir un archivo que no es PDF,
- **Cuando** intenta cargarlo,
- **Entonces** el sistema rechaza el archivo informando que solo se aceptan formatos PDF.
</details>

<details>
<summary><strong>US-06 · Solicitud de becas</strong></summary>

**Criterio 1:**
- **Dado** que el aspirante selecciona un porcentaje de beca (30% o 100%),
- **Cuando** confirma la opción,
- **Entonces** el sistema habilita un campo obligatorio para adjuntar el formulario de beca en PDF.

**Criterio 2:**
- **Dado** que no se adjuntó el PDF de beca,
- **Cuando** el usuario intenta finalizar la inscripción,
- **Entonces** el sistema impide el envío por documentación incompleta.
</details>

<details>
<summary><strong>US-07 · Motivaciones y forma de conocer la oferta</strong></summary>

**Criterio 1:**
- **Dado** que el aspirante está en el formulario,
- **Cuando** ingresa sus motivaciones en el campo de texto,
- **Entonces** el sistema permite un máximo de 500 caracteres para la descripción.

**Criterio 2:**
- **Dado** que el aspirante selecciona cómo conoció la oferta,
- **Cuando** elige la opción "Otros",
- **Entonces** el sistema despliega un campo de texto para especificar la fuente.
</details>

<details>
<summary><strong>US-08 · Generar enlace único de inscripción</strong></summary>

**Criterio 1:**
- **Dado** que la conducción necesita abrir inscripciones,
- **Cuando** presiona el botón "Generar enlace",
- **Entonces** el sistema crea una URL única vinculada a la carrera y cohorte actual.

**Criterio 2:**
- **Dado** que el enlace fue generado,
- **Cuando** el sistema lo muestra,
- **Entonces** ofrece la opción de "Copiar al portapapeles" para facilitar el envío por correo.
</details>

### EP-02 · Legajo y Perfil Académico

<details>
<summary><strong>US-03 · Indicador visual ("Semáforo")</strong></summary>

**Criterio 1:**
- **Dado** que el equipo de conducción revisa a un aspirante con documentos faltantes,
- **Cuando** accede al panel,
- **Entonces** ve un indicador visual en color rojo.

**Criterio 2:**
- **Dado** que el estudiante tiene el legajo completo,
- **Cuando** se consulta su perfil,
- **Entonces** el indicador cambia automáticamente a color verde.
</details>

<details>
<summary><strong>US-04 · Registro de asistencia y notas (Manual)</strong></summary>

**Criterio 1:**
- **Dado** que se cargan notas finales de un acta de examen,
- **Cuando** se confirman los datos,
- **Entonces** el sistema actualiza inmediatamente el promedio y estado del estudiante.

**Criterio 2:**
- **Dado** que se registra la asistencia a un seminario,
- **Cuando** el porcentaje es inferior al mínimo requerido,
- **Entonces** el sistema marca al alumno como "Libre" automáticamente.
</details>

<details>
<summary><strong>US-09 · Alertas de plazos de vencimiento</strong></summary>

**Criterio 1:**
- **Dado** que se aproxima el vencimiento de un seminario,
- **Cuando** el sistema detecta la fecha límite según el tipo de carrera,
- **Entonces** genera una alerta visual en el perfil del estudiante.

**Criterio 2:**
- **Dado** que la alerta fue emitida,
- **Cuando** el estudiante regulariza su situación,
- **Entonces** la alerta desaparece del tablero de control.
</details>

<details>
<summary><strong>US-10 · Carga de datos de Tesis (CPR)</strong></summary>

**Criterio 1:**
- **Dado** que un usuario con rol CPR ingresa datos de tesis (título, director),
- **Cuando** guarda los cambios,
- **Entonces** el perfil del estudiante de maestría/doctorado se actualiza con la resolución oficial.

**Criterio 2:**
- **Dado** que un usuario de conducción general intenta editar datos de tesis,
- **Cuando** intenta guardar,
- **Entonces** el sistema bloquea la acción por falta de permisos específicos del CPR.
</details>

<details>
<summary><strong>US-11 · Seguimiento del TFI (Especialización)</strong></summary>

**Criterio 1:**
- **Dado** que el alumno cursa una Especialización,
- **Cuando** se accede a su perfil,
- **Entonces** el sistema muestra exclusivamente el módulo de seguimiento de TFI.

**Criterio 2:**
- **Dado** que el tutor registra un avance en el TFI,
- **Cuando** guarda el comentario,
- **Entonces** el sistema registra la fecha y el usuario que realizó el seguimiento.
</details>

<details>
<summary><strong>US-12 · Descarga de perfil académico</strong></summary>

**Criterio 1:**
- **Dado** que la conducción necesita un reporte físico,
- **Cuando** selecciona a un estudiante,
- **Entonces** el sistema genera un archivo descargable con todo su historial académico.

**Criterio 2:**
- **Dado** que se requiere información de un grupo,
- **Cuando** se selecciona una cohorte completa,
- **Entonces** el sistema permite la descarga masiva de los perfiles en un archivo comprimido.
</details>

### EP-03 · Gestión Docente

<details>
<summary><strong>US-05 · Acceso docente vía enlace</strong></summary>

**Criterio 1:**
- **Dado** que el docente recibe el link en su correo,
- **Cuando** lo abre,
- **Entonces** accede directamente a su planilla activa sin requerir login manual.

**Criterio 2:**
- **Dado** que el enlace es específico para un seminario,
- **Cuando** el docente lo utiliza,
- **Entonces** solo puede ver y editar a los alumnos inscriptos en esa comisión particular.
</details>

<details>
<summary><strong>US-13 · Registro de asistencia por fecha</strong></summary>

**Criterio 1:**
- **Dado** que el docente carga la asistencia por fecha de cursada,
- **Cuando** confirma la carga,
- **Entonces** el sistema recalcula el porcentaje acumulado de cada alumno automáticamente.

**Criterio 2:**
- **Dado** que un alumno tiene asistencia perfecta,
- **Cuando** se cierra el seminario,
- **Entonces** el sistema lo habilita para la carga de la calificación final.
</details>

<details>
<summary><strong>US-14 · Recordatorios automáticos</strong></summary>

**Criterio 1:**
- **Dado** que venció el plazo de carga de notas,
- **Cuando** el sistema detecta la planilla vacía,
- **Entonces** envía un correo automático de recordatorio al docente.

**Criterio 2:**
- **Dado** que el docente completó la carga,
- **Cuando** el sistema realiza el barrido de control,
- **Entonces** no debe disparar ningún correo de advertencia.
</details>

<details>
<summary><strong>US-15 · Descarga de planilla analógica</strong></summary>

**Criterio 1:**
- **Dado** que el docente dará clases presenciales,
- **Cuando** solicita la descarga de la planilla,
- **Entonces** el sistema genera un formato imprimible con los datos básicos de los alumnos.

**Criterio 2:**
- **Dado** que la planilla se descarga,
- **Cuando** se visualiza el archivo,
- **Entonces** debe incluir nombre, apellido, DNI y correo de cada estudiante de la cohorte.
</details>

### EP-04 · Estadísticas y Reportes

<details>
<summary><strong>US-16 · Reporte de desgranamiento</strong></summary>

**Criterio 1:**
- **Dado** que el equipo de conducción selecciona una cohorte,
- **Cuando** genera el reporte,
- **Entonces** el sistema muestra el porcentaje de alumnos que abandonaron la cursada respecto al total inicial.

**Criterio 2:**
- **Dado** que se visualizan los datos,
- **Cuando** se detecta un pico de deserción,
- **Entonces** el sistema permite filtrar los motivos registrados en las tutorías.
</details>

<details>
<summary><strong>US-17 · Estado de trabajos finales</strong></summary>

**Criterio 1:**
- **Dado** que accede al panel de estadísticas y selecciona una cohorte,
- **Cuando** consulta la situación de trabajos finales,
- **Entonces** el sistema muestra la cantidad de estudiantes en cada etapa (sin iniciar, en curso, presentado, aprobado).

**Criterio 2:**
- **Dado** que accede al panel de estadísticas,
- **Cuando** consulta la vista general de todas las cohortes,
- **Entonces** el sistema muestra una comparación entre cohortes que permite identificar en qué etapa se concentra la mayor cantidad de estudiantes sin avanzar.
</details>

<details>
<summary><strong>US-20 · Acreditación de seminarios</strong></summary>

**Criterio 1:**
- **Dado** que accede al panel de estadísticas y selecciona una cohorte,
- **Cuando** consulta el estado de acreditación de seminarios,
- **Entonces** el sistema muestra para cada seminario la cantidad de estudiantes que lo acreditaron, que lo tienen pendiente y que no lo iniciaron.

**Criterio 2:**
- **Dado** que accede al panel de estadísticas,
- **Cuando** consulta el estado de acreditación en general,
- **Entonces** el sistema muestra una vista comparativa entre cohortes.
</details>

<details>
<summary><strong>US-21 · Inscripciones por cohorte</strong></summary>

**Criterio 1:**
- **Dado** que accede al panel de estadísticas y selecciona una cohorte,
- **Cuando** consulta la cantidad de inscripciones,
- **Entonces** el sistema muestra el total de estudiantes inscriptos en esa cohorte.

**Criterio 2:**
- **Dado** que accede al panel de estadísticas,
- **Cuando** consulta la vista general de inscripciones,
- **Entonces** el sistema muestra el total de inscriptos por cada cohorte disponible.
</details>

<details>
<summary><strong>US-22 · Graduados por cohorte</strong></summary>

**Criterio 1:**
- **Dado** que accede al panel de estadísticas y selecciona una cohorte,
- **Cuando** consulta el indicador de graduados,
- **Entonces** el sistema muestra la cantidad de egresados de esa cohorte y el porcentaje que representan sobre el total de inscriptos.

**Criterio 2:**
- **Dado** que accede al panel de estadísticas,
- **Cuando** consulta la vista general de graduados,
- **Entonces** el sistema muestra el total acumulado y permite comparar las tasas de egreso entre cohortes.
</details>

<details>
<summary><strong>US-23 · Ralentización de carrera</strong></summary>

**Criterio 1:**
- **Dado** que accede al panel de estadísticas y selecciona una cohorte,
- **Cuando** consulta el indicador de ralentización,
- **Entonces** el sistema lista los estudiantes que superaron el tiempo esperado de cursada sin haber completado la carrera.

**Criterio 2:**
- **Dado** que accede al panel de estadísticas,
- **Cuando** consulta la vista general entre todas las cohortes,
- **Entonces** el sistema muestra el porcentaje de estudiantes en situación de ralentización por cohorte.
</details>

### EP-05 · Administración del Sistema

<details>
<summary><strong>US-18 · Abrir o cerrar período de inscripción</strong></summary>

**Criterio 1:**
- **Dado** que se cierra el período,
- **Cuando** la autoridad presiona "Cerrar",
- **Entonces** el enlace de inscripción deja de estar operativo y muestra un mensaje de "Inscripciones cerradas".

**Criterio 2:**
- **Dado** que se abre una nueva cohorte,
- **Cuando** se configura la fecha de apertura,
- **Entonces** el sistema habilita automáticamente el formulario web en el día estipulado.
</details>

<details>
<summary><strong>US-19 · Búsquedas individuales</strong></summary>

**Criterio 1:**
- **Dado** que el administrador ingresa un DNI en el buscador,
- **Cuando** presiona buscar,
- **Entonces** el sistema devuelve el legajo del estudiante independientemente de la cohorte a la que pertenezca.

**Criterio 2:**
- **Dado** que se busca por apellido,
- **Cuando** hay coincidencias múltiples,
- **Entonces** el sistema muestra una lista de resultados con nombre, carrera y cohorte para diferenciar a los alumnos.
</details>
</details>

---

<details>
<summary>## 🎯 Story Points</summary>

La escala utilizada sigue la secuencia de **Fibonacci** para estimar el esfuerzo relativo de cada historia:

| SP | Nivel | Descripción |
|:---:|---|---|
| **1** | Muy simple | Pocas horas de trabajo |
| **2** | Simple | Aproximadamente medio día |
| **3** | Moderada | Cerca de 1 día de trabajo |
| **5** | Compleja | Requiere varios días |
| **8** | Muy compleja | Aproximadamente 1 semana |
| **13** | Épica | Requiere ser subdividida |

| ID | Historia de Usuario | SP | Justificación |
|---|---|:---:|---|
| US-01 | Formulario web de inscripción | **5** | Requiere validaciones y persistencia de múltiples campos |
| US-02 | Adjuntar documentos en PDF | **3** | Implica gestión de archivos y almacenamiento vinculado al legajo |
| US-03 | Indicador visual ("Semáforo") | **3** | Lógica visual basada en el estado de los datos |
| US-04 | Registro manual de asistencia/notas | **5** | Debe impactar en el promedio y estado académico |
| US-05 | Acceso docente vía enlace | **3** | Seguridad basada en tokens sin login tradicional |
| US-06 | Selección de becas y adjunto | **5** | Incluye lógica condicional para habilitar campos obligatorios |
| US-07 | Ingreso de motivaciones y fuente | **2** | Campos de texto adicionales en el formulario |
| US-08 | Generar enlace único de inscripción | **3** | Lógica de backend para URLs únicas |
| US-09 | Alertas de plazos de vencimiento | **5** | Requiere cálculos de fechas por tipo de carrera y procesos de fondo |
| US-10 | Carga de datos de Tesis (CPR) | **3** | Formulario específico con permisos restringidos |
| US-11 | Seguimiento del TFI | **3** | Módulo de registro de tutorías y avances |
| US-12 | Descarga de perfil académico | **5** | Generación de documentos PDF con datos dinámicos de la DB |
| US-13 | Registro de asistencia por fecha | **5** | Cálculo automático de porcentajes en tiempo real |
| US-14 | Recordatorios automáticos | **5** | Integración con servicio de correo y barrido de cumplimiento |
| US-15 | Descarga de planilla analógica | **3** | Generación de formato imprimible de la cohorte |
| US-16 | Reporte de desgranamiento | **8** | Requiere consultas analíticas cruzadas entre cohortes |
| US-17 | Estado de trabajos finales | **5** | Reportes estadísticos sobre estados de tesis/TFI |
| US-18 | Abrir o cerrar período de inscripción | **2** | Cambio de estado lógico que habilita/deshabilita la URL |
| US-19 | Búsquedas individuales | **3** | Implementación de filtros de búsqueda por DNI o apellido |
| US-20 | Acreditación de seminarios | **5** | Requiere cruzar estudiantes, cohortes y múltiples seminarios |
| US-21 | Inscripciones por cohorte | **2** | Contar registros agrupados por cohorte |
| US-22 | Graduados por cohorte | **3** | Requiere cruzar dos conjuntos de datos |
| US-23 | Ralentización de carrera | **5** | Definir y calcular el tiempo esperado vs. avance real por cohorte |
<details>

---

<details>
<summary>## 🏷️ Priorización MoSCoW</summary>

| Etiqueta | Significado |
|---|---|
| 🔴 **M — Must Have** | Funcionalidad imprescindible para el lanzamiento. Sin ella el sistema no tiene razón de ser. |
| 🟡 **S — Should Have** | Funcionalidad importante pero no vital. Debería incluirse si es posible. |
| 🟢 **C — Could Have** | Funcionalidad deseable que se incluirá solo si queda tiempo y presupuesto. |
| ⚪ **W — Won't Have** | No se incluirá en esta versión o fase inicial. |

| ID | Historia de Usuario | Prioridad | Justificación |
|---|---|:---:|---|
| US-01 | Formulario web de inscripción | 🔴 **M** | Base del sistema para eliminar el proceso manual por correo |
| US-08 | Generar enlace único de inscripción | 🔴 **M** | Imprescindible para iniciar el flujo de captación de datos |
| US-02 | Adjuntar documentos en PDF | 🔴 **M** | Crítico para conformar el legajo digital obligatorio |
| US-03 | Indicador visual ("Semáforo") | 🔴 **M** | Requerimiento explícito para conocer el estado de carga del legajo |
| US-04 | Registro manual de asistencia/notas | 🔴 **M** | Funcionalidad central para el seguimiento académico básico |
| US-05 | Acceso docente vía enlace | 🔴 **M** | Canal esencial para que el docente alimente el sistema |
| US-13 | Registro de asistencia por fecha | 🔴 **M** | Necesario para que el sistema calcule el porcentaje mínimo |
| US-18 | Abrir o cerrar período de inscripción | 🔴 **M** | Control administrativo básico para la operación del área |
| US-21 | Inscripciones por cohorte | 🔴 **M** | Dato más básico y estructural, punto de partida de cualquier análisis |
| US-22 | Graduados por cohorte | 🔴 **M** | La tasa de egreso es el indicador de resultado más importante de una carrera |
| US-06 | Selección de becas y adjunto | 🟡 **S** | Importante para la gestión administrativa, pero no detiene la cursada |
| US-09 | Alertas de plazos de vencimiento | 🟡 **S** | Importante para el cumplimiento normativo, pero secundario al registro |
| US-10 | Carga de datos de Tesis (CPR) | 🟡 **S** | Vital para maestrías/doctorados, pero ocurre al final del trayecto |
| US-14 | Recordatorios automáticos | 🟡 **S** | Asegura la salud de los datos, aunque inicialmente podría ser manual |
| US-17 | Estado de trabajos finales | 🟡 **S** | Indicador crítico pero más operativo que estratégico |
| US-19 | Búsquedas individuales | 🟡 **S** | Fundamental para la agilidad administrativa diaria |
| US-20 | Acreditación de seminarios | 🟡 **S** | Importante para el seguimiento académico |
| US-07 | Ingreso de motivaciones y fuente | 🟢 **C** | Datos cualitativos que no afectan la gestión académica central |
| US-11 | Seguimiento del TFI | 🟢 **C** | Deseable para formalizar tutorías, similar a la tesis |
| US-12 | Descarga de perfil académico | 🟢 **C** | Útil para reportes físicos, pero ya se visualiza en el panel |
| US-15 | Descarga de planilla analógica | 🟢 **C** | Soporte para clases presenciales, deseable para conveniencia docente |
| US-16 | Reporte de desgranamiento | 🟢 **C** | Estadística compleja que puede esperar a una segunda etapa |
| US-23 | Ralentización de carrera | 🟢 **C** | Indicador más complejo de calcular, requiere definir criterios de negocio |
</details>

---

<details>
<summary>## 🚀 Planificación de Sprints</summary>

> **Configuración del equipo:** 6 integrantes · Velocidad estimada: ~18 SP por sprint · Duración: 2 semanas por sprint

### Resumen General

| Sprint | Nombre | Semanas | Story Points | Foco |
|:---:|---|:---:|:---:|---|
| **Sprint 1** | Núcleo de Inscripción | 1–2 | **18 SP** | Must Have |
| **Sprint 2** | Seguimiento Académico | 3–4 | **18 SP** | Must Have |
| **Sprint 3** | Gestión Administrativa y Becas | 5–6 | **18 SP** | Should Have |
| **Sprint 4** | Analítica y Automatizaciones | 7–8 | **18 SP** | Should / Could |
| **Sprint 5** | Reportes, Exportaciones y Datos Cualitativos | 9–10 | **19 SP** | Could Have |
| **TOTAL** | **23 historias de usuario** | **10 semanas** | **91 SP** | |

---

### 🏃 Sprint 1 · Núcleo de Inscripción
> **Semanas 1–2 · 18 SP**
>
> *Objetivo: El alumno puede inscribirse mediante un enlace único y subir sus documentos.*

| ID | Historia de Usuario | Prioridad | SP |
|---|---|:---:|:---:|
| US-01 | Formulario web de inscripción | 🔴 M | 5 |
| US-08 | Generar enlace único de inscripción | 🔴 M | 3 |
| US-18 | Abrir o cerrar período de inscripción | 🔴 M | 2 |
| US-02 | Adjuntar documentos en PDF | 🔴 M | 3 |
| US-03 | Indicador visual "Semáforo" | 🔴 M | 3 |
| US-21 | Inscripciones por cohorte | 🔴 M | 2 |
| **Total** | | | **18 SP** |

---

### 🏃 Sprint 2 · Seguimiento Académico
> **Semanas 3–4 · 18 SP**
>
> *Objetivo: El docente puede ingresar asistencia y notas desde su enlace; el sistema calcula el estado del alumno.*

| ID | Historia de Usuario | Prioridad | SP |
|---|---|:---:|:---:|
| US-05 | Acceso docente vía enlace (sin login) | 🔴 M | 3 |
| US-04 | Registro manual de asistencia/notas | 🔴 M | 5 |
| US-13 | Registro de asistencia por fecha | 🔴 M | 5 |
| US-22 | Graduados por cohorte | 🔴 M | 3 |
| US-19 | Búsquedas individuales | 🟡 S | 3 |
| **Total** | | | **19 SP** |

---

### 🏃 Sprint 3 · Gestión Administrativa y Becas
> **Semanas 5–6 · 18 SP**
>
> *Objetivo: El área administrativa completa la gestión de becas, plazos y carga de trabajos finales.*

| ID | Historia de Usuario | Prioridad | SP |
|---|---|:---:|:---:|
| US-06 | Selección de becas y adjunto de solicitud | 🟡 S | 5 |
| US-09 | Alertas de plazos de vencimiento | 🟡 S | 5 |
| US-10 | Carga de datos de Tesis (CPR) | 🟡 S | 3 |
| US-17 | Estado de trabajos finales | 🟡 S | 5 |
| **Total** | | | **18 SP** |

---

### 🏃 Sprint 4 · Analítica y Automatizaciones
> **Semanas 7–8 · 18 SP**
>
> *Objetivo: El sistema envía recordatorios automáticos y permite análisis de avance y acreditación de seminarios.*

| ID | Historia de Usuario | Prioridad | SP |
|---|---|:---:|:---:|
| US-14 | Recordatorios automáticos de carga | 🟡 S | 5 |
| US-20 | Acreditación de seminarios | 🟡 S | 5 |
| US-23 | Ralentización de carrera | 🟢 C | 5 |
| US-11 | Seguimiento del TFI (Especialización) | 🟢 C | 3 |
| **Total** | | | **18 SP** |

---

### 🏃 Sprint 5 · Reportes, Exportaciones y Datos Cualitativos
> **Semanas 9–10 · 19 SP**
>
> *Objetivo: Completar reportes analíticos complejos, exportaciones y datos cualitativos de baja prioridad.*

| ID | Historia de Usuario | Prioridad | SP |
|---|---|:---:|:---:|
| US-16 | Reporte de desgranamiento por cohorte | 🟢 C | 8 |
| US-12 | Descarga de perfil académico (PDF) | 🟢 C | 5 |
| US-15 | Descarga de planilla analógica para docentes | 🟢 C | 3 |
| US-07 | Ingreso de motivaciones y fuente | 🟢 C | 2 |
| **Total** | | | **18 SP** |
</details>

---

<details>
<summary>## 📊 Product Backlog Completo</summary>

| ID | Épica | Historia de Usuario | Criterios de Aceptación (resumen) | SP | Prior. | Sprint |
|:---:|:---:|---|---|:---:|:---:|:---:|
| US-01 | EP-01 | Como aspirante, quiero acceder a un formulario web, para inscribirme sin enviar correos manuales. | Dado que ingresa al enlace, cuando completa los campos, entonces los datos se guardan. / Dado que hay campos vacíos, cuando intenta enviar, entonces el sistema bloquea el envío. | 5 | 🔴 M | 1 |
| US-08 | EP-01 | Como equipo de conducción, quiero generar un enlace de inscripción único, para centralizar la carga de datos. | Dado que presiona "Generar enlace", cuando lo crea, entonces el sistema devuelve una URL única. / Dado que el enlace fue creado, cuando se muestra, entonces ofrece "Copiar al portapapeles". | 3 | 🔴 M | 1 |
| US-18 | EP-05 | Como autoridad del área, quiero abrir o cerrar el período de inscripción, para controlar el acceso al formulario. | Dado que cierra el período, cuando presiona "Cerrar", entonces el enlace queda inoperativo. / Dado que abre una cohorte, cuando configura la fecha, entonces el sistema habilita el formulario automáticamente. | 2 | 🔴 M | 1 |
| US-02 | EP-01 | Como aspirante, quiero adjuntar mis documentos en PDF, para completar mi legajo digital de forma remota. | Dado que selecciona archivos, cuando los sube, entonces el sistema los valida y almacena. / Dado que sube un archivo que no es PDF, cuando intenta cargarlo, entonces el sistema rechaza el archivo. | 3 | 🔴 M | 1 |
| US-03 | EP-01 | Como conducción, quiero ver el indicador visual ("semáforo") del legajo, para saber si la documentación está completa. | Dado que hay documentos faltantes, cuando accede al panel, entonces el indicador es rojo. / Dado que el legajo está completo, cuando consulta el perfil, entonces el indicador es verde. | 3 | 🔴 M | 1 |
| US-21 | EP-04 | Como equipo de conducción, quiero conocer la cantidad de inscripciones por cohorte, para entender la evolución del volumen de estudiantes. | Dado que selecciona una cohorte, cuando consulta, entonces el sistema muestra el total de inscriptos. / Dado que consulta la vista general, cuando la carga, entonces muestra el total por cada cohorte. | 2 | 🔴 M | 1 |
| US-05 | EP-03 | Como docente, quiero acceder a mi planilla vía enlace, para cargar asistencia y notas sin usuario y contraseña. | Dado que recibe el link, cuando lo abre, entonces accede a su planilla activa sin login. / Dado que el enlace es de un seminario específico, cuando lo usa, entonces solo ve a los alumnos de esa comisión. | 3 | 🔴 M | 2 |
| US-04 | EP-02 | Como conducción, quiero registrar asistencia y notas finales del estudiante, para mantener actualizado su perfil académico. | Dado que se cargan notas, cuando se confirman, entonces el sistema actualiza el promedio. / Dado que la asistencia es insuficiente, cuando se registra, entonces el alumno queda marcado como "Libre". | 5 | 🔴 M | 2 |
| US-13 | EP-03 | Como docente, quiero registrar la asistencia por fecha, para que el sistema calcule si el alumno cumple el mínimo requerido. | Dado que se carga la asistencia, cuando se confirma, entonces el sistema recalcula el porcentaje acumulado. / Dado que un alumno tiene asistencia perfecta, cuando se cierra el seminario, entonces se habilita su calificación final. | 5 | 🔴 M | 2 |
| US-22 | EP-04 | Como equipo de conducción, quiero conocer la cantidad de graduados por cohorte, para evaluar la tasa de egreso. | Dado que selecciona una cohorte, cuando consulta, entonces el sistema muestra egresados y porcentaje sobre inscriptos. / Dado que consulta la vista general, cuando la carga, entonces muestra el total acumulado y permite comparar cohortes. | 3 | 🔴 M | 2 |
| US-19 | EP-05 | Como equipo de conducción, quiero realizar búsquedas individuales por estudiante, para consultar avances de forma ágil. | Dado que ingresa un DNI, cuando presiona buscar, entonces devuelve el legajo sin importar la cohorte. / Dado que busca por apellido con múltiples coincidencias, cuando carga los resultados, entonces muestra nombre, carrera y cohorte. | 3 | 🟡 S | 2 |
| US-06 | EP-01 | Como aspirante, quiero seleccionar un porcentaje de beca y adjuntar el formulario PDF, para formalizar mi solicitud de ayuda económica. | Dado que selecciona un porcentaje de beca, cuando confirma, entonces el sistema habilita el campo para adjuntar el PDF. / Dado que no se adjuntó el PDF, cuando intenta finalizar, entonces el sistema impide el envío. | 5 | 🟡 S | 3 |
| US-09 | EP-02 | Como equipo de conducción, quiero recibir alertas de plazos de vencimiento de seminarios, para notificar a alumnos en riesgo de retraso. | Dado que se aproxima el vencimiento, cuando el sistema detecta la fecha, entonces genera una alerta visual en el perfil. / Dado que la alerta fue emitida, cuando el estudiante regulariza, entonces la alerta desaparece del tablero. | 5 | 🟡 S | 3 |
| US-10 | EP-02 | Como integrante de la CPR, quiero cargar los datos de la tesis, para oficializar el seguimiento de maestrías y doctorados. | Dado que un usuario CPR ingresa datos de tesis, cuando guarda, entonces el perfil se actualiza con la resolución oficial. / Dado que un usuario sin permisos intenta editar tesis, cuando guarda, entonces el sistema bloquea la acción. | 3 | 🟡 S | 3 |
| US-17 | EP-04 | Como equipo de conducción, quiero ver el estado de los trabajos finales (TFI o tesis) por cohorte, para detectar cuellos de botella. | Dado que selecciona una cohorte, cuando consulta, entonces el sistema muestra estudiantes por etapa (sin iniciar, en curso, presentado, aprobado). / Dado que consulta la vista general, cuando la carga, entonces muestra una comparación entre cohortes. | 5 | 🟡 S | 3 |
| US-14 | EP-03 | Como docente, quiero recibir recordatorios automáticos por correo, para cumplir con la carga de notas en los plazos estipulados. | Dado que vence el plazo y la planilla está vacía, cuando el sistema hace el barrido, entonces envía un recordatorio al docente. / Dado que el docente completó la carga, cuando el sistema hace el barrido, entonces no envía ningún correo. | 5 | 🟡 S | 4 |
| US-20 | EP-04 | Como equipo de conducción, quiero ver el estado de acreditación de seminarios por cohorte, para tomar decisiones pedagógicas. | Dado que selecciona una cohorte, cuando consulta, entonces muestra acreditados, pendientes y no iniciados por seminario. / Dado que consulta la vista general, cuando la carga, entonces muestra una comparativa entre cohortes. | 5 | 🟡 S | 4 |
| US-23 | EP-04 | Como equipo de conducción, quiero conocer qué estudiantes presentan ralentización, para intervenir con acompañamiento a tiempo. | Dado que selecciona una cohorte, cuando consulta, entonces lista los estudiantes que superaron el tiempo esperado sin completar la carrera. / Dado que consulta la vista general, cuando la carga, entonces muestra el porcentaje de ralentización por cohorte. | 5 | 🟢 C | 4 |
| US-11 | EP-02 | Como equipo de conducción, quiero registrar el seguimiento del TFI, para controlar el avance de alumnos de especializaciones. | Dado que el alumno cursa una Especialización, cuando accede a su perfil, entonces el sistema muestra exclusivamente el módulo de TFI. / Dado que el tutor registra un avance, cuando guarda, entonces el sistema registra fecha y usuario. | 3 | 🟢 C | 4 |
| US-16 | EP-04 | Como equipo de conducción, quiero generar un reporte de desgranamiento por cohorte, para identificar deserción temprana. | Dado que selecciona una cohorte, cuando genera el reporte, entonces muestra el porcentaje de abandono respecto al total inicial. / Dado que se detecta un pico de deserción, cuando se visualizan los datos, entonces permite filtrar por motivos registrados. | 8 | 🟢 C | 5 |
| US-12 | EP-02 | Como equipo de conducción, quiero descargar el perfil académico de un estudiante o cohorte, para tener un reporte físico del avance. | Dado que selecciona a un estudiante, cuando solicita descarga, entonces el sistema genera un archivo con todo su historial. / Dado que selecciona una cohorte completa, cuando solicita descarga, entonces el sistema genera un archivo comprimido con todos los perfiles. | 5 | 🟢 C | 5 |
| US-15 | EP-03 | Como docente, quiero descargar la planilla de mis alumnos en formato analógico, para utilizarla durante la cursada presencial. | Dado que solicita la descarga, cuando la confirma, entonces el sistema genera un formato imprimible con los datos básicos. / Dado que se descarga la planilla, cuando se visualiza el archivo, entonces incluye nombre, apellido, DNI y correo. | 3 | 🟢 C | 5 |
| US-07 | EP-01 | Como aspirante, quiero ingresar mis motivaciones y forma de conocer la oferta, para que el equipo de conducción evalúe mi perfil. | Dado que ingresa sus motivaciones, cuando escribe en el campo, entonces el sistema permite un máximo de 500 caracteres. / Dado que selecciona "Otros" como fuente, cuando confirma, entonces el sistema despliega un campo de texto adicional. | 2 | 🟢 C | 5 |
</details>

---

<div align="center">

**Sistema de Gestión Académica para Posgrado · UTN FRLP**

*Un buen backlog es la base de un proyecto ágil exitoso.*

![Scrum](https://img.shields.io/badge/Framework-Scrum-1a3a5c?style=flat-square)
![Sprints](https://img.shields.io/badge/Sprints-5%20×%202%20semanas-0d7a5f?style=flat-square)
![SP Total](https://img.shields.io/badge/Story%20Points-91%20SP%20totales-1e6b9e?style=flat-square)
![Historias](https://img.shields.io/badge/User%20Stories-23%20historias-2d6a4f?style=flat-square)

</div>
