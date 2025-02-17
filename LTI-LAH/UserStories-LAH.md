# 📌 Backlog de Producto - ATS LTI ::: V1

> Esta primera versión de la solución está enfocada en enviarle a ChatGPT la descripción del ejercicio propuesto por LTI e indicarle que me genere unas tareas clave.
> 
> Luego, basado en esas tareas, le indiqué que adjuntaría el archivo LTI-LAH.md del ejercicio anterior para implementar las tareas previamente propuestas.
> 
> Posteriormente, le especifiqué que, antes de terminar cada tarea, debía detenerse para validar la información suministrada y así yo poder darle la instrucción de continuar.
> 
> Por último, le indiqué que organizara todo en un archivo .md.

## 📍 Descripción del Proyecto
El ATS LTI es un sistema de gestión de candidatos que automatiza y optimiza el proceso de selección. Sus principales funcionalidades incluyen:
- Filtrado automático de CVs con IA.
- Coordinación de entrevistas con integración de calendarios.
- Notificaciones automáticas a candidatos.
- Evaluación y feedback de entrevistas.
- Análisis y reportes de métricas de selección.


## 📝 **Historias de Usuario**

### **1. Filtrado Automático de Candidatos**
**Como** reclutador, **quiero** que el sistema clasifique automáticamente los CVs según su relevancia, **para** agilizar el proceso de selección.

#### **Criterios de Aceptación:**
✅ El sistema debe analizar los CVs y ordenarlos según coincidencias con la descripción del puesto.
✅ Se debe mostrar un puntaje de relevancia basado en experiencia, habilidades y educación.
✅ Los reclutadores pueden aplicar filtros adicionales (ejemplo: años de experiencia, tecnologías específicas).
✅ El sistema debe permitir modificar manualmente la clasificación de un candidato.

### **2. Coordinación de Entrevistas con Integración de Calendario**
**Como** reclutador, **quiero** programar entrevistas con los candidatos de manera automatizada y sincronizada con mi calendario, **para** optimizar mi tiempo y evitar conflictos de agenda.

#### **Criterios de Aceptación:**
✅ El sistema debe permitir a los reclutadores seleccionar horarios disponibles en su calendario.
✅ Los candidatos deben recibir automáticamente una invitación con la opción de aceptar o reprogramar.
✅ La entrevista confirmada debe reflejarse en el calendario del reclutador y el candidato.
✅ Si hay un cambio en la entrevista, ambas partes deben ser notificadas automáticamente.

### **3. Notificaciones Automáticas para Candidatos**
**Como** candidato, **quiero** recibir notificaciones sobre el estado de mi postulación, **para** estar informado sobre mi proceso de selección.

#### **Criterios de Aceptación:**
✅ El sistema debe enviar un correo cuando el candidato pase a una nueva etapa.
✅ Las notificaciones deben incluir detalles del estado actual y posibles próximos pasos.
✅ El candidato debe poder acceder a un panel donde pueda revisar el historial de cambios en su postulación.
✅ Si el candidato es rechazado, el sistema debe enviar un mensaje con feedback opcional.

### **4. Evaluación y Feedback de Entrevistas**
**Como** manager, **quiero** que los reclutadores puedan registrar evaluaciones y feedback de los candidatos en el sistema, **para** tomar decisiones más informadas sobre la contratación.

#### **Criterios de Aceptación:**
✅ El sistema debe permitir a los entrevistadores ingresar comentarios y calificaciones tras cada entrevista.
✅ Los comentarios deben ser visibles solo para los reclutadores y managers con acceso autorizado.
✅ Se debe permitir la edición de evaluaciones dentro de un periodo determinado.
✅ El feedback consolidado debe mostrarse en el perfil del candidato para consulta posterior.

### **5. Panel de Análisis y Reportes**
**Como** administrador de RRHH, **quiero** acceder a reportes sobre el proceso de selección, **para** evaluar la eficiencia del sistema y mejorar la estrategia de reclutamiento.

#### **Criterios de Aceptación:**
✅ El sistema debe generar reportes con métricas como tiempo promedio de contratación, número de entrevistas realizadas y tasa de conversión de candidatos.
✅ Los reportes deben poder exportarse en formatos como PDF y Excel.
✅ El usuario debe poder aplicar filtros como rango de fechas, posiciones abiertas o responsables del proceso.
✅ El sistema debe permitir visualizar gráficos para análisis rápido de tendencias.



## 📝 **Backlog Priorizado (Metodología MoSCoW)**

