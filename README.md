# Around The U.S. - React
Autor

Rocio Zarate

Desarrolladora Web en formación | TripleTen

Proyecto desarrollado como parte del Bootcamp de Desarrollo Web de TripleTen.


## Descripción

Around The U.S. es una aplicación web desarrollada con React como parte del Bootcamp de Desarrollo Web de TripleTen.

En esta versión del proyecto se implementó un sistema de registro, inicio de sesión y autorización de usuarios. Los usuarios pueden crear una cuenta, iniciar sesión y acceder a las funciones de la aplicación únicamente cuando están autenticados.

Una vez iniciada la sesión, los usuarios pueden:

- Ver su perfil y la información del usuario.
- Editar su información personal.
- Cambiar su foto de avatar.
- Agregar nuevas tarjetas.
- Dar y quitar "Me gusta" a las tarjetas.
- Eliminar tarjetas.
- Visualizar las imágenes de las tarjetas.
- Cerrar sesión.

La aplicación también mantiene la sesión del usuario mediante un token JWT almacenado en `localStorage`.

---

## Funcionalidades

### Registro

Los usuarios pueden crear una cuenta utilizando su correo electrónico y contraseña.

### Inicio de sesión

Los usuarios registrados pueden iniciar sesión. Al hacerlo, la aplicación recibe un token JWT que se utiliza para identificar y autorizar al usuario.

### Rutas protegidas

La ruta principal de la aplicación está protegida.

Si un usuario no ha iniciado sesión e intenta acceder a la aplicación, es redirigido a la página de inicio de sesión.

### Sesión persistente

El token JWT se guarda en `localStorage`, permitiendo mantener la sesión cuando el usuario recarga la página.

Al abrir nuevamente la aplicación, se verifica el token antes de permitir el acceso a las rutas protegidas.

### Funciones de tarjetas

Los usuarios autenticados pueden:

- Ver las tarjetas disponibles.
- Crear nuevas tarjetas.
- Dar y quitar "Me gusta".
- Eliminar tarjetas.
- Abrir las imágenes de las tarjetas en una ventana emergente.

### Perfil de usuario

Los usuarios pueden:

- Ver su información.
- Editar nombre y descripción.
- Actualizar su avatar.

---

## Tecnologías utilizadas

- React
- Vite
- JavaScript (ES6+)
- JSX
- CSS
- HTML5
- React Router
- Context API
- React Hooks
  - `useState`
  - `useEffect`
  - `useContext`
- `localStorage`
- JWT (JSON Web Token)
- Fetch API
- API REST

---

## Técnicas y conceptos utilizados

Durante el desarrollo del proyecto se trabajó con:

- Componentes reutilizables de React.
- Manejo de estado con `useState`.
- Efectos secundarios con `useEffect`.
- Compartición de información mediante Context API.
- Navegación y rutas con React Router.
- Rutas protegidas mediante componentes de autorización.
- Autenticación mediante JWT.
- Persistencia de sesión utilizando `localStorage`.
- Peticiones HTTP utilizando `fetch`.
- Métodos HTTP como `GET`, `POST`, `PATCH`, `PUT` y `DELETE`.
- Manejo de respuestas y errores de una API.
- Formularios controlados y validación.
- Comunicación con APIs REST.

---

## Estructura del proyecto

```text
src/
├── assets/
│
├── blocks/
│
├── components/
│   ├── Footer/
│   ├── Header/
│   │
│   ├── Login/
│   │   └── Login.jsx
│   │
│   ├── Register/
│   │   └── Register.jsx
│   │
│   ├── ProtectedRoute/
│   │   └── ProtectedRoute.jsx
│   │
│   ├── InfoTooltip/
│   │   └── InfoTooltip.jsx
│   │
│   └── Main/
│       ├── components/
│       │   └── Card/
│       │       └── Card.jsx
│       │
│       ├── Popup/
│       │   ├── EditAvatar/
│       │   ├── EditProfile/
│       │   ├── ImagePopup/
│       │   ├── NewCard/
│       │   └── RemoveCard/
│       │
│       ├── Popup.jsx
│       └── Main.jsx
│
├── contexts/
│   └── CurrentUserContext.js
│
├── hooks/
│   └── UseFormValidation.js
│
├── images/
│
├── utils/
│   ├── api.js
│   └── auth.js
│
├── vendor/
│
├── App.jsx
├── index.css
└── main.jsx
```

## Instalación

Clona el repositorio:

```bash
git clone https://github.com/ruzarate31-sudo/web_project_around_auth.git
```

Entra en la carpeta del proyecto:

```bash
cd web_project_around_auth
```

Instala las dependencias:

```bash
npm install
```

Ejecuta el proyecto en modo desarrollo:

```bash
npm run dev
```

Para crear la versión de producción:

```bash
npm run build
```

### Repositorio

https://github.com/ruzarate31-sudo/web_project_around_auth
