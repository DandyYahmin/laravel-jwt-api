
## Laravel register, login, logout API🔥 with JSON Web Token

This project was created to explore the API🔥 & JSON Web Token in laravel, the time spent making this project is 1 hour.


## Installation

```bash
  git clone https://github.com/DandyYahmin/laravel-jwt-api.git
```
    
### Environment Variables

To run this project, you will need to add the following environment variables to your .env file

`JWT_SHOW_BLACKLIST_EXCEPTION=true`


### Deployment

To deploy this project run
```bash
  php artisan jwt:secret
  php artisan migrate
  php artisan serve
```

### API Reference

#### Add User

```http
  POST /api/register
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `name` | `string` | **Required** |
| `email` | `string` | **Required**. **Email**. **Unique** |
| `password` | `string` | **Required**. **Min 8 character** |

#### User Login

```http
  POST /api/login
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `email` | `string` | **Required** |
| `password` | `string` | **Required** |

#### User Information

```http
  GET /api/User
```

| Authorization |
| :-------- |
| bearer + **token** |

#### User Logout

```http
  POST /api/logout
```

| Authorization |
| :-------- |
| bearer + **token** |