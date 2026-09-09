# Library Management System (Java, Console-Based)

## Overview
A simple console-based Library Management System built in core Java. It lets
a Librarian manage a book catalog and lets Members issue and return books,
with automatic fine calculation for late returns. Data is stored in plain
text files, so no database setup is required.

## Features
- Login as Librarian or Member (role-based menu)
- Add, update, delete, and search books (CRUD)
- Issue a book to a member and return it
- Automatic fine calculation for late returns
- View issue history
- Data persisted to text files (no database needed)

## Technologies / Tools Used
- Core Java (JDK 17 or any recent version)
- File I/O (java.io / java.nio) for data persistence
- Collections (ArrayList, HashMap) for in-memory management
- No external libraries or frameworks required

## Project Structure
```
src/
 ├── Book.java             - Model class for a book
 ├── Member.java           - Model class for a library member
 ├── Librarian.java        - Model class for the librarian (admin) user
 ├── LibraryException.java - Custom checked exception for library errors
 ├── FileStorage.java      - Handles reading/writing books & members to file (Singleton)
 ├── LibraryService.java   - Core business logic (add/search/issue/return/fine)
 └── Main.java             - Console menu, application entry point
data/
 ├── books.txt             - Stores book records (created automatically)
 └── members.txt           - Stores member records (created automatically)
```

## Steps to Install & Run
1. Make sure Java (JDK 17+) is installed:
   ```
   java -version
   ```
2. Navigate to the project folder and compile:
   ```
   cd library-management-system
   javac -d out src/*.java
   ```
3. Run the application:
   ```
   java -cp out Main
   ```
4. Follow the on-screen menu to log in as Librarian or Member and use the system.

## Instructions for Testing
- Manually test each menu option: add book, search book, issue book, return
  book (try returning after the due date to see the fine calculated), delete
  book, and view issue history.
- Test error handling by entering an invalid ISBN, trying to issue a book
  with zero copies available, or searching for a book that doesn't exist —
  the system should show a clear error message instead of crashing.
- (Optional) Add JUnit if you want automated tests for `LibraryService`
  methods like fine calculation and availability checks.
