This is a RESTful API for managing user registration, authentication, and diary entries for a travel diary platform.

Setup Instructions
Clone the repository:
PS C:\Users\gg\OneDrive\Desktop\travel-diary-1> 
cd server
Install Dependencies:
npm install
Initialize the database and start the server:
npm start
Usage
User Registration
Endpoint: POST /register
Request Body:
{
"username": "userb@example.com",
"password": "secretpassword"
}
Response:
{
  "message": "User registered successfully"
}
User Login
Endpoint: POST /login
Request Body:
{
"username": "userb@example.com",
"password": "secretpassword"
}
Response:
{
"accessToken": "your_access_token_here"
}

Diary Entries CRUD operations
Create Diary Entry
Endpoint: POST /diary-entries
Authorization Header: Bearer {accessToken}
You can replace placeholders like {accessToken} and {id}
Request Body:
{
"title": "Meeting",
"description": "Developer Meeting",
"location": "chennai"
}
Response:
{
"message": "Diary entry created successfully",
"id": 1
}
Get All Diary Entries
Endpoint: GET /diary-entries
Authorization Header: Bearer {accessToken}
Response:
[
{
  "id": 1,
  "title": "Meeting",
  "description": "Developer Meeting",
  "location": "chennai",
  "date": "2024-05-22T12:00:00.000Z"
}
]

Get Diary Entry by ID
Endpoint: GET /diary-entries/{id}
Authorization Header: Bearer {accessToken}
Update Diary Entry
Endpoint: PUT /diary-entries/{id}
Authorization Header: Bearer {accessToken}
Request Body:
{
{
"title": "goa",
"description": "first time",
"location": "Goa"
}  
}
Response:
{
"message": "Diary entry updated successfully"
}

Delete Diary Entry
Endpoint: DELETE /diary-entries/{id}
Authorization Header: Bearer {accessToken}
Response:
{
"message": "Diary entry deleted successfully"
}
