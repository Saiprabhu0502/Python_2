## Library Management System

This Python script implements a basic library management system using object-oriented programming principles. The system allows for the management of books, borrowers, and their interactions within a library context.

### Classes

#### 1. Book

The `Book` class represents a book in the library with the following attributes:
- `title`: Title of the book.
- `author`: Author of the book.
- `isbn`: ISBN (International Standard Book Number) of the book.
- `genre`: Genre or category of the book.
- `quantity`: Number of copies available in the library.

**Methods:**
- `__init__(self, title, author, isbn, genre, quantity)`: Initializes a new book object with specified attributes.
- `update(self, title=None, author=None, quantity=None)`: Updates the book's attributes if specified.
- `__str__(self)`: Returns a string representation of the book.

#### 2. Borrower

The `Borrower` class represents a library borrower with the following attributes:
- `name`: Name of the borrower.
- `contact`: Contact information of the borrower.
- `membership_id`: Unique identifier for the borrower.

**Methods:**
- `__init__(self, name, contact, membership_id)`: Initializes a new borrower object with specified attributes.
- `update(self, name=None, contact=None)`: Updates the borrower's attributes if specified.
- `__str__(self)`: Returns a string representation of the borrower.

#### 3. Library

The `Library` class manages the collection of books, borrowers, and their interactions within the library.

**Attributes:**
- `books`: Dictionary storing books with ISBN as keys.
- `borrowers`: Dictionary storing borrowers with membership IDs as keys.
- `borrowed_books`: Dictionary tracking borrowed books by borrowers.

**Methods:**
- Book Management:
  - `add_book(self, book)`: Adds a new book to the library.
  - `update_book(self, isbn, title=None, author=None, quantity=None)`: Updates existing book information.
  - `remove_book(self, isbn)`: Removes a book from the library.
  
- Borrower Management:
  - `add_borrower(self, borrower)`: Adds a new borrower to the library.
  - `update_borrower(self, membership_id, name=None, contact=None)`: Updates existing borrower information.
  - `remove_borrower(self, membership_id)`: Removes a borrower from the library.
  
- Book Borrowing and Returning:
  - `borrow_book(self, membership_id, isbn, due_date)`: Allows a borrower to borrow a book.
  - `return_book(self, membership_id, isbn)`: Allows a borrower to return a borrowed book.
  
- Search and Display:
  - `search_books(self, title=None, author=None, genre=None)`: Searches books by title, author, or genre.
  - `display_books(self)`: Displays all books in the library.
  - `display_borrowers(self)`: Displays all borrowers in the library.


### Flow of Methods

1. **Initialization**: Instantiate a `Library` object.
2. **Adding Data**: Use `add_book()` and `add_borrower()` methods to populate the library with books and borrowers.
3. **Managing Data**: Use methods like `borrow_book()`, `return_book()`, `update_book()`, `update_borrower()`, `remove_book()`, and `remove_borrower()` to manage books and borrowers.
4. **Searching**: Use `search_books()` to find books based on title, author, or genre.
5. **Displaying**: Use `display_books()` and `display_borrowers()` to see all books and borrowers currently in the library.

