# Book Management App

A simple RESTful API for managing books, users, and borrowing functionality. This application allows users to add, update, delete, and search for books, as well as manage borrowing and returning of books.

## Features

•⁠  ⁠User registration and login
•⁠  ⁠Add, update, delete, and view books
•⁠  ⁠Search for books by title or author
•⁠  ⁠Borrow and return books

## Technologies Used

•⁠  ⁠Node.js
•⁠  ⁠Express.js
•⁠  ⁠MongoDB
•⁠  ⁠Mongoose
•⁠  ⁠JWT for authentication
•⁠  ⁠Bcrypt for password hashing
•⁠  ⁠dotenv for environment variable management

## Installation

1.⁠ ⁠Clone the repository:

   bash
   git clone https://github.com/sidd1603/Book_Management_App
   
   cd book-management-app
   

2.⁠ ⁠Install the dependencies:

   bash
   npm install
   
3.⁠ ⁠.env file
    
   No need to change anything(Mongo_url already exists)
 

## Usage

1.⁠ ⁠Start the server:

   bash
   npm start or node server.js or nodemon server.js
   

2.⁠ ⁠The API will be running on http://localhost:8080.

## API Endpoints

### User Routes

•⁠  ⁠POST /api/register - Register a new user
In body (json format)
{
  "username": "testuser",
  "password": "password123"
}

•⁠  ⁠POST /api/login - Log in an existing user
{
  "username": "testuser",
  "password": "password123"
}


### Book Routes

•⁠  ⁠POST /api/books - Add a new book
{
  "title": "Harry Potter",
  "author": "J.K. Rowling",
  "genre": "Fantasy",
  "publishedYear": 1997
}
•⁠  ⁠GET /api/books - View all books
•⁠  ⁠GET /api/books/search - Search for books by title or author
•⁠  ⁠PUT /api/books/:id - Update a book by ID
{
  "title": "Harry",
}

•⁠  ⁠DELETE /api/books/:id - Delete a book by ID

### Borrow Routes

•⁠  ⁠POST /api/borrow - Borrow books
{
  "userId": "user_id_here",
  "bookIds": ["book_id_here"]
}

•⁠  ⁠POST /api/return - Return borrowed books
{
  "userId": "user_id_here",
  "bookIds": ["book_id_here"]
}

•⁠  ⁠GET /api/borrowed/:userId - Get borrowed books for a user
