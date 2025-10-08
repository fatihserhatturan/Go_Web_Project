# Product Management REST API

A simple product management REST API application built with Go.

## Technologies

- Go 1.21
- Echo Framework (Web Framework)
- PostgreSQL (Database)
- pgx (PostgreSQL Driver)

## Project Structure

The project follows layered architecture principles:

- `controller`: HTTP request handling layer
- `service`: Business logic layer
- `persistence`: Database access layer
- `domain`: Domain models
- `common`: Shared configurations

## Setup

Configure database connection:
```go
Host: localhost
Port: 6432
Database: productapp
User: postgres
Password: postgres
```

Install dependencies:
```bash
go mod download
```

Run the application:
```bash
go run main.go
```

## API Endpoints

- `GET /api/v1/products` - List all products
- `GET /api/v1/products?store={store}` - Filter by store
- `GET /api/v1/products/:id` - Get product by ID
- `POST /api/v1/products` - Add new product
- `PUT /api/v1/products/:id?newPrice={price}` - Update price
- `DELETE /api/v1/products/:id` - Delete product

## Testing

Prepare test database:
```bash
./test/scripts/test_db.sh
```

Run tests:
```bash
go test ./test/...
```
