### Spaceship Travel System API

---

#### Introduction:
Welcome to the Spaceship Travel System API! This API is designed to manage the operations of a spaceship travel system, facilitating the booking of missions to destinations like Moon, Mars, and Jupiter. This README provides instructions on how to run the API locally and interact with its endpoints.

---
## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [API Endpoints](#api-endpoints)
- [Examples](#examples)
- [Database Schema](#database-schema)
- [API Documentation](#api-documentation)
- [Additional Notes](#additional-notes)
  
---
## Features

- Create, read, update, and delete spaceships
- Manage crew members and assign them to spaceships
- Schedule and monitor missions to various destinations
- Session management for user authentication
---

#### Technologies Used:
- Node.js
- Express.js
- MySQL
- Postman (for API testing)

---

#### Installation:

1. **Clone the Repository:**

      ```bash
      git clone https://github.com/your-username/spaceship-travel-system-api.git


2. **Install Dependencies:**

    ```bash
    cd spaceship-travel-system-api
    npm install



3. **Database Setup:**
- Make sure you have MySQL installed and running on your local machine.
- Create a new database named `spaceship_travel_system`.
- Import the database schema from the `database/schema.sql` file.

4. **Environment Variables:**
- Create a `.env` file in the root directory.
- Add the following environment variables:
  ```
  DB_HOST=localhost
  DB_USER=root
  DB_PASSWORD=your_password
  DB_DATABASE=spaceship_travel_system
  ```

5. **Start the Server:**
   ```bash
   npm start


6. **Accessing the API:**
- The API server will start running on `http://localhost:3000`.
- You can now send requests to the API endpoints using tools like Postman or directly from your application.

---

#### API Endpoints:
- **Spaceships:**
- `GET /spaceships`: Retrieve a list of all spaceships.
- `POST /spaceships`: Add a new spaceship.
- `GET /spaceships/:id`: Retrieve a single spaceship by ID.
- `PUT /spaceships/:id`: Update a spaceship's information.
- `PATCH /spaceships/:id`: Partially update a spaceship's information.
- `DELETE /spaceships/:id`: Delete a spaceship.

- **Crew Members:**
- `GET /crewmembers`: Retrieve a list of all crew members.
- `POST /crewmembers`: Add a new crew member.
- `GET /crewmembers/:id`: Retrieve a single crew member by ID.
- `PUT /crewmembers/:id`: Update a crew member's information.
- `PATCH /crewmembers/:id`: Partially update a crew member's information.
- `DELETE /crewmembers/:id`: Delete a crew member.

- **Missions:**
- `GET /missions`: Retrieve a list of all missions.
- `POST /missions`: Add a new mission.
- `GET /missions/:id`: Retrieve a single mission by ID.
- `PUT /missions/:id`: Update a mission.
- `PATCH /missions/:id`: Partially update a mission.
- `DELETE /missions/:id`: Delete a mission.

---
#### Examples:
1.**Adding a New Spaceship:**

    ```json
    POST /api/v1/spaceships
    Content-Type: application/json

    {
        "name": "Apollo 11",
        "capacity": 6,
        "launch_date": "2025-07-20T14:00:00.000Z",
        "status": "Active"
    }


2.**Retrieving All Crew Members:**

    ```json
    GET /api/v1/crewmembers


3.**Creating a New Mission:**
    
    ```json
    POST /api/v1/missions
    Content-Type: application/json

    {
        "spaceship_id": 1,
        "destination": "Mars",
        "launch_date": "2026-04-15T10:30:00.000Z",
        "duration": 720
    }


---
#### Database Schema:
- ![Database Schema](path_to_your_database_schema_image)

---
#### API Documentation:
[API Documentation In Postman](https://speeding-capsule-4673.postman.co/workspace/spaceship-travel-system~8b5586ca-b582-48c0-a707-acfd90349d90/collection/29726783-6d90a496-bb16-4fdf-97b8-52a69c88d179?action=share&creator=29726783)


---

#### Additional Notes:
- Make sure to replace `your_password` in the `.env` file with your actual MySQL password.
- Error handling is implemented to handle various scenarios such as invalid requests, database errors, etc.




---

