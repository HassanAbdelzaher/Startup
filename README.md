# Golang Projects: Very Easy to Medium (With Knowledge Requirements, Descriptions & Detailed Guides)

---

## Very Easy Projects

### 1. Hello World CLI
**Knowledge Requirements:**  
- Go installation and setup  
- Basic Go syntax  
- Using `fmt` for printing  

**Description:**  
Your first Go program! Print "Hello, World!" or a custom message to the terminal.

**Detailed Guide:**  
- [ ] Install the Go SDK from [golang.org](https://go.dev/dl/).
- [ ] Create a directory for your project and run `go mod init helloworld`.
- [ ] Write a `main.go` file with:
  ```go
  package main
  import "fmt"
  func main() {
    fmt.Println("Hello, World!")
  }
  ```
- [ ] Use `go run main.go` to run your program.
- [ ] Modify the message and try printing variables or user input.

---

### 2. Simple Calculator
**Knowledge Requirements:**  
- Reading user input  
- Basic arithmetic operations  
- Using `switch` statements  

**Description:**  
A CLI tool that takes two numbers and an operation (+, -, *, /) and prints the result.

**Detailed Guide:**  
- [ ] Use `fmt.Scanln()` to read two numbers and an operator from the user.
- [ ] Implement arithmetic for each operation using a `switch`.
- [ ] Print the result with `fmt.Printf`.
- [ ] Handle invalid input gracefully (e.g., division by zero).

---

### 3. Temperature Converter
**Knowledge Requirements:**  
- User input and output  
- Variables and type conversion  
- Simple math operations  

**Description:**  
Converts temperatures between Celsius and Fahrenheit.

**Detailed Guide:**  
- [ ] Prompt the user for the temperature value and the unit (C/F).
- [ ] Use the correct formula for conversion.
- [ ] Print the converted value with the correct unit.
- [ ] Add support for repeated conversions in a loop.

---

### 4. Guess the Number Game
**Knowledge Requirements:**  
- Random number generation (`math/rand`)  
- Loops and conditionals  
- Reading user input  

**Description:**  
A simple game where the program picks a random number and you try to guess it.

**Detailed Guide:**  
- [ ] Generate a random number using `rand.Intn`.
- [ ] Prompt the user to guess the number.
- [ ] Loop until the user guesses correctly, giving feedback on each guess.
- [ ] Count the number of attempts and display it at the end.

---

### 5. Word Counter
**Knowledge Requirements:**  
- Reading strings  
- String manipulation (`strings.Fields`)  
- Slices  

**Description:**  
Counts the number of words in a sentence entered by the user.

**Detailed Guide:**  
- [ ] Read a full line of text using `bufio.Scanner`.
- [ ] Split the text into words using `strings.Fields`.
- [ ] Count and print the number of words.
- [ ] Optionally, add functionality to count characters or sentences.

---

## Easy Projects

### 6. To-Do List (CLI)
**Knowledge Requirements:**  
- Slices and loops  
- Structs for custom types  
- Simple CLI menu logic  

**Description:**  
A command-line to-do list: add, list, and remove tasks.

**Detailed Guide:**  
- [ ] Define a `Task` struct with a description and completion status.
- [ ] Use a slice to store tasks in memory.
- [ ] Implement a CLI menu to add, list, mark as done, and remove tasks.
- [ ] Loop the menu until the user exits.
- [ ] Optionally, display completed and pending tasks separately.

---

### 7. File Copier
**Knowledge Requirements:**  
- File operations (`os.Open`, `os.Create`)  
- Error handling  
- Using `io.Copy`  

**Description:**  
Copy a file from source to destination path.

**Detailed Guide:**  
- [ ] Accept source and destination file paths from the user.
- [ ] Open the source file with `os.Open`.
- [ ] Create the destination file with `os.Create`.
- [ ] Use `io.Copy` to copy contents.
- [ ] Handle errors and display appropriate messages.
- [ ] Optionally, check for file existence and overwrite confirmation.

---

### 8. JSON Formatter
**Knowledge Requirements:**  
- JSON parsing and formatting (`encoding/json`)  
- Reading from files or standard input  
- Error handling  

**Description:**  
Reads raw JSON and pretty-prints it.

**Detailed Guide:**  
- [ ] Read JSON data from a file or standard input.
- [ ] Use `json.Unmarshal` to parse the JSON into an `interface{}`.
- [ ] Use `json.MarshalIndent` to pretty-print the JSON.
- [ ] Print the formatted JSON, or write it to a new file.

---

### 9. Timer/Stopwatch
**Knowledge Requirements:**  
- The `time` package  
- Loops and goroutines (optional for more advanced timers)  
- User input  

**Description:**  
A CLI timer or stopwatch that counts down or up.

**Detailed Guide:**  
- [ ] Prompt the user for a time duration.
- [ ] Use `time.Sleep` or a loop with `time.Tick` to count down/up.
- [ ] Print the remaining or elapsed time every second.
- [ ] Optionally, add pause, resume, and reset features.

---

### 10. Palindrome Checker
**Knowledge Requirements:**  
- String manipulation  
- Functions  
- Basic logic  

**Description:**  
Checks if a given word or sentence is a palindrome.

**Detailed Guide:**  
- [ ] Read a string from the user.
- [ ] Remove spaces and convert to lowercase.
- [ ] Check if the string equals its reverse.
- [ ] Print the result: palindrome or not.

---

### 11. Simple Contact Book
**Knowledge Requirements:**  
- Structs and slices  
- CLI menu logic  
- User input  

**Description:**  
Store, display, and delete contacts with name and phone.

**Detailed Guide:**  
- [ ] Define a `Contact` struct.
- [ ] Use a slice to store contacts.
- [ ] CLI menu: add, list, search, delete contacts.
- [ ] Optional: Save/load contacts to/from a file.

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

**Detailed Guide:**  
- [ ] Serialize the tasks slice to a JSON or CSV file after every change.
- [ ] Load tasks from the file when the program starts.
- [ ] Update your CLI to use file-backed storage.
- [ ] Handle file not found and corrupted file errors gracefully.

---

### 13. REST API for To-Do List
**Knowledge Requirements:**  
- HTTP server basics (`net/http`)  
- JSON serialization/deserialization  
- Routing and handlers  
- Slices and structs  

**Description:**  
Create a web API with endpoints to add, list, and delete tasks.

**Detailed Guide:**  
- [ ] Set up an HTTP server with `net/http`.
- [ ] Define handlers for `GET /tasks`, `POST /tasks`, and `DELETE /tasks/{id}`.
- [ ] Store tasks in a slice.
- [ ] Use `encoding/json` to handle request and response bodies.
- [ ] Test your API with `curl` or Postman.

---

### 14. Weather CLI App
**Knowledge Requirements:**  
- HTTP requests (`net/http`)  
- JSON parsing (`encoding/json`)  
- Command-line input  

**Description:**  
Get current weather for a city using a public API.

**Detailed Guide:**  
- [ ] Register for a free API key at [OpenWeatherMap](https://openweathermap.org/api).
- [ ] Prompt the user for a city name.
- [ ] Make an HTTP GET request to the weather API.
- [ ] Parse the JSON response and display the temperature and weather description.
- [ ] Handle API errors and invalid city names.

---

### 15. URL Shortener (In-Memory)
**Knowledge Requirements:**  
- HTTP server (`net/http`)  
- Maps  
- Routing and URL parameters  
- Random string generation  

**Description:**  
Shorten URLs and redirect using an HTTP server.

**Detailed Guide:**  
- [ ] Set up HTTP handlers for creating and accessing short links.
- [ ] Store mappings from short codes to URLs in a map.
- [ ] Generate random strings for short codes.
- [ ] On a short URL visit, redirect to the stored URL using `http.Redirect`.
- [ ] Optionally, add a web interface for submitting URLs.

---

### 16. Markdown to HTML Converter
**Knowledge Requirements:**  
- File I/O  
- Markdown processing library (e.g., `github.com/gomarkdown/markdown`)  
- Command-line arguments  

**Description:**  
Read a markdown file and output HTML.

**Detailed Guide:**  
- [ ] Accept a markdown file as input from the command line.
- [ ] Use a markdown library to convert the file contents.
- [ ] Write the result to an HTML file.
- [ ] Optionally, support batch conversion.

---

### 17. Simple Chat App (CLI, Local Network)
**Knowledge Requirements:**  
- TCP/UDP networking (`net` package)  
- Goroutines for concurrency  
- Reading/writing with connections  

**Description:**  
Send messages between clients on the same network.

**Detailed Guide:**  
- [ ] Build a server that accepts multiple client connections.
- [ ] Each client can send messages, which are broadcast to all connected clients.
- [ ] Use goroutines to handle reading/writing for each connection.
- [ ] Optionally, add nicknames and private messaging.

---

### 18. Expense Tracker
**Knowledge Requirements:**  
- Structs and slices  
- Basic reporting logic  
- File I/O (for persistence, optional)  

**Description:**  
Track expenses, add categories, and show simple reports.

**Detailed Guide:**  
- [ ] Define an `Expense` struct with fields for amount, category, and date.
- [ ] Allow users to add new expenses and list all expenses.
- [ ] Calculate and display totals by category.
- [ ] Optionally, save/load expenses from a JSON or CSV file.

---

### 19. Basic Authentication System
**Knowledge Requirements:**  
- Maps and structs  
- Password hashing (`crypto/sha256`)  
- User input and validation  

**Description:**  
CLI or basic web app for user signup/login (in memory).

**Detailed Guide:**  
- [ ] Store usernames and hashed passwords in a map.
- [ ] Implement signup (register), login, and logout functions.
- [ ] Use `crypto/sha256` to hash passwords before storage.
- [ ] Optionally, extend to a web interface using `net/http`.

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