| **Prioridad**  | **User Story**  | **Descripción** | **Responsable** | **Esfuerzo Estimado (Puntos de Historia)** | **Fecha Estimada** |
|--------------|--------------|---------------|----------------|----------------------------|-----------------|
| **M** Must Have | **Filtrado Automático de Candidatos** | Implementar un sistema basado en IA para analizar CVs y asignarles un puntaje de relevancia según requisitos del puesto. | Equipo Backend & Data Science | 13 | 01 - 15 Marzo 2025 |
| **M** Must Have | **Coordinación de Entrevistas con Integración de Calendario** | Permite a los reclutadores sincronizar sus calendarios y programar entrevistas automáticamente. | Equipo Backend & Frontend | 8 | 10 - 20 Marzo 2025 |
| **M** Must Have | **Notificaciones Automáticas para Candidatos** | Implementar un sistema de notificaciones vía correo y SMS para mantener informados a los candidatos. | Equipo Backend | 5 | 15 - 25 Marzo 2025 |
| **S** Should Have | **Evaluación y Feedback de Entrevistas** | Crear un módulo donde los reclutadores registren comentarios y puntuaciones tras las entrevistas. | Equipo Backend & UX/UI | 8 | 25 Marzo - 05 Abril 2025 |
| **C** Could Have | **Panel de Análisis y Reportes** | Implementar dashboards con métricas clave del proceso de selección. | Equipo Backend & Data Science | 13 | 10 - 25 Abril 2025 |



## 🎟️ **Tickets de Trabajo - Filtrado Automático de Candidatos**

| **ID** | **Título del Ticket** | **Descripción Técnica** | **Responsable** | **Esfuerzo Estimado (Puntos de Historia)** | **Dependencias** |
|--------|----------------------|------------------------|----------------|----------------------------|-----------------|
| **T-101** | **Diseñar Modelo de IA para Filtrado de CVs** | Crear un modelo de Machine Learning que analice CVs y determine relevancia basada en palabras clave, experiencia y educación. | Data Science | 8 | Ninguna |
| **T-102** | **Desarrollar API para Evaluación de CVs** | Construir una API en Spring Boot que reciba CVs en PDF/Texto, los procese y retorne un puntaje. | Backend | 8 | T-101 |
| **T-103** | **Implementar Almacenamiento de CVs en Base de Datos** | Diseñar esquema en PostgreSQL para almacenar CVs y resultados del análisis. | Backend | 5 | Ninguna |
| **T-104** | **Integrar Frontend con API de Filtrado** | Implementar en React la interfaz para que los reclutadores puedan visualizar la clasificación de CVs. | Frontend | 5 | T-102 |
| **T-105** | **Pruebas y Optimización del Modelo de IA** | Evaluar el rendimiento del modelo y ajustar hiperparámetros para mejorar precisión. | Data Science | 8 | T-101 |
| **T-106** | **Implementar Logging y Monitoreo** | Configurar logs en la API para registrar procesamiento de CVs y métricas de desempeño. | DevOps | 3 | T-102 |

**Total de Esfuerzo Estimado:** **75 - 100 horas**

***

# 📌 Backlog de Producto - ATS LTI ::: V2

> En esta segunda versión se opto por darle informacion puntual a **ChatGPT** minimizando la probabilidad de generar informacion inecesaria 

## Historias de Usuario

### Historia de Usuario 1: **Recepción y Filtrado de CVs**
**Como** reclutador, **quiero** recibir y filtrar CVs de los candidatos, **para** poder priorizar los más adecuados para el puesto.

**Criterios de Aceptación:**
- Los reclutadores pueden recibir CVs desde diferentes portales de empleo.
- Los CVs se filtran usando palabras clave y criterios definidos.
- Los candidatos se priorizan según el filtro aplicado.

---

### Historia de Usuario 2: **Gestión del Proceso de Selección**
**Como** reclutador, **quiero** gestionar el proceso de selección de los candidatos, **para** poder hacer seguimiento de su estado y coordinar las entrevistas.

**Criterios de Aceptación:**
- Los reclutadores pueden asignar estados a los candidatos (Pendiente, Revisado, Entrevistado, Contratado, Rechazado).
- Se pueden programar entrevistas con los candidatos.
- Los perfiles de los candidatos pueden ser compartidos con otros miembros del equipo.

---

### Historia de Usuario 3: **Comunicación con Candidatos**
**Como** candidato, **quiero** recibir notificaciones de los avances en mi proceso de selección, **para** estar informado sobre el estado de mi aplicación.

**Criterios de Aceptación:**
- Los candidatos reciben notificaciones sobre su estado en el proceso de selección.
- Se notifica a los candidatos cuando se les programa una entrevista.
- Los candidatos pueden recibir respuestas a preguntas frecuentes.

---

## Backlog del Proyecto

| **Tarea**                                          | **Estimación (Fibonacci)** | **Dependencias**                     | **Estado**        |
|----------------------------------------------------|----------------------------|--------------------------------------|-------------------|
| Implementar sistema de recepción y filtrado de CVs | **5**                      | Ninguna                              | No comenzada      |
| Implementar gestión de estados de candidatos       | **8**                      | Implementar sistema de filtrado de CVs| No comenzada      |
| Desarrollar funcionalidad de programación de entrevistas | **8**                  | Implementar gestión de estados de candidatos | No comenzada      |
| Implementar opción de compartir perfiles con el equipo | **5**                  | Implementar gestión de estados de candidatos | No comenzada      |

