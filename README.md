# 🍹 APIRD: Drinks Management API

A robust RESTful API built with **Django 5.1** and **Django REST Framework** for managing a catalog of drinks. This project is structured for global scalability with extensive localization support.

---

## 📁 Project Structure
```text
APIRD/
├── APIRD/              # Project Configuration
│   ├── settings.py     # Global Settings
│   ├── urls.py         # Root URL Routing
│   ├── asgi.py         # ASGI configuration for deployment
│   └── wsgi.py         # WSGI configuration for deployment
├── Drinks/             # Main Application Logic
│   ├── migrations/     # Database Evolution files
│   ├── templates/      # HTML templates (e.g., index.html)
│   ├── models.py       # Database Schema
│   ├── serializers.py  # Data Serialization logic
│   ├── views.py        # API Request/Response Handling
│   └── admin.py        # Admin interface registration
├── venv/               # Virtual Environment & Django i18n Files
├── manage.py           # Django Admin Utility
└── db.sqlite3          # Local SQLite Database
Introduction to MongoDBConcepts: Understanding NoSQL vs. SQL databases, the document data model (JSON/BSON), and installing tools like MongoDB Compass and mongosh.  mongosh Example:JavaScript// Check your version and connection
db.version();
Database and Collection OperationsConcepts: Creating/dropping databases and managing collections (capped vs. uncapped).  mongosh Example:JavaScriptuse university_db; // Create/Switch to database[cite: 1]
db.createCollection("students"); // Create a collection[cite: 1]
show collections; // List all collections
CRUD Operations (Create, Read, Update, Delete)Concepts: Mastering the basic verbs of data management.  mongosh Example:JavaScript// Create[cite: 1]
db.students.insertOne({ name: "Alice", age: 22, major: "CS" }); 

// Read[cite: 1]
db.students.find({ name: "Alice" }); 

// Update[cite: 1]
db.students.updateOne({ name: "Alice" }, { $set: { age: 23 } }); 

// Delete[cite: 1]
db.students.deleteOne({ name: "Alice" }); 
Query Filtering and OperatorsConcepts: Using comparison ($gt, $lt), logical ($and, $or), and element operators.  mongosh Example:JavaScript// Find students older than 20 AND in the CS major[cite: 1]
db.students.find({ 
  $and: [
    { age: { $gt: 20 } }, 
    { major: "CS" }
  ] 
});
Sorting, Limiting, and Skipping DataConcepts: Implementing pagination and organizing query results.  mongosh Example:JavaScript// Sort by age descending, skip the first 5, and show the next 5[cite: 1]
db.students.find().sort({ age: -1 }).skip(5).limit(5); 
Aggregation Framework BasicsConcepts: Building pipelines with $match, $group, and $project.  mongosh Example:JavaScript// Count students per major[cite: 1]
db.students.aggregate([
  { $group: { _id: "$major", totalStudents: { $sum: 1 } } }
]);
Advanced MongoDB ConceptsConcepts: Indexing for performance, data modeling (Embedding vs. Referencing), and transactions.  mongosh Example:JavaScript// Create an index on the 'email' field to speed up searches[cite: 1]
db.students.createIndex({ email: 1 }, { unique: true });
