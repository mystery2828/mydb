

---

# MyDB (A In-Memory DB) in Go

An efficient and simple in-memory database implemented in Golang. Designed for fast storage and retrieval of data within a single process, making it ideal for applications requiring quick access to data without the overhead of a persistent storage system.

## Features

- **Key-Value Storage**: Simple key-value storage with support for various data types.
- **CRUD Operations**: Support for Create, Read, Update, and Delete operations.
- **In-Memory Only**: Data is stored in memory, making it highly performant for read/write operations.
- **Concurrency**: Supports concurrent access to handle multiple operations simultaneously (WIP).
- **Persistence (Optional)**: Optionally persist data to disk (future feature).

## Getting Started

### Prerequisites

- Go 1.18 or later.

### Installation

Clone this repository to get started.

```bash
git clone https://github.com/yourusername/in-memory-db
cd in-memory-db
```

### Usage

Import the database in your Go project:

```go
import "github.com/yourusername/in-memory-db"
```

#### Example

```go
package main

import (
    "fmt"
    "your-module-name/db"
)

func main() {
    db := db.NewDB()
    
    // Set a key-value pair
    db.Set("foo", "bar")
    
    // Get a value
    value, exists := db.Get("foo")
    if exists {
        fmt.Println("Value:", value)
    }
    
    // Delete a key
    db.Delete("foo")
}
```

## Roadmap

- [ ] Add support for complex data types (e.g., lists, sets).
- [ ] Implement data persistence.
- [ ] Enhanced concurrency management.
- [ ] Optimizations for large datasets.

## Contributing

Contributions are welcome! Feel free to submit issues or pull requests to improve the functionality.

## License

This project is licensed under the MIT License.

--- 

This template outlines basic functionality and project goals. Update it as you add new features or enhance capabilities!