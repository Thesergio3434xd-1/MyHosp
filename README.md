# =====================================================================
#                               MyHosp
# =====================================================================

> Plataforma web hospitalaria con asistente de voz, gestion de citas y panel de usuario.

![Node](https://img.shields.io/badge/Node.js-14%2B-3C873A?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-4.21-000000?style=for-the-badge&logo=express&logoColor=white)
![Socket.IO](https://img.shields.io/badge/Socket.IO-4.8-010101?style=for-the-badge&logo=socket.io&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)

---

## Vista general

MyHosp es una aplicacion enfocada en experiencia de paciente y gestion hospitalaria, con:

- Navegacion web multipagina (inicio, login, perfil, citas, historial, ayuda).
- Asistente virtual con comandos de voz.
- Soporte de eventos en tiempo real con Socket.IO.
- Arquitectura simple para extender backend y frontend de forma rapida.

---

## Estructura del proyecto (organizada)

```text
Myhosp/
|-- public/
|   |-- css/                # estilos por modulo
|   |-- js/                 # logica cliente y view models
|   |-- img/                # recursos graficos y creditos
|   |-- *.html              # vistas principales
|-- server/
|   |-- services/           # servicios backend (auth/socket)
|-- docs/
|   |-- ORGANIZACION_CARPETAS.md
|-- server.js               # entrada principal del servidor
|-- package.json
```

Mas detalle de organizacion: ver `docs/ORGANIZACION_CARPETAS.md`.

---

## Inicio rapido

### 1) Instalar dependencias

```bash
npm install
```

### 2) Ejecutar en desarrollo

```bash
npm run dev
```

### 3) Ejecutar en produccion local

```bash
npm start
```

Servidor por defecto: `http://localhost:3000` (o el puerto configurado en `server.js`).

---

## Scripts disponibles

- `npm start`: inicia el servidor con Node.
- `npm run dev`: inicia el servidor con Nodemon.

---

## Secciones principales

- `index.html`: landing principal.
- `login.html` y `registro.html`: autenticacion.
- `dashboard.html` y `dashboard.index.html`: panel de control.
- `crear_citas*.html`, `editar_citas.html`, `ver_citas.html`: flujo de citas.
- `perfil*.html`, `editar_perfil.html`: gestion de perfil.
- `Ayuda*.html`: soporte y ayuda.
- `historial_medico.html`: historial clinico.

---

## Galeria / Decoracion (pendiente de tus imagenes)

> Esta seccion esta preparada para que luego me digas exactamente que imagenes quieres usar.

### Banner principal

```md
![Banner MyHosp](public/img/TU_BANNER_AQUI.jpg)
```

### Capturas de pantalla

```md
![Home](public/img/TU_HOME_AQUI.jpg)
![Dashboard](public/img/TU_DASHBOARD_AQUI.jpg)
![Citas](public/img/TU_CITAS_AQUI.jpg)
```

### Creditos de imagenes

Actualmente hay creditos en `public/img/README.md`.

---

## Stack tecnico

- Backend: Node.js + Express + Socket.IO
- Frontend: HTML + CSS + JavaScript + Bootstrap
- Comunicacion tiempo real: WebSockets (Socket.IO)

---

## Notas de mantenimiento

- Mantener nombres de archivos en `snake_case` para vistas HTML.
- Mantener CSS por modulo en `public/css/`.
- Mantener logica JS por responsabilidad en `public/js/`.
- Evitar mover archivos HTML sin actualizar rutas y enlaces internos.

---

## Licencias y recursos

- Revisar creditos de imagenes en `public/img/README.md`.
- Si se publica en produccion, almacenar imagenes localmente y optimizadas.
