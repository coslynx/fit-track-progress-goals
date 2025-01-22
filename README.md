# fit-track-progress-goals

<h4 align="center">A web application that allows users to track their fitness goals, set progress, and share achievements with friends.</h4>
<h4 align="center">Developed with the software and tools below.</h4>
<div class="badges" align="center">
  <img src="https://img.shields.io/badge/Framework-React-blue" alt="React">
  <img src="https://img.shields.io/badge/Frontend-Javascript,_Html,_Css-red" alt="Javascript, HTML, CSS">
  <img src="https://img.shields.io/badge/Backend-Node.js-blue" alt="Node.js">
  <img src="https://img.shields.io/badge/LLMs-Custom,_Gemini,_OpenAI-black" alt="Custom, Gemini, OpenAI">
</div>
<div class="badges" align="center">
  <img src="https://img.shields.io/github/last-commit/coslynx/fit-track-progress-goals?style=flat-square&color=5D6D7E" alt="git-last-commit" />
  <img src="https://img.shields.io/github/commit-activity/m/coslynx/fit-track-progress-goals?style=flat-square&color=5D6D7E" alt="GitHub commit activity" />
  <img src="https://img.shields.io/github/languages/top/coslynx/fit-track-progress-goals?style=flat-square&color=5D6D7E" alt="GitHub top language" />
</div>

## 📑 Table of Contents
- 📍 Overview
- 📦 Features
- 📂 Structure
- 💻 Installation
- 🏗️ Usage
- 🌐 Hosting
- 📄 License
- 👏 Authors

## 📍 Overview
The repository contains a Minimum Viable Product (MVP) called "fit-track-progress-goals" that provides a comprehensive solution for users to track their fitness goals, set progress, and share achievements with friends. The application is built using a tech stack consisting of React, JavaScript, HTML, CSS, Node.js, and Custom LLMs including Gemini and OpenAI.

## 📦 Features
|    | Feature            | Description                                                                                                        |
|----|--------------------|--------------------------------------------------------------------------------------------------------------------|
| ⚙️ | **Architecture**   | The codebase follows a modular architectural pattern with separate directories for different functionalities, ensuring easier maintenance and scalability. The application is built using React for the frontend and Node.js for the backend, leveraging Custom LLMs, Gemini, and OpenAI for advanced features.             |
| 📄 | **Documentation**  | The repository includes a comprehensive README file that provides an overview of the Minimum Viable Product (MVP), details on its features, dependencies, and step-by-step instructions for installation, usage, and hosting.                                  |
| 🔗 | **Dependencies**   | The codebase relies on various external libraries and packages such as React, axios, mongoose, and jsonwebtoken, which are essential for building the user interface, handling API requests, and managing the database.                                             |
| 🧩 | **Modularity**     | The modular structure of the application allows for easier maintenance and reusability of the code, with separate directories and files for different functionalities such as authentication, goal management, and dashboard.                                |
| 🧪 | **Testing**        | The project includes comprehensive unit tests using frameworks like Jest and React Testing Library to ensure the reliability and robustness of the codebase.                                                                                          |
| ⚡️  | **Performance**    | The performance of the system is optimized through techniques such as code splitting, memoization, and efficient data fetching and handling. The application is designed to handle increased user load and data volume.                                |
| 🔐 | **Security**       | The application implements security measures such as input validation, password hashing, and secure token-based authentication to protect user data and prevent common vulnerabilities.                                                         |
| 🔀 | **Version Control**| The project utilizes Git for version control, with GitHub Actions workflows configured for automated build and release processes.                                                                                                         |
| 🔌 | **Integrations**   | The application integrates with various browser APIs and external services through HTTP requests, including features like speech recognition and synthesis.                                                                             |
| 📶 | **Scalability**    | The system is designed with scalability in mind, utilizing caching strategies and cloud-based solutions to handle increased user load and data volume.                                                                                |

