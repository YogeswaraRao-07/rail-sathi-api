# Rail Sathi Complaint Microservice

This is a FastAPI-based microservice for handling passenger complaints in Indian Railways. 
It supports complaint creation, media file uploads, updates, deletion, and train detail lookup. 
It is containerized using Docker and uses PostgreSQL for persistent storage.

---

## Technologies Used

- **FastAPI**
- **PostgreSQL**
- **Docker & Docker Compose**
- **Psycopg2**
- **Uvicorn**
- **Threading & Async File Handling**

---

## How to Run

1. Clone the Repo
   
2.Create a .env file and include:
  POSTGRES_USER=postgres
  POSTGRES_PASSWORD=postgres
  POSTGRES_DB=railsathidb
  MAIL_USERNAME=your-email@gmail.com
  MAIL_PASSWORD=your-app-password
  MAIL_FROM=your-email@gmail.com

3. Start the App with Docker
  docker-compose up --build
  Wait until Uvicorn running on http://0.0.0.0:8000 appears in the terminal.

API Endpoints
Swagger UI:
  http://localhost:8000/rs_microservice/docs

Health Check:
  http://localhost:8000/health

Sample Routes:

GET	/rs_microservice/complaint/get/{complain_id}	Fetch a complaint by ID
POST	/rs_microservice/complaint/add	Submit a new complaint
PATCH	/rs_microservice/complaint/update/{complain_id}	Partially update a complaint
DELETE	/rs_microservice/complaint/delete/{complain_id}	Delete a complaint
GET	/rs_microservice/train_details/{train_no}	Get train, depot, division, zone
