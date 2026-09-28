# CRUD Serverless de Libros (Laboratorio 3)

API REST con AWS Lambda, API Gateway (HTTP API) y DynamoDB, definida con Serverless Framework v4.

## Requisitos
- Node.js 20+
- Serverless Framework v4 (`npm install -g serverless`)
- Cuenta de AWS y credenciales configuradas (`aws configure`)
- Cuenta en app.serverless.com

## Despliegue
```bash
npm install
serverless deploy
```

## Pruebas locales
Requiere haber desplegado antes (usa la tabla real de AWS).
```bash
serverless offline
```
Servidor en `http://localhost:3000`.

## Endpoints
| Método | Ruta | Respuesta |
|---|---|---|
| POST | /libros | 201 · 400 |
| GET | /libros | 200 |
| GET | /libros/{id} | 200 · 404 |
| PUT | /libros/{id} | 200 · 400 · 404 |
| DELETE | /libros/{id} | 200 · 404 |

Ejemplo de body:
```json
{ "titulo": "Cien años de soledad", "autor": "Gabriel García Márquez", "precio": 50000, "stock": 5 }
```

## URL de la API
https://6mwwnyj7te.execute-api.us-east-1.amazonaws.com

## Limpieza
```bash
serverless remove
```