---

## Tickets de Trabajo

### Tarea 1: Crear sistema de gestión de estados de los candidatos
- **Descripción**: Crear un sistema que permita actualizar y gestionar los diferentes estados de los candidatos a lo largo del proceso de selección (Pendiente, Revisado, Entrevistado, Contratado, Rechazado).
- **Particularidades Técnicas**:
  - Crear una enumeración (`Enum`) en el backend para los estados de los candidatos.
  - Implementar una API RESTful en Spring Boot para actualizar y consultar el estado de los candidatos.
  - Integración con la base de datos para persistir los estados en la entidad `Candidate`.
  - Seguridad y control de acceso para garantizar que solo usuarios con permisos de reclutador puedan modificar el estado.
- **Responsables**:
  - **Desarrollador Backend**: Implementación del sistema de gestión de estados y la creación de la API.
  - **Desarrollador Frontend**: Integración con la interfaz para mostrar y actualizar el estado de los candidatos.
- **Flujo de Planificación**:
  - **Semana 1**: Diseño de la base de datos y definición de la API.
  - **Semana 2**: Implementación de la API y pruebas unitarias.
  - **Semana 3**: Implementación del frontend para mostrar los estados.
  - **Semana 4**: Pruebas integradas y validación de seguridad.

---

### Tarea 2: Crear sistema de programación de entrevistas
- **Descripción**: Crear una funcionalidad para que los reclutadores puedan programar entrevistas con los candidatos seleccionados.
- **Particularidades Técnicas**:
  - Crear un formulario para capturar los datos de la entrevista (fecha, hora, lugar, reclutador asignado).
  - Implementar lógica en el backend para asociar entrevistas a aplicaciones (`Interview` y `Application`).
  - Integrar con el calendario del reclutador para gestionar la disponibilidad.
  - Notificar a los candidatos cuando se haya programado una entrevista.
- **Responsables**:
  - **Desarrollador Backend**: Implementación de la lógica de programación de entrevistas y su integración con la base de datos.
  - **Desarrollador Frontend**: Desarrollo de la interfaz de usuario para la programación de entrevistas.
  - **Desarrollador de Integración**: Integración con el calendario (posiblemente usando APIs como Google Calendar).
- **Flujo de Planificación**:
  - **Semana 1**: Reunión con el equipo para definir la integración del calendario.
  - **Semana 2**: Implementación del backend y la base de datos.
  - **Semana 3**: Desarrollo de la interfaz de usuario para programación de entrevistas.
  - **Semana 4**: Realización de pruebas de integración.

---

### Tarea 3: Crear opción para compartir perfiles con el equipo
- **Descripción**: Crear una funcionalidad que permita a los reclutadores compartir los perfiles de los candidatos con otros miembros del equipo de selección.
- **Particularidades Técnicas**:
  - Implementar una API que permita compartir la información del candidato (nombre, CV, estado) a otros usuarios (reclutadores o managers).
  - Implementar controles de acceso para asegurar que solo los usuarios autorizados puedan ver y compartir la información.
  - Enviar notificaciones a los usuarios destinatarios del perfil.
  - Integrar esta funcionalidad en la interfaz de usuario.
- **Responsables**:
  - **Desarrollador Backend**: Creación de la API para compartir perfiles y manejo de permisos de acceso.
  - **Desarrollador Frontend**: Desarrollo de la interfaz de usuario para compartir perfiles.
  - **Desarrollador de Seguridad**: Gestión de los controles de acceso y permisos.
- **Flujo de Planificación**:
  - **Semana 1**: Diseño de la arquitectura de permisos y API.
  - **Semana 2**: Implementación de la API y pruebas unitarias.
  - **Semana 3**: Desarrollo de la interfaz de usuario para compartir perfiles.
  - **Semana 4**: Realización de pruebas de integración y validación de seguridad.

---

## Estimaciones con Fibonacci

| **Tarea**                                          | **Responsables**                                     | **Estimación (Fibonacci)** | **Dependencias**                     | **Estado**        |
|----------------------------------------------------|------------------------------------------------------|----------------------------|--------------------------------------|-------------------|
| Crear sistema de gestión de estados de los candidatos | Backend, Frontend                                   | **5**                      | Ninguna                              | No comenzada      |
| Crear sistema de programación de entrevistas       | Backend, Frontend, Integración                       | **8**                      | Crear sistema de gestión de estados  | No comenzada      |
| Crear opción para compartir perfiles con el equipo | Backend, Frontend, Seguridad                         | **8**                      | Crear sistema de gestión de estados  | No comenzada      |
"""