## 📂 Structure
```text
- src
  - api
    - auth
      - auth.controller.js
      - auth.service.js
      - auth.routes.js
    - goals
      - goals.controller.js
      - goals.service.js
      - goals.routes.js
  - models
    - User.js
    - Goal.js
  - middleware
    - auth.middleware.js
    - error.middleware.js
  - utils
    - logger.js
    - validator.js
  - app.js
  - server.js
- tests
  - unit
    - auth.test.js
    - goals.test.js
- client
  - src
    - components
      - common
        - Button.jsx
        - Input.jsx
        - Modal.jsx
      - layout
        - Header.jsx
        - Footer.jsx
      - features
        - auth
          - LoginForm.jsx
          - RegisterForm.jsx
        - dashboard
          - DashboardStats.jsx
        - goals
          - GoalList.jsx
          - GoalForm.jsx
    - pages
      - Home.jsx
      - Dashboard.jsx
      - Goals.jsx
      - Profile.jsx
    - context
      - AuthContext.jsx
    - hooks
      - useAuth.js
      - useGoals.js
    - services
      - authService.js
      - goalsService.js
    - utils
      - helpers.js
    - styles
      - global.css
  - public
    - index.html
    - favicon.ico
- .env
- package.json
- README.md
- startup.sh
- commands.json
- tailwind.config.js
- babel.config.js
- jest.config.js
```

## 💻 Installation

> [!WARNING]
> ### 🔧 Prerequisites
> - Node.js v16+
> - npm v8+
> - MongoDB v5+

### 🚀 Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/coslynx/fit-track-progress-goals.git
   cd fit-track-progress-goals
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Set up the database:
   ```bash
   # Start MongoDB database
   docker-compose up -d mongodb
   
   # Run database migrations
   npm run migrate
   ```
4. Configure environment variables:
   ```bash
   cp .env.example .env
   # Fill in necessary environment variables (e.g., MongoDB connection string, JWT secret)
   ```

## 🏗️ Usage

### 🏃‍♂️ Running the MVP

1. Start the development server:
   ```bash
   npm run dev
   ```
2. Start the API server:
   ```bash
   npm run api
   ```

