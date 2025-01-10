# Sistema de inicio de sesión angular con autenticación JWT

Este proyecto es una implementación de un sistema de inicio de sesión en Angular utilizando JWT (JSON Web Tokens) para la autenticación. El frontend se comunica con una API RESTful para validar las credenciales del usuario y almacenar el token de acceso en el almacenamiento local (localStorage) para mantener la sesión activa.

## Estructura del Proyecto

El proyecto está organizado de la siguiente manera:

```
src/
  app/
    app-routing.module.ts
│   app.component.css
│   app.component.html
│   app.component.spec.ts
│   app.component.ts
│   app.module.ts
│
├───components
│   ├───dashboard
│   │       dashboard.component.css
│   │       dashboard.component.html
│   │       dashboard.component.spec.ts
│   │       dashboard.component.ts
│   │
│   └───login
│           login.component.css
│           login.component.html
│           login.component.spec.ts
│           login.component.ts
│
├───guards
│       auth.guard.spec.ts
│       auth.guard.ts
│       login.guard.spec.ts
│       login.guard.ts
│
├───interceptors
│       auth.interceptor.spec.ts
│       auth.interceptor.ts
│
├───models
│       login.ts
│
└───services
        auth.service.spec.ts
        auth.service.ts
```

## Funcionalidades

- **Inicio de sesión con JWT**: Los usuarios pueden iniciar sesión proporcionando su correo electrónico y contraseña. El backend valida las credenciales y devuelve un token JWT que se guarda en el almacenamiento local.
- **Interceptor para solicitudes autenticadas**: Un interceptor de HTTP asegura que el token JWT se adjunte a todas las solicitudes protegidas.

- **Redirección y manejo de errores**: Si las credenciales son correctas, el usuario es redirigido a la página principal. Si hay un error, se muestra un mensaje de error en el formulario.

## Tecnologías Utilizadas

- **Angular**: Framework frontend para construir la interfaz de usuario interactiva.
- **RxJS**: Para manejar operaciones asíncronas en Angular.

## Instrucciones de Instalación

1. Clona el repositorio:

   ```bash
   https://github.com/Hassam11/frontend-angular-auth-jwt
   ```

2. Navega al directorio del proyecto:

   ```bash
   cd frontend-angular-auth-jwt
   ```

3. Instala las dependencias:

   ```bash
   npm install
   ```

4. Ejecuta el proyecto:

   ```bash
   ng serve
   ```
