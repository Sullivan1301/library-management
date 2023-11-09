# Library API OpenAPI Specification

This OpenAPI spec defines the Library API, allowing you to manage books and authors.

## API Details

- **Title:** Library API
- **Version:** 1.1.0
- **Description:** STD22048 - STD22005
- **Base URL:** [https://library.com](https://library.com)

## Endpoints

### Books

- **GET /books**: Retrieve all books. The returned books are ordered by updated datetime.
- **PUT /books**: Create or update a list of books.

### Authors

- **GET /authors**: Retrieve all authors. Filter authors by name.
- **PUT /authors**: Create or update a list of authors.
- **DELETE /authors**: Delete an author by name.
- **GET /authors/page/{page}/size/{size}**: Retrieve authors with pagination.

### Books and Authors Relations

- **PUT /books/{bookId}/authors/{authorId}**: Update the author of a book. 
- **PUT /books/authors**: Update authors for books.
  
### Import
- **POST /books/import**: Return the list of imported books in JSON or Excel
- **POST /authors/import**: Return the list of imported auhors in JSON or Excel
## Data Schemas

- **Book**: `id`, `bookName`, `author` (Reference), `pageNumbers`, `topic`, `releaseDate`
- **Author**: `id`, `name`, `sex` (M/F)
- **crupdateBook**: `id`, `bookName`, `pageNumbers`, `topic`, `releaseDate`
- **updateAuthorBook**: `bookId`, `authorId`

## Usage

Interact with the API via HTTP clients or explore it in [Swagger UI](https://petstore.swagger.io/?url=https://raw.githubusercontent.com/Sullivan1301/library-management/OAS-TD4-STD22048-STD22005/docs/api.yml).
