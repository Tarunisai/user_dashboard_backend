# User Management REST API

A backend REST API to manage users with CRUD operations (Create, Read, Update, Delete).
Built using **Node.js** + **Express** and connected to a **SQLite database**.
 ---

## Folder Structure
backend/
├── routes/
│   └── users.js
├── database.js
├── server.js
├── package.json
├── package-lock.json
├── .gitignore
└── users.db

---

## Live Deployment

[The backend API is live at:
https://your-backend-on-render.onrender.com/api/users]

---

## API Endpoints
### 1. Get All Users
- URL: /api/users
- Method: GET
- Live Example: All Users
Response Example:
[
  {
    "id": 1,
    "name": "Taruni",
    "email": "taruni@example.com",
    "phone": "7093659787",
    "company": "Forty4 Technologies",
    "street": "Dolphin Street",
    "city": "Hyderabad",
    "zipcode": "567987",
    "lat": "12",
    "lng": "11"
  }
]


Screenshot Placeholder:
![All Users Screenshot](./screenshots/get_all_users.png)

### 2. Get Single User

- URL: /api/users/:id
- Method: GET
- Example:
GET https://your-backend-on-render.onrender.com/api/users/1

Response Example:

{
  "id": 1,
  "name": "Taruni",
  "email": "taruni@example.com",
  "phone": "7093659787",
  "company": "Forty4 Technologies",
  "street": "Dolphin Street",
  "city": "Hyderabad",
  "zipcode": "567987",
  "lat": "12",
  "lng": "11"
}


Screenshot Placeholder:
![Single User Screenshot](./screenshots/get_single_user.png)

### 3. Create a New User

- URL: /api/users
- Method: POST
- Request Body (JSON):
{
  "name": "John Doe",
  "email": "john@example.com",
  "phone": "9876543210",
  "company": "Example Inc",
  "street": "Main Street",
  "city": "CityName",
  "zipcode": "123456",
  "lat": "10",
  "lng": "20"
}

Response Example:

{
  "message": "User created successfully",
  "id": 2
}


Screenshot Placeholder:
![Create User Screenshot](./screenshots/create_user.png)

### 4. Update a User

- URL: /api/users/:id
- Method: PUT
- Request Body (JSON):
{
  "name": "John Updated",
  "email": "john.updated@example.com",
  "phone": "9876543210",
  "company": "Updated Inc",
  "street": "Main Street",
  "city": "CityName",
  "zipcode": "123456",
  "lat": "10",
  "lng": "20"
}


Response Example:

{
  "message": "User updated successfully"
}


Screenshot Placeholder:
![Update User Screenshot](./screenshots/update_user.png)

### 5. Delete a User

- URL: /api/users/:id
- Method: DELETE
- Response Example:
{
  "message": "User deleted successfully"
}

Screenshot Placeholder:
![Delete User Screenshot](./screenshots/delete_user.png)

---

## Notes

- Address fields are stored as separate columns (street, city, zipcode, lat, lng) in SQLite.

- CORS is enabled for frontend integration.

- Proper HTTP status codes and validations are implemented.

---


## .env.example
- PORT=8081
