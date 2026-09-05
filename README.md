# MongoDB Library System

## 1. Introduction

MongoDB is a NoSQL document-oriented database that stores data in flexible JSON-like documents. This project demonstrates MongoDB concepts by creating a simple library management database.

## 2. Objectives

The objectives of this project are:

- Understand MongoDB and NoSQL concepts
- Understand document-based data models
- Create collections and documents
- Perform CRUD operations
- Search books and authors using MongoDB queries
- Understand the importance of NoSQL databases

## 3. Database Design

The database is named:

libraryDB

It contains three collections:

- books
- authors
- genres

## 4. Books Collection

Each book contains:

- title
- author
- genre
- year
- available

## 5. Authors Collection

Each author contains:

- name
- country
- birthYear

## 6. Genres Collection

Each genre contains:

- name
- description

## 7. CRUD Operations

### Create

MongoDB uses insertOne() and insertMany() to create documents.

Example:

db.books.insertOne({
  title: "The Alchemist",
  author: "Paulo Coelho",
  genre: "Fiction",
  year: 1988,
  available: true
});

### Read

Documents can be retrieved using find().

Example:

db.books.find();

### Update

Documents can be modified using updateOne().

Example:

db.books.updateOne(
  { title: "The Guide" },
  { $set: { available: true } }
);

### Delete

Documents can be removed using deleteOne().

Example:

db.books.deleteOne({
  title: "The Alchemist"
});

## 8. Search Queries

Books can be searched using title, author, genre, year and availability.

Authors can be searched using name, country and birth year.

## 9. MongoDB Data Model

MongoDB uses a document-oriented data model. Documents are stored in collections and use flexible schemas.

## 10. Advantages of NoSQL

- Flexible schema
- Easy horizontal scaling
- High performance
- Suitable for large amounts of data
- Handles semi-structured data
- Useful for modern web and mobile applications

## 11. Importance of NoSQL

NoSQL databases are important in modern applications because they can handle large volumes of rapidly changing and semi-structured data. They provide flexible data models and are suitable for applications that require scalability and high availability.

## 12. Project Structure

data/
├── books.json
├── authors.json
└── genres.json

queries/
└── library_queries.mongodb

README.md

## 13. Conclusion

This project demonstrates the fundamentals of MongoDB and NoSQL by implementing a library database containing books, authors and genres. CRUD operations and search queries were performed to understand how MongoDB manages document-based data. NoSQL systems are important for modern applications because of their flexibility, scalability and ability to handle large and changing datasets.