# Financial Risk Analytics System

## Project Title

**Financial Risk Analytics System**

## Project Description

Financial Risk Analytics System is a web-based application developed to manage and analyze financial information such as customers, accounts, and transactions.

The system provides APIs for managing financial data and implements secure user authentication and authorization using JSON Web Tokens (JWT). Protected API endpoints can be accessed only after successful authentication.

The application was developed and tested using sample and trial records entered directly into the database. The APIs were tested using Swagger UI, and the application was also tested through the frontend.

The main purpose of the project is to provide a structured platform for managing financial information and supporting financial risk-related operations.

## Technologies Used

### Backend

* Python
* FastAPI
* Uvicorn
* JSON Web Token (JWT)
* Python-JOSE

### Frontend

* HTML
* CSS
* JavaScript

### Database

* PostgreSQL
* pgAdmin
* MongoDB

### API Testing

* Swagger UI
* REST APIs

### Development Tools

* Visual Studio Code
* Git
* GitHub

## Installation / Setup

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/Financial-Risk-Analytics.git
cd Financial-Risk-Analytics
```

### 2. Create a Virtual Environment

For Windows:

```powershell
python -m venv venv
```

Activate the virtual environment:

```powershell
.\venv\Scripts\Activate.ps1
```

### 3. Install Required Dependencies

```powershell
pip install -r requirements.txt
```

### 4. Configure the Database

The application uses databases for storing application data.

Create a `.env` file in the project and configure the required database connection details and secret key.

Example:

```text
DATABASE_URL=your_database_connection
MONGO_URI=your_mongodb_connection
SECRET_KEY=your_secret_key
```

Replace the example values with the appropriate local database configuration.

**Do not upload the `.env` file to GitHub because it may contain database credentials and secret keys.**

## How to Run the Project

### Run the Backend

Activate the virtual environment:

```powershell
.\venv\Scripts\Activate.ps1
```

Start the FastAPI application:

```powershell
uvicorn main:app --reload
```

The backend will normally run at:

```text
http://127.0.0.1:8000
```

### Open Swagger UI

Open the following URL in a web browser:

```text
http://127.0.0.1:8000/docs
```

Swagger UI provides an interactive interface for viewing and testing the available APIs.

### Authentication and Authorization

1. Open the `/login` endpoint in Swagger UI.
2. Enter the required login credentials.
3. Execute the request.
4. A JWT access token is generated after successful authentication.
5. Click the **Authorize** button in Swagger UI.
6. Enter the generated token in the **HTTPBearer** authorization field.
7. Click **Authorize**.
8. Access the protected API endpoints.

### Authorization Testing

The protected endpoint:

```text
GET /customers
```

was tested using a valid JWT Bearer token.

The server successfully returned:

```text
200 OK
```

along with the customer records.

This confirms that the JWT-based authentication and authorization mechanism is working correctly.

## Screenshots / Results

Screenshots of the working project and API testing are included in the `screenshots` folder.

The screenshots include:

* Login page
* Swagger UI
* Successful login and JWT token generation
* Swagger HTTPBearer authorization
* Authorized `GET /customers` request
* Successful `200 OK` response
* Frontend application

### Authorization Test Result

```text
Login
  ↓
JWT Access Token Generated
  ↓
Swagger HTTPBearer Authorization
  ↓
GET /customers
  ↓
200 OK
  ↓
Customer Data Returned
```

### Result

The Financial Risk Analytics System was successfully developed and tested.

The login API successfully generated a JWT access token. The generated token was successfully used through Swagger UI to authorize access to protected API endpoints.

The protected `GET /customers` endpoint returned a **200 OK** response with customer records after valid authorization.

Therefore, the authentication and authorization functionality was successfully implemented and verified.


### Team Members

1. **utkalika** — 2510080004
2. **divya sri** — 2510080025
3. **Ambika Naidu** — 2510080035
4. **Kavitha Reddy** — 2510080033

## Academic Project

This project was developed as part of an academic/student project for educational and demonstration purposes.
