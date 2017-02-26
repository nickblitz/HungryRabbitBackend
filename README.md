## HungryRabbit Backend

HungryRabbit express backend for Restful endpoints

### Installation procedure

**1. Downloading the code**

  Clone the repo with `git clone git@github.com:nickblitz/HungryRabbitBackend.git`


**2. Starting the server**

1. Make sure you have mongoDB installed on your system
2. Run `mongod` to initiate mongoDB
3. Inside the project root, run these commands

```sh
$ npm install
$ npm start
```

### API endpoints

- Login
  - API path: api/auth/login
  - Method: POST
  - Parameters:
    - email
    - password
  - Response format
    ```
    {
      "success": true,
      "message": "user created successfully",
      "data": {
        "jwtAccessToken": "JWT eyJhbGciOiJIUzI1NiIsI...",
        "user": {
          "__v": 0,
          "email": "user@gmail.com",
          "password": "$2a$10$6U3AOzzdBbPH6a3kqA6.feei6GgvPSURkVHNdL13QhPFmnZVVTgnm",
          "phoneNo": "9191919191",
          "_id": "57e272c7268e9103947bc472",
          "jwtAccessToken": null,
          "createdAt": "2016-09-21T11:45:11.898Z"
        }
      }
    }
    ```
- Logout
  - API path: api/auth/logout
  - Method: GET
  - Parameters: none (Authorization header must be present)
  - Response format
    ```
    {
      "success": true,
      "message": "user logout successfully"
    }
    ```
- Register
  - API path: api/users/register
  - Method: POST
  - Parameters:
    - email
    - password
  - Response format
    ```
    {
      "success": true,
      "message": "user created successfully",
      "data": {
        "jwtAccessToken": "JWT eyJhbG...",
        "user": {
          "__v": 0,
          "email": "user@gmail.com",
          "password": "$2a$10$6U3AOzzdBbPH6a3kqA6.feei6GgvPSURkVHNdL13QhPFmnZVVTgnm",
          "_id": "57e272c7268e9103947bc472",
          "jwtAccessToken": null,
          "createdAt": "2016-09-21T11:45:11.898Z"
        }
      }
    }
    ```
- Get user details
  - API path: api/users
  - Method: GET
  - Parameters: none (Authorization header must be present)
  - Response format
    ```
    {
      "success": true,
      "message": "User found",
      "data": {
        "user": {
          "_id": "57f7a4a94780025e27f8349b",
          "email": "user@gmail.com",
          "__v": 0,
          "jwtAccessToken": null,
          "createdAt": "2016-10-07T13:35:37.378Z"
        }
      }
    }
    ```

Full documentation coming soon.

Happy coding!
