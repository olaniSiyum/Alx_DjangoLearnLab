# Create Operation

## Python Command
```python
from bookshelf.models import Book

# Creating a Book instance
book = Book.objects.create(title="1984", author="George Orwell", publication_year=1949)
book.save()
## Expected Output
>>> book
<Book: 1984>

# Retrieve Operation
# Retrieving the created book
book = Book.objects.get(title="1984")
print(book.title, book.author, book.publication_year)

## Expected Output
1984 George Orwell 1949

# Updating the title of the book
book.title = "Nineteen Eighty-Four"
book.save()
## Expected Output
>>> book
<Book: Nineteen Eighty-Four>

# Deleting the book instance
book.delete()

# Verifying the deletion by trying to retrieve all books
books = Book.objects.all()
print(books)
## Expected Output
>>> books
<QuerySet []>