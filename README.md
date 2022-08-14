## JWT Authentication Token with MySQL database

- BD en MySQL

> Test-0

Method: GET
Url: /api/test/user

Response:
{
    "path": "/api/test/user",
    "error": "Unauthorized",
    "message": "Full authentication is required to access this resource",
    "status": 401
}

> Registrar un nuevo usuario:

Method: POST 
Url: /api/auth/signup

Body:
{
    "username":"username",
    "email":"user@correo.com",
    "password":"Password",
    "role": [
        "mod", 
        "user"
    ]
}

Roles: 
    admin => Administrador
    mod => Moderador
    user => Usuario

> Inicio de sesion de un usuario (Token JWT)

Method: POST 
Url: /api/auth/signin
Key: Authorization Bearer XXXXXXXX....

Body:
{
    "username":"usuariodos",
    "password":"Password321*"
}

> Test-1 () 

Method: GET
Url: /api/test/user
Key: Authorization Bearer XXXXXXXX....

Response: User Content.

