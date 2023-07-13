---------------Login and Signup REST API with JWT Authentication---------------

This is a backend application built with Node.js and Express.js that provides login and signup functionality with JWT (JSON Web Token) authentication. It uses Sequelize as the ORM and an SQLite database for storing user information.

---------------Installation---------------

- Make sure you have Node.js installed on your machine. You can download it from the official website: https://nodejs.org
- Clone this repository or download the source code.
- Open a terminal or command prompt and navigate to the project directory.
- Install the dependencies by running the following command: npm install
- Once the dependencies are installed, you can start the server with the following command: node index.js
- The server will start running on http://localhost:3000.

---------------Usage---------------

----------Signup Endpoint----------

To create a new user account, send a POST request to http://localhost:3000/signup with a JSON payload containing the following fields:
{
  "username": "your-username",
  "password": "your-password",
  "email": "your-email@example.com"
}

If the signup is successful, you will receive a response with a status code of 201 and a message indicating that the user was created successfully.

----------Login Endpoint----------

To log in and obtain a JWT token, send a POST request to http://localhost:3000/login with a JSON payload containing the following fields:
{
  "username": "your-username",
  "password": "your-password"
}

If the provided credentials are valid, you will receive a response with a status code of 200 and a JSON object containing a JWT token.

----------Hello Endpoint----------

To access the protected "Hello" endpoint, send a GET request to http://localhost:3000/hello. Make sure to include the JWT token in the Authorization header as Bearer <token>, where <token> is the JWT token obtained from the login request.

If the token is valid and the user is authenticated, you will receive a response with a status code of 200 and a message of "Hello from GreenStitch".


