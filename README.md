# MyHosp 🏥

> Plataforma web de gestión hospitalaria centrada en la experiencia del usuario, accesibilidad para adultos mayores y optimización del agendamiento médico.

![Node](https://img.shields.io/badge/Node.js-14%2B-3C873A?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-4.21-000000?style=for-the-badge&logo=express&logoColor=white)
![Socket.IO](https://img.shields.io/badge/Socket.IO-4.8-010101?style=for-the-badge&logo=socket.io&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)

---

## 👥 Creadores

- Cristian Eduardo Carvajal Izquierdo
- Daniel Alejandro Gamba Martínez
- Ronald Neomar Tapias Rojas
- Sergio Alejandro Uribe Montealegre

---

## 🧭 Tabla de contenido

1. [Contexto y definición del problema](#-contexto-y-definicion-del-problema)
2. [Justificación del proyecto](#-justificacion-del-proyecto-desde-la-experiencia-del-usuario)
3. [Recolección de requerimientos y análisis de usuario](#-recoleccion-de-requerimientos-y-analisis-de-usuario)
4. [Mapa de experiencia del usuario](#-mapa-de-experiencia-del-usuario-user-journey-map)
5. [Historias de usuario](#-historias-de-usuario)
6. [Arquitectura de la información](#-arquitectura-de-la-informacion)
7. [Diagrama de navegación](#-diagrama-de-navegacion)
8. [Diseño de interfaces](#-diseno-de-interfaces)
9. [Pruebas de usabilidad](#-pruebas-de-usabilidad)
10. [Validación del diseño](#-validacion-del-diseno)
11. [Reflexión final](#-reflexion-final)
12. [Vista previa e imágenes](#-vista-previa-e-imagenes)
13. [Estructura técnica del repositorio](#-estructura-tecnica-del-repositorio)
14. [Inicio rápido](#-inicio-rapido)
15. [Bibliografía](#-bibliografia)

---

## 🎯 Contexto y definición del problema

Colombia enfrenta barreras importantes en el acceso oportuno a servicios de salud. Según cifras referenciadas en el proyecto:

- El **64% de los colombianos** percibe una sobrecarga del sistema de salud (Ipsos, 2024).
- El **83% de los colombianos** reporta al menos una barrera para acceder a la atención médica (The Economist, 2023).

Estas dificultades impactan especialmente a personas mayores de edad y a usuarios con baja alfabetización digital, quienes experimentan procesos lentos para solicitar citas, comprender interfaces y gestionar su información médica.

---

## 💡 Justificación del proyecto desde la experiencia del usuario

MyHosp nace para reducir fricción en procesos críticos del sistema de salud:

- Agendar citas médicas en pocos pasos.
- Consultar historial clínico de forma clara y rápida.
- Facilitar el acceso mediante interfaz amigable y asistente de voz.
- Mejorar la eficiencia del personal médico con información más accesible.

### Metas del proyecto

- Alcanzar una aceptación mínima del **75%** en usuarios finales.
- Reducir el tiempo de agendamiento a **2-3 minutos**.
- Lograr indicadores de satisfacción/usabilidad cercanos al **80%**.

---

## 🔎 Recolección de requerimientos y análisis de usuario

### Investigación de usuario

- **Población de estudio:** ciudadanos colombianos insatisfechos con el sistema de salud.
- **Público objetivo:** adultos colombianos mayores de 60 años.
- **Técnicas UX utilizadas:** revisión de estudios cuantitativos, observación de comportamiento, pruebas moderadas y entrevistas cortas post-tarea.

### Fuentes de investigación clave

- Informe de Servicios de Salud de Ipsos 2024.
- Health Inclusivity Index (The Economist Impact).

### Personas / arquetipos

#### 1) Claudia Piraban

- Objetivo: navegar entre secciones y completar login/registro con claridad.
- Frustraciones: instrucciones poco visibles para activar el asistente virtual.

#### 2) Ana Isabel Martínez (tercera edad)

- Objetivo: iniciar sesión y consultar perfil sin apoyo externo.
- Frustraciones: tipografía pequeña y baja claridad visual en formularios.

#### 3) Luis Hernando Reyes

- Objetivo: acceso veloz a perfil, dashboard e historial clínico.
- Frustraciones: navegación poco intuitiva y sobrecarga visual en algunos módulos.

### Escenarios de uso y necesidad clave

1. **Agendamiento rápido de cita médica** desde móvil.
2. **Consulta de resultados de laboratorio** con filtros por fecha/tipo.
3. **Flujo médico de consulta**: revisar historial, añadir nota y generar receta.

---

## 🗺️ Mapa de experiencia del usuario (User Journey Map)

El User Journey Map permitió identificar:

- Emociones predominantes (confusión inicial, alivio tras completar tareas).
- Puntos de contacto críticos (login, asistente virtual, dashboard).
- Oportunidades de mejora en accesibilidad, visibilidad y flujo.

### Relación directa con la solución propuesta

- Aumento de contraste y tamaño de tipografía.
- Reorganización de elementos en interfaz para reducir carga cognitiva.
- Clarificación de indicaciones para uso del asistente virtual.
- Creación de una navegación más lineal e intuitiva entre módulos.

---

## 🧾 Historias de usuario

1. Como paciente adulta, quiero navegar fácilmente entre secciones para usar la plataforma sin confusiones.
2. Como paciente mayor con limitaciones visuales, quiero textos legibles y campos claros para iniciar sesión sin ayuda.
3. Como usuario habitual, quiero acceder rápido a citas y perfil desde dashboard para ahorrar tiempo.
4. Como ciudadano afectado por retrasos, quiero agendar citas en línea desde cualquier lugar para evitar barreras de acceso.
5. Como paciente con consultas previas, quiero visualizar y descargar historial médico para gestionar mi información de salud.

---

## 🏗️ Arquitectura de la información

La plataforma sigue una estructura jerárquica con módulos principales:

- Inicio
- Login / Registro
- Dashboard
- Citas
- Perfil
- Historial médico
- Consultas online
- Ayuda

### Relación entre elementos

- Flujo principal: **Landing → Login/Registro → Dashboard → Módulos**.
- Flujo secundario: recuperación de cuenta y regreso rápido a secciones clave.
- Taxonomía: categorías y subcategorías claras.
- Ontología: conexión entre perfil, citas e historial clínico.
- Folksonomía: uso potencial de etiquetas por especialidad/tema médico.

---

## 🧭 Diagrama de navegación

Se adoptó un modelo **lineal con jerarquía**, orientado a:

- Reducir distracciones.
- Facilitar la curva de aprendizaje.
- Guiar de forma práctica al usuario en tareas prioritarias.

---

## 🎨 Diseño de interfaces

### Wireframes

Se definió una arquitectura conceptual de navegación y disposición por módulos, usada como base para estructurar el flujo de pantallas.

### Mockups

Se diseñaron mockups de alta fidelidad en Figma para:

- Landing page
- Login / Registro
- Dashboard
- Módulos: perfil, citas, historial y consultas online

### Prototipo

El prototipo web se implementó con **HTML, CSS, Bootstrap y Node.js**, incluyendo un asistente de voz como herramienta de inclusión digital.

### Diseño visual con accesibilidad y usabilidad

- Tipografía legible y mayor contraste.
- Botones, enlaces y formularios con jerarquía visual clara.
- Consistencia visual para reducir confusión.
- Enfoque especial en usuarios mayores y personas con limitaciones visuales.

---

## 🧪 Pruebas de usabilidad

### Método utilizado

Pruebas moderadas con usuarios representativos, observación directa, medición de tiempos y entrevistas breves de cierre por tarea.

### Resultados principales

- Dificultades iniciales en activación/uso del asistente virtual.
- Problemas de legibilidad en campos de formulario.
- Errores de navegación por botones o enlaces inactivos.

### Mejoras implementadas

- Mayor claridad visual en formularios.
- Señales más intuitivas en el asistente virtual.
- Corrección de errores de redirección y navegación.
- Simplificación del dashboard para priorizar acciones clave.

---

## ✅ Validación del diseño

### Conclusiones de la evaluación

- Se evidenció una mejora significativa frente a flujos tradicionales.
- Se confirmaron áreas críticas para iteración continua.
- La retroalimentación de usuarios fue clave para ajustar accesibilidad y usabilidad.

### Ajustes aplicados tras feedback

- Incremento de tipografía y contraste en componentes clave.
- Mayor visibilidad de etiquetas y campos de entrada.
- Reestructuración de navegación para disminuir confusión.
- Optimización visual y funcional del asistente virtual.

---

## 🧠 Reflexión final

MyHosp confirma que una solución funcional no siempre es intuitiva hasta validarse con usuarios reales. El aprendizaje principal del equipo fue integrar investigación UX, accesibilidad y pruebas iterativas como eje del desarrollo para lograr una plataforma útil, clara e inclusiva.

---

## 🖼️ Vista previa e imágenes

### Logo del proyecto

![Logo MyHosp](public/img/logo.png)

### Recursos visuales de referencia

| Vista | Imagen |
|---|---|
| Atención médica | ![Doctor](public/img/DOCTOR.png) |
| Gestión documental | ![Documento](public/img/documento.png) |

### Nota sobre imágenes

Los créditos y fuentes se encuentran en `public/img/README.md`.

---

## 🧱 Estructura técnica del repositorio

```text
Myhosp/
|-- public/
|   |-- css/
|   |-- js/
|   |-- img/
|   |-- *.html
|-- server/
|   |-- services/
|-- server.js
|-- package.json
```

---

## 🚀 Inicio rápido

### 1) Instalar dependencias

```bash
npm install
```

### 2) Ejecutar en desarrollo

```bash
npm run dev
```

### 3) Ejecutar en producción local

```bash
npm start
```

Servidor local por defecto: `http://localhost:3000`.

---

## ⚙️ Scripts disponibles

- `npm start`: inicia el servidor con Node.
- `npm run dev`: inicia el servidor con Nodemon.

---

## 📚 Bibliografía

- Economist Impact. *Health inclusivity index* (infographic). https://impact.economist.com/projects/health-inclusivity-index/infographic-phase2
- Mantilla, N. (2024). ¿Por qué es tan difícil agendar citas médicas en Colombia? Coco Tecnologías. https://cocotech.ai/por-que-es-tan-dificil-agendar-citas-medicas-en-colombia-transformando-el-acceso-a-la-salud/
- Ipsos. (2024). *Ipsos Health Service Report 2024*. https://www.ipsos.com/sites/default/files/ct/news/documents/2024-09/Ipsos%20Health%20Service%20Report%202024%20Global%20Charts_ESP_PE.pdf
- Las2orillas. 77% de colombianos piensa que esperas de citas médicas son muy largas. https://www.las2orillas.co/77-de-colombianos-piensa-que-esperas-de-citas-medicas-son-muy-largas-y-otros-datos-reveladores/

---

## ❤️ Estado del proyecto

Proyecto académico y funcional en evolución, con foco en mejoras continuas de usabilidad, accesibilidad y desempeño del flujo de citas médicas.
