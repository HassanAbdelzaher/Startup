# Golang Projects: Very Easy to Medium (With Knowledge Requirements, Descriptions & Guides)

---

## Very Easy Projects

### 1. Hello World CLI
**Knowledge Requirements:**  
- Go installation and setup  
- Basic Go syntax  
- Using `fmt` for printing  

**Description:**  
Your first Go program! Print "Hello, World!" or a custom message to the terminal.

**Guide:**  
- Install Go.
- Create a file `main.go`.
- Use `fmt.Println("Hello, World!")`.
- Run with `go run main.go`.

---

### 2. Simple Calculator
**Knowledge Requirements:**  
- Reading user input  
- Basic arithmetic operations  
- Using `switch` statements  

**Description:**  
A CLI tool that takes two numbers and an operation (+, -, *, /) and prints the result.

**Guide:**  
- Use `fmt.Scanln()` to read input.
- Use a `switch` to choose operation.
- Print the result.

---

### 3. Temperature Converter
**Knowledge Requirements:**  
- User input and output  
- Variables and type conversion  
- Simple math operations  

**Description:**  
Converts temperatures between Celsius and Fahrenheit.

**Guide:**  
- Ask user for input value and type.
- Use formulas:
  - C → F: `F = (C × 9/5) + 32`
  - F → C: `C = (F - 32) × 5/9`
- Print the converted value.

---

### 4. Guess the Number Game
**Knowledge Requirements:**  
- Random number generation (`math/rand`)  
- Loops and conditionals  
- Reading user input  

**Description:**  
A simple game where the program picks a random number and you try to guess it.

**Guide:**  
- Use `math/rand` for random numbers.
- Loop until the user guesses correctly.
- Give hints: "too high", "too low".

---

### 5. Word Counter
**Knowledge Requirements:**  
- Reading strings  
- String manipulation (`strings.Fields`)  
- Slices  

**Description:**  
Counts the number of words in a sentence entered by the user.

**Guide:**  
- Read input using `bufio.Scanner`.
- Use `strings.Fields` to split into words.
- Print the length of the slice.

---

## Easy Projects

### 6. To-Do List (CLI)
**Knowledge Requirements:**  
- Slices and loops  
- Structs for custom types  
- Simple CLI menu logic  

**Description:**  
A command-line to-do list: add, list, and remove tasks.

**Guide:**  
- Use a slice to store tasks.
- Use a loop to show menu options: add, list, remove, exit.
- Use `fmt.Scanln` or `bufio.Scanner` for input.

---

### 7. File Copier
**Knowledge Requirements:**  
- File operations (`os.Open`, `os.Create`)  
- Error handling  
- Using `io.Copy`  

**Description:**  
Copy a file from source to destination path.

**Guide:**  
- Use `os.Open` and `os.Create`.
- Use `io.Copy` to copy contents.
- Handle errors.

---

### 8. JSON Formatter
**Knowledge Requirements:**  
- JSON parsing and formatting (`encoding/json`)  
- Reading from files or standard input  
- Error handling  

**Description:**  
Reads raw JSON and pretty-prints it.

**Guide:**  
- Use `encoding/json` to unmarshal and marshal with indentation.
- Read JSON from a file or standard input.

---

### 9. Timer/Stopwatch
**Knowledge Requirements:**  
- The `time` package  
- Loops and goroutines (optional for more advanced timers)  
- User input  

**Description:**  
A CLI timer or stopwatch that counts down or up.

**Guide:**  
- Use `time.Sleep` and `time.Tick`.
- Take user input for duration.
- Print updates each second.

---

### 10. Palindrome Checker
**Knowledge Requirements:**  
- String manipulation  
- Functions  
- Basic logic  

**Description:**  
Checks if a given word or sentence is a palindrome.

**Guide:**  
- Normalize input (remove spaces, lowercase).
- Compare string with its reverse.

---