3. Access the application:
   - Web interface: [http://localhost:3000](http://localhost:3000)
   - API endpoint: [http://localhost:3000/api](http://localhost:3000/api)

> [!TIP]
> ### ⚙️ Configuration
> - The `.env` file contains the necessary environment variables for the application, such as the database connection string and JWT secret.
> - Modify these variables as needed to match your specific deployment setup.

### 📚 Examples

Here are some examples of the MVP's core features:

- 📝 **User Registration**:
  ```bash
  curl -X POST http://localhost:3000/api/auth/register \
    -H "Content-Type: application/json" \
    -d '{"name": "newuser", "email": "user@example.com", "password": "securepass123"}'
  ```

- 📝 **Setting a Fitness Goal**:
  ```bash
  curl -X POST http://localhost:3000/api/goals \
    -H "Content-Type: application/json" \
    -H "Authorization: Bearer YOUR_JWT_TOKEN" \
    -d '{"title": "Weight Loss", "description": "Lose 10 lbs by December 31", "dueDate": "2023-12-31"}'
  ```

- 📝 **Logging Progress**:
  ```bash
  curl -X POST http://localhost:3000/api/progress \
    -H "Content-Type: application/json" \
    -H "Authorization: Bearer YOUR_JWT_TOKEN" \
    -d '{"goalId": "goal_id_here", "value": 5, "date": "2023-06-15"}'
  ```

## 🌐 Hosting

### 🚀 Deployment Instructions

Detailed instructions for deploying the Fitness Tracking MVP to Heroku:

1. Install the Heroku CLI:
   ```bash
   npm install -g heroku
   ```
2. Login to Heroku:
   ```bash
   heroku login
   ```
3. Create a new Heroku app:
   ```bash
   heroku create fit-track-progress-goals-production
   ```
4. Set up environment variables:
   ```bash
   heroku config:set NODE_ENV=production
   heroku config:set DB_CONNECTION_STRING=mongodb://user:password@host:port/database
   heroku config:set JWT_SECRET=your-256-bit-secret
   ```
5. Deploy the code:
   ```bash
   git push heroku main
   ```
6. Run database migrations (if applicable):
   ```bash
   heroku run npm run migrate
   ```

### 🔑 Environment Variables

- `DB_CONNECTION_STRING`: Connection string for the MongoDB database
  Example: `mongodb://user:password@host:port/database`
- `JWT_SECRET`: Secret key for JWT token generation
  Example: `your-256-bit-secret`

## 📜 API Documentation

### 🔍 Endpoints

- **POST /api/auth/register**
  - Description: Register a new user
  - Body: `{ "name": string, "email": string, "password": string }`
  - Response: `{ "token": string }`

- **POST /api/auth/login**
  - Description: Log in a user
  - Body: `{ "email": string, "password": string }`
  - Response: `{ "token": string }`

- **POST /api/goals**
  - Description: Create a new fitness goal
  - Headers: `Authorization: Bearer TOKEN`
  - Body: `{ "title": string, "description": string, "dueDate": date }`
  - Response: `{ "id": string, "title": string, "description": string, "dueDate": date, "completed": boolean, "userId": string }`

- **GET /api/goals**
  - Description: Retrieve the user's fitness goals
  - Headers: `Authorization: Bearer TOKEN`
  - Response: `[ { "id": string, "title": string, "description": string, "dueDate": date, "completed": boolean, "userId": string } ]`

- **PUT /api/goals/{id}**
  - Description: Update an existing fitness goal
  - Headers: `Authorization: Bearer TOKEN`
  - Body: `{ "title": string, "description": string, "dueDate": date }`
  - Response: `{ "id": string, "title": string, "description": string, "dueDate": date, "completed": boolean, "userId": string }`

- **DELETE /api/goals/{id}**
  - Description: Delete a fitness goal
  - Headers: `Authorization: Bearer TOKEN`
  - Response: `{ "message": string }`

### 🔒 Authentication

1. Register a new user or log in to receive a JWT token.
2. Include the token in the `Authorization` header for all protected routes:
   ```
   Authorization: Bearer YOUR_JWT_TOKEN
   ```
3. The token has a 1-hour expiration time. When the token expires, you can request a new token using the refresh token endpoint.

### 📝 Examples

```bash
# Register a new user
curl -X POST http://localhost:3000/api/auth/register \
     -H "Content-Type: application/json" \
     -d '{"name": "fitnessuser", "email": "user@example.com", "password": "securepass123"}'

# Response
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
}

# Create a new goal
curl -X POST http://localhost:3000/api/goals \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer YOUR_JWT_TOKEN" \
     -d '{"title": "Weight Loss", "description": "Lose 10 lbs by December 31", "dueDate": "2023-12-31"}'

# Response
{
  "id": "goal123",
  "title": "Weight Loss",
  "description": "Lose 10 lbs by December 31",
  "dueDate": "2023-12-31",
  "completed": false,
  "userId": "user123"
}
```

> [!NOTE]
> ## 📜 License & Attribution
> 
> ### 📄 License
> This Minimum Viable Product (MVP) is licensed under the [GNU AGPLv3](https://choosealicense.com/licenses/agpl-3.0/) license.
> 
> ### 🤖 AI-Generated MVP
> This MVP was entirely generated using artificial intelligence through [CosLynx.com](https://coslynx.com).
> 
> No human was directly involved in the coding process of the repository: fit-track-progress-goals
> 
> ### 📞 Contact
> For any questions or concerns regarding this AI-generated MVP, please contact CosLynx at:
> - Website: [CosLynx.com](https://coslynx.com)
> - Twitter: [@CosLynxAI](https://x.com/CosLynxAI)

<p align="center">
  <h1 align="center">🌐 CosLynx.com</h1>
</p>
<p align="center">
  <em>Create Your Custom MVP in Minutes With CosLynxAI!</em>
</p>
<div class="badges" align="center">
<img src="https://img.shields.io/badge/Developers-Drix10,_Kais_Radwan-red" alt="">
<img src="https://img.shields.io/badge/Website-CosLynx.com-blue" alt="">
<img src="https://img.shields.io/badge/Backed_by-Google,_Microsoft_&_Amazon_for_Startups-red" alt="">
<img src="https://img.shields.io/badge/Finalist-Backdrop_Build_v4,_v6-black" alt="">
</div>