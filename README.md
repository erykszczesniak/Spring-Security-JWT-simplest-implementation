## 1. Register a new user

**URL**: `POST /auth/register` 

`http://localhost:8080/auth/register`
```json
{
"name": "Eryk",
"password": "123456",
"email": "eryk@gmail.com",
"roles": "USER"
}
```

![Screenshot 2024-04-23 at 20 04 44](https://github.com/erykszczesniak/Spring-Security-JWT-simplest-implementation/assets/64661383/7b7a599e-23a3-490f-ab4d-babc49c50020)



## 2. Token Generation

**Endpoint**: `POST /auth/generateToken`

**Description**: This endpoint is used for existing users to generate a new authentication token.

**Request JSON**:

```json
{
  "username": "Eryk",
  "password": "123456"
}
```

![Screenshot 2024-04-23 at 20 07 54](https://github.com/erykszczesniak/Spring-Security-JWT-simplest-implementation/assets/64661383/b42e46a1-e9ce-4d73-9f67-9c9c0abe21e7)

**Response**: A `200 OK` status with a JWT token in the response body.



## 3. Protected Endpoint Access

**Endpoint**: `GET /auth/hello`

**Description**: This endpoint returns a greeting message. It is a protected endpoint that requires a valid token.

**Authentication**: Bearer Token

**Response**: A `200 OK` status with a simple greeting message in the response body.

![img_2.png](src/main/resources/static/img/img_2.png)

---
