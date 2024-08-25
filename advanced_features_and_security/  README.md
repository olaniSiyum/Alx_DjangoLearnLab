# Permissions and Groups Setup

This application uses Django's permissions and groups to control access to user data.

## Groups

- **Editors**: Can view and edit user data.
- **Viewers**: Can only view user data.
- **Admins**: Can view, create, edit, and delete user data.

## Permissions

Custom permissions are defined in the `CustomUser` model:

- `can_view`: Allows viewing of user data.
- `can_create`: Allows creation of new user instances.
- `can_edit`: Allows editing of existing user data.
- `can_delete`: Allows deletion of user instances.

## Views

The following views are protected by these permissions:

- `user_list`: Requires `can_view` permission.
- `edit_user`: Requires `can_edit` permission.

# LibraryProject

This is a Django project called `LibraryProject` that includes an app named `bookshelf`.

## Project Structure

- `bookshelf/`: Contains the core application files for managing books.
- `bookshelf/models.py`: Defines the `Book` model for storing book information.
- `bookshelf/views.py`: Contains views like `book_list` to display books.
- `bookshelf/urls.py`: URL routing for the `bookshelf` app.

## Features

- **Book Management**: Add, edit, and view books in the library.
- **Custom User Model**: A custom user model is implemented for managing user data.
- **Permissions and Groups**: Implemented permissions and groups to control access to different parts of the application.

## Setup

1. Clone the repository.
2. Install the dependencies.
3. Run the migrations.
4. Start the development server.

## Usage

- Access the book list at `/books/`.
- Admin users can manage books via the Django admin interface.

