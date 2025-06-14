This repository contains the MongoDB assignment for Week 1, focusing on MongoDB fundamentals and advanced techniques.

## Database Information
- **Database Name**: `plp_bookstore`
- **Collection Name**: `books`
- **Connection URI**: `mongodb://localhost:27017`

## Prerequisites

1. **MongoDB Installation**
   - MongoDB Community Edition installed locally
   - MongoDB Compass (GUI tool) installed
   - MongoDB Shell (mongosh) installed

2. **Node.js Requirements**
   - Node.js installed (v14 or higher)
   - MongoDB Node.js driver installed

## Setup Instructions

1. **Verify MongoDB Installation**
   ```bash
   mongod --version
   mongosh --version
   ```

2. **Install Dependencies**
   ```bash
   npm install mongodb
   ```

3. **Database Setup**
   - MongoDB should be running as a service
   - Database `plp_bookstore` will be created automatically
   - Collection `books` will be created automatically

4. **Running the Scripts**

   a. First, populate the database with sample data:
   ```bash
   node insert_books.js
   ```
   Expected output:
   ```
   Connected to MongoDB server
   12 books were successfully inserted into the database
   ```

   b. To run the queries, use MongoDB Shell (mongosh):
   ```bash
   mongosh
   use plp_bookstore
   ```
   Then copy and paste the queries from `queries.js`

   c. To view data in MongoDB Compass:
   - Open MongoDB Compass
   - Connect to: `mongodb://localhost:27017`
   - Navigate to `plp_bookstore` database
   - Click on `books` collection

## Assignment Tasks

1. **Basic CRUD Operations**
   - Finding books by genre, publication year, and author
   - Updating book prices
   - Deleting books by title

2. **Advanced Queries**
   - Finding books in stock published after 2010
   - Using projection to show specific fields
   - Sorting books by price
   - Implementing pagination

3. **Aggregation Pipeline**
   - Calculating average price by genre
   - Finding author with most books
   - Grouping books by publication decade

4. **Indexing**
   - Creating indexes for performance optimization
   - Demonstrating performance improvements

## Files in this Repository

- `insert_books.js`: Script to populate the database with sample book data
- `queries.js`: Contains all MongoDB queries for the assignment tasks
- `README.md`: This file, containing setup and running instructions

## Sample Data Structure
Each book document contains:
```javascript
{
    title: String,
    author: String,
    genre: String,
    published_year: Number,
    price: Number,
    in_stock: Boolean,
    pages: Number,
    publisher: String
}
```

## Troubleshooting

1. **MongoDB Connection Issues**
   - Ensure MongoDB service is running
   - Check if port 27017 is available
   - Verify MongoDB installation

2. **Script Execution Issues**
   - Ensure Node.js is installed
   - Check if mongodb package is installed
   - Verify you're in the correct directory

3. **Query Issues**
   - Ensure you're connected to the correct database
   - Verify collection name is correct
   - Check query syntax

## Submission Requirements

1. **Required Files**
   - `insert_books.js` (with your modifications if any)
   - `queries.js` (containing all MongoDB queries)
   - `README.md` (this file)
   - Screenshot of MongoDB Compass showing your collections and sample data

2. **Screenshot Requirements**
   - Place your screenshot in the `screenshots` directory
   - Name it `mongodb-compass-view.png` or similar
   - Show the `plp_bookstore` database
   - Show the `books` collection
   - Display at least 5 sample documents

## Resources

- [MongoDB Documentation](https://docs.mongodb.com/)
- [MongoDB University](https://university.mongodb.com/)
- [MongoDB Node.js Driver](https://mongodb.github.io/node-mongodb-native/) 
- [MongoDB Compass Documentation](https://docs.mongodb.com/compass/)
