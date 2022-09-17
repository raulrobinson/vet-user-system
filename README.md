# Microservicio para usuarios del sistema VET Ruta2 - UTP

```
- Database en MySQL
database name: "vetsystem"
database user: "root"
database pass: "soporte"

en la tabla "roles" hacer SQL e insertar los roles siguientes:

INSERT INTO `roles` (`id`, `name`) VALUES
(1, 'ROLE_USER'),
(2, 'ROLE_MODERATOR'),
(3, 'ROLE_ADMIN');

```

## Test-0

- Method: GET
- Url: /api/public/user

- Response:
```json
{
    "path": "/api/public/user",
    "error": "Unauthorized",
    "message": "Full authentication is required to access this resource",
    "status": 401
}
```
# Registrar un nuevo usuario:

- Method: POST 
- Url: /api/auth/signup

- Body:
```json
{
    "username":"username",
    "email":"user@correo.com",
    "password":"Password123*",
    "role": [
        "mod", 
        "user"
    ]
}
```
```
Roles: 
    admin => Administrador
    mod   => Moderador
    user  => Usuario
```
# Inicio de sesion de un usuario (Token JWT)

Method: POST 
Url: /api/auth/signin
Key: Authorization Bearer XXXXXXXX....

Body:
```json
{
    "username":"username",
    "password":"Password123*"
}
```

# Test-1 via @Param

- Method: GET
- Url: /api/public/user
- Key: Authorization Bearer XXXXXXXX....

- Response: 

Body:
```
User Content.
```
