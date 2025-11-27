# Friend List API 👫

This project is a simple API for managing a list of friends, demonstrating user authentication and basic CRUD operations. It's built with Node.js and Express, providing a robust backend for handling user sessions and data management.

## 🚀 Technologies and Skills Demonstrated

This project showcases proficiency in the following areas:

### Backend Development

- **Node.js**: Asynchronous event-driven JavaScript runtime, enabling the development of scalable network applications.
- **Express.js**: A fast, unopinionated, minimalist web framework for Node.js, used for building robust APIs and web applications.
- **RESTful APIs**: Design and implementation of REST principles for efficient and stateless communication between client and server.

### Authentication & Authorization

- **JWT (JSON Web Tokens)**: Securely transmitting information between parties as a compact, URL-safe JSON object. Used for access token generation and verification.
- **`express-session`**: Middleware for managing user sessions, providing persistent storage of session data on the server-side.
- **User Registration & Login**: Implementation of secure user signup and sign-in flows with authentication checks.
- **Middleware**: Custom middleware for authenticating requests and protecting API endpoints.

### Data Management

- **In-memory Data Store**: Simple object-based data storage for users and friends, suitable for demonstration purposes.
- **CRUD Operations**: Full implementation of Create, Read, Update, and Delete functionalities for friend records.

### Development Tools

- **Nodemon**: A utility that monitors for any changes in your source and automatically restarts your server, enhancing development workflow.
- **`package.json`**: Management of project metadata and dependencies.

## ⚙️ Setup and Installation

To get this project up and running locally, follow these steps:

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/rafael-a-g-n/nodejs_PracticeProject_AuthUserMgmt.git
    cd nodejs_PracticeProject_AuthUserMgmt
    ```

2.  **Install dependencies:**

    ```bash
    npm install
    ```

3.  **Start the server:**
    ```bash
    npm start
    ```
    The server will run on `http://localhost:3000`.

## 📈 API Endpoints

The API provides the following endpoints:

### Authentication

- `POST /login`

  - **Description**: Authenticate a user and receive an access token.
  - **Request Body**:
    ```json
    {
      "username": "your_username",
      "password": "your_password"
    }
    ```
  - **Response**: `User successfully logged in` or `Invalid Login. Check username and password`.

- `POST /register`
  - **Description**: Register a new user.
  - **Request Body**:
    ```json
    {
      "username": "new_username",
      "password": "new_password"
    }
    ```
  - **Response**: `User successfully registered. Now you can login` or `User already exists!`.

### Friends Management (Protected by Authentication)

- `GET /friends`

  - **Description**: Retrieve a list of all friends.

- `GET /friends/:email`

  - **Description**: Retrieve details of a specific friend by email.
  - **Path Parameter**: `email` (e.g., `johnsmith@gmail.com`)

- `POST /friends`

  - **Description**: Add a new friend to the list.
  - **Request Body**:
    ```json
    {
      "email": "new_friend@example.com",
      "firstName": "New",
      "lastName": "Friend",
      "DOB": "01-01-2000"
    }
    ```
  - **Response**: `The user New Has been added!`

- `PUT /friends/:email`

  - **Description**: Update the details of an existing friend.
  - **Path Parameter**: `email` (e.g., `johnsmith@gmail.com`)
  - **Request Body**: (any combination of)
    ```json
    {
      "firstName": "Updated",
      "lastName": "Name",
      "DOB": "02-02-2001"
    }
    ```
  - **Response**: `Friend with the email updated.`

- `DELETE /friends/:email`
  - **Description**: Delete a friend by email.
  - **Path Parameter**: `email` (e.g., `johnsmith@gmail.com`)
  - **Response**: `Friend with the email deleted.`

## 🙏 Credits

This project was originally forked from the IBM Developer Skills Network.

- **Original Author**: IBM Developer Skills Network (https://github.com/ibm-developer-skills-network)
- **Forked by**: rafael-a-g-n (https://github.com/rafael-a-g-n)

## 📄 License

This project is licensed under the Apache License 2.0. See the `LICENSE` file for details.