### 11. Simple Contact Book
**Knowledge Requirements:**  
- Structs and slices  
- CLI menu logic  
- User input  

**Description:**  
Store, display, and delete contacts with name and phone.

**Guide:**  
- Use a slice of structs.
- Add, list, and delete contacts.
- Use menu system for user interaction.

---

## Medium Projects

### 12. To-Do List with File Storage
**Knowledge Requirements:**  
- File I/O  
- Structs and slices  
- JSON or CSV serialization (`encoding/json`, `encoding/csv`)  
- Combining previous To-Do List knowledge  

**Description:**  
Enhance your CLI to-do app to save/load tasks from a file.

**Guide:**  
- Use `encoding/json` or `encoding/csv` to serialize tasks.
- Read from file on start, write to file on changes.

---

### 13. REST API for To-Do List
**Knowledge Requirements:**  
- HTTP server basics (`net/http`)  
- JSON serialization/deserialization  
- Routing and handlers  
- Slices and structs  

**Description:**  
Create a web API with endpoints to add, list, and delete tasks.

**Guide:**  
- Use `net/http` for server.
- Use handlers for `/tasks`, `/add`, `/delete`.
- Store tasks in memory.

---

### 14. Weather CLI App
**Knowledge Requirements:**  
- HTTP requests (`net/http`)  
- JSON parsing (`encoding/json`)  
- Command-line input  

**Description:**  
Get current weather for a city using a public API.

**Guide:**  
- Use `net/http` to call an API (e.g., OpenWeatherMap).
- Parse JSON response.
- Print weather info.

---

### 15. URL Shortener (In-Memory)
**Knowledge Requirements:**  
- HTTP server (`net/http`)  
- Maps  
- Routing and URL parameters  
- Random string generation  

**Description:**  
Shorten URLs and redirect using an HTTP server.

**Guide:**  
- Use a map to store short keys and URLs.
- Handler for creating short URLs and redirecting.
- Use `net/http`.

---

### 16. Markdown to HTML Converter
**Knowledge Requirements:**  
- File I/O  
- Markdown processing library (e.g., `github.com/gomarkdown/markdown`)  
- Command-line arguments  

**Description:**  
Read a markdown file and output HTML.

**Guide:**  
- Use a Go markdown library.
- Read file with `os` and convert.

---

### 17. Simple Chat App (CLI, Local Network)
**Knowledge Requirements:**  
- TCP/UDP networking (`net` package)  
- Goroutines for concurrency  
- Reading/writing with connections  

**Description:**  
Send messages between clients on the same network.

**Guide:**  
- Use TCP or UDP sockets.
- Handle sending/receiving in goroutines.

---

### 18. Expense Tracker
**Knowledge Requirements:**  
- Structs and slices  
- Basic reporting logic  
- File I/O (for persistence, optional)  

**Description:**  
Track expenses, add categories, and show simple reports.

**Guide:**  
- Use a struct for expenses.
- Store in slice or file.
- Calculate total per category.

---

### 19. Basic Authentication System
**Knowledge Requirements:**  
- Maps and structs  
- Password hashing (`crypto/sha256`)  
- User input and validation  

**Description:**  
CLI or basic web app for user signup/login (in memory).

**Guide:**  
- Use a map for users.
- Hash passwords with `crypto/sha256`.
- Check credentials on login.

---

## How to Start

1. **Pick a project** that matches your level.
2. **Break it down**: List the steps as seen in each guide.
3. **Write code** in small pieces, test as you go.
4. **Keep learning**: As you finish each project, try to improve it (better error handling, add tests, use file/database storage, etc).
5. **Publish** your finished projects on GitHub with a README!

---

## Resources

- [A Tour of Go](https://tour.golang.org/)
- [Go by Example](https://gobyexample.com/)
- [Effective Go](https://go.dev/doc/effective_go)
- [Go Standard Library docs](https://pkg.go.dev/std)

---
