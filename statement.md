# Problem Statement

## Problem Statement
Small libraries (school, college department, or community libraries) often
track books and their issue/return status manually using registers or
spreadsheets. This is error-prone, makes it hard to know which books are
currently available, and makes it easy to forget late fines. This project
builds a simple console-based Java application to manage the book catalog
and handle issuing/returning books with automatic fine calculation.

## Scope of the Project
The system covers:
- Adding, updating, deleting, and searching books in the catalog
- Registering members
- Issuing a book to a member and recording the due date
- Returning a book and calculating a late fine if overdue
- Viewing issue history for a member or a book

Out of scope: online reservations, email/SMS notifications, multi-branch
library support, and a graphical user interface (may be considered as
future enhancements).

## Target Users
- **Librarian** — manages the book catalog and oversees issue/return records
- **Member** — searches the catalog and issues/returns books

## High-Level Features
1. Role-based login (Librarian / Member)
2. Book catalog management (CRUD)
3. Issue and return workflow with due dates
4. Automatic fine calculation for overdue returns
5. Issue history tracking
