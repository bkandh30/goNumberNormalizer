# Go Phone Number Normalizer

A Go application that normalizes phone numbers stored in a PostgreSQL database by removing all non-digit characters and handling duplicates intelligently.

## Installation

1. Clone the repository:

```bash
git clone https://github.com/bkandh30/goNumberNormalizer.git
cd goNumberNormalizer
```

2. Install dependencies:

```bash
go mod tidy
```

3. Set up your PostgreSQL database and update the connection parameters in `main.go`:

```go
const (
    host     = "localhost"
    port     = 5432
    user     = "your_username"
    password = "your_password"
    dbname   = "phone"
)
```

## Usage

Run the application:

```bash
go run main.go
```

The application will:

1. Reset and recreate the database
2. Create the `phone_numbers` table
3. Seed the database with sample phone numbers
4. Normalize all phone numbers by removing non-digit characters
5. Handle duplicates by removing the original entries

## Dependencies

- `github.com/lib/pq` - PostgreSQL driver for Go
