# CRUD API in Go

This project is a simple CRUD (Create, Read, Update, Delete) API built using Go and the [Gorilla Mux](https://github.com/gorilla/mux) router. The API manages a collection of movies, each with an ID, ISBN, title, and director information.

## Features

- **Get All Movies**: Retrieve a list of all movies.
- **Get a Single Movie**: Retrieve details of a specific movie by its ID.
- **Create a Movie**: Add a new movie to the collection.
- **Update a Movie**: Modify the details of an existing movie by its ID.
- **Delete a Movie**: Remove a movie from the collection by its ID.

## Prerequisites

- [Go](https://golang.org/) (version 1.24.1 or later)
- A terminal or command-line interface

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/israelowusu/crud_api_go.git
   cd crud_api_go
   ```

2. Install dependencies:
   ```sh
   go mod tidy
   ```

## Usage

1. Run the application:
   ```sh
   go run main.go
   ```

2. The server will start on port `8080`. You can interact with the API using tools like [Postman](https://www.postman.com/) or `curl`.

### API Endpoints

#### Get All Movies
- **URL**: `/movies`
- **Method**: `GET`
- **Response**: JSON array of all movies.

#### Get a Single Movie
- **URL**: `/movies/{id}`
- **Method**: `GET`
- **Response**: JSON object of the movie with the specified ID.

#### Create a Movie
- **URL**: `/movies`
- **Method**: `POST`
- **Request Body**:
  ```json
  {
    "isbn": "123456",
    "title": "New Movie",
    "director": {
      "firstname": "John",
      "lastname": "Doe"
    }
  }
  ```
- **Response**: JSON object of the created movie.

#### Update a Movie
- **URL**: `/movies/{id}`
- **Method**: `PUT`
- **Request Body**:
  ```json
  {
    "isbn": "654321",
    "title": "Updated Movie",
    "director": {
      "firstname": "Jane",
      "lastname": "Smith"
    }
  }
  ```
- **Response**: JSON object of the updated movie.

#### Delete a Movie
- **URL**: `/movies/{id}`
- **Method**: `DELETE`
- **Response**: JSON array of remaining movies.

## Project Structure

```
crud_api_go/
├── .gitignore       # Git ignore file
├── go.mod           # Go module file
├── go.sum           # Go dependencies checksum
├── LICENSE          # Project license
├── main.go          # Main application code
```

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgments

- [Gorilla Mux](https://github.com/gorilla/mux) for routing.
- Go community for their excellent resources and documentation.
```