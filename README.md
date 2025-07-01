# Golang Projects

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

### 7. File Copier (with concurrency enhancement)
**Knowledge Requirements:**  
- File operations (`os.Open`, `os.Create`)  
- Error handling  
- Using `io.Copy`  
- Goroutines and channels (for concurrency)  

**Description:**  
Copy a file from source to destination path.  
**Concurrency Enhancement:** Support copying multiple files concurrently.

**Detailed Guide:**  
- [ ] Accept a list of source and destination file paths from the user.
- [ ] For each file, launch a goroutine that copies the file using `io.Copy`.
- [ ] Use a channel to report completion or errors for each copy operation.
- [ ] Wait for all copy operations to finish before exiting.
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

### 9. Timer/Stopwatch (with concurrency enhancement)
**Knowledge Requirements:**  
- The `time` package  
- Loops and goroutines (for concurrency)  
- User input  

**Description:**  
A CLI timer or stopwatch that counts down or up.  
**Concurrency Enhancement:** Allow running multiple timers/stopwatches concurrently.

**Detailed Guide:**  
- [ ] Prompt the user for multiple time durations.
- [ ] Launch a goroutine for each timer/stopwatch, each prints updates independently.
- [ ] Use channels to signal when each timer finishes.
- [ ] Optionally, allow pausing/resuming specific timers using channels.

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

### 11. Simple Contact Book (with file I/O)
**Knowledge Requirements:**  
- Structs and slices  
- CLI menu logic  
- User input  
- File I/O (read/write contacts)  

**Description:**  
Store, display, and delete contacts with name and phone.

**Detailed Guide:**  
- [ ] Define a `Contact` struct.
- [ ] Use a slice to store contacts.
- [ ] CLI menu: add, list, search, delete contacts.
- [ ] Save contacts to a file after changes; read from file on start.
- [ ] Optionally, support exporting/importing contacts in different formats (CSV, JSON).

---

## Medium Projects

### 12. To-Do List with File Storage (with concurrency enhancement)
**Knowledge Requirements:**  
- File I/O  
- Structs and slices  
- JSON or CSV serialization (`encoding/json`, `encoding/csv`)  
- Goroutines and channels (for concurrency in saving/loading tasks)  
- Combining previous To-Do List knowledge  

**Description:**  
Enhance your CLI to-do app to save/load tasks from a file.  
**Concurrency Enhancement:** Save tasks to file in the background using a goroutine after each modification.

**Detailed Guide:**  
- [ ] Serialize the tasks slice to a JSON or CSV file after every change.
- [ ] Use a goroutine that listens on a channel for save requests and writes to the file.
- [ ] Load tasks from the file when the program starts.
- [ ] Handle file not found and corrupted file errors gracefully.

---

### 13. REST API for To-Do List (with concurrency enhancement)
**Knowledge Requirements:**  
- HTTP server basics (`net/http`)  
- JSON serialization/deserialization  
- Routing and handlers  
- Slices and structs  
- Sync primitives (`sync.Mutex` or channels) for safe concurrent access  

**Description:**  
Create a web API with endpoints to add, list, and delete tasks.  
**Concurrency Enhancement:** Use a mutex or channel to safely handle concurrent requests.

**Detailed Guide:**  
- [ ] Set up an HTTP server with `net/http`.
- [ ] Define handlers for `GET /tasks`, `POST /tasks`, and `DELETE /tasks/{id}`.
- [ ] Store tasks in a slice, use a `sync.Mutex` to guard access.
- [ ] Use `encoding/json` to handle request and response bodies.
- [ ] Test your API with `curl` or Postman.

---

### 14. Weather CLI App (with concurrency enhancement)
**Knowledge Requirements:**  
- HTTP requests (`net/http`)  
- JSON parsing (`encoding/json`)  
- Command-line input  
- Goroutines and WaitGroups for concurrency  

**Description:**  
Get current weather for multiple cities in parallel using a public API.

**Detailed Guide:**  
- [ ] Register for a free API key at [OpenWeatherMap](https://openweathermap.org/api).
- [ ] Prompt the user for a list of city names.
- [ ] For each city, launch a goroutine to fetch weather data.
- [ ] Use a `sync.WaitGroup` to wait for all results before displaying them.
- [ ] Parse and display results for each city.

---

### 15. URL Shortener (In-Memory, with concurrency enhancement)
**Knowledge Requirements:**  
- HTTP server (`net/http`)  
- Maps  
- Routing and URL parameters  
- Random string generation  
- `sync.RWMutex` for concurrent map access  

**Description:**  
Shorten URLs and redirect using an HTTP server.  
**Concurrency Enhancement:** Use a `sync.RWMutex` to allow multiple concurrent readers and safe updates to the in-memory map.

**Detailed Guide:**  
- [ ] Set up HTTP handlers for creating and accessing short links.
- [ ] Store mappings from short codes to URLs in a map, protected by a `sync.RWMutex`.
- [ ] Generate random strings for short codes.
- [ ] On a short URL visit, redirect to the stored URL using `http.Redirect`.
- [ ] Optionally, add a web interface for submitting URLs.

---

### 16. Markdown to HTML Converter (with concurrency enhancement)
**Knowledge Requirements:**  
- File I/O  
- Markdown processing library (e.g., `github.com/gomarkdown/markdown`)  
- Command-line arguments  
- Goroutines and WaitGroups for concurrency  

**Description:**  
Read multiple markdown files and output HTML files concurrently.

**Detailed Guide:**  
- [ ] Accept multiple markdown files as input from the command line.
- [ ] Launch a goroutine for each conversion.
- [ ] Use a `sync.WaitGroup` to wait for all conversions to complete.
- [ ] Write results to HTML files with the same base name.

---

### 17. Simple Chat App (CLI, Local Network, with concurrency enhancement)
**Knowledge Requirements:**  
- TCP/UDP networking (`net` package)  
- Goroutines for concurrency  
- Reading/writing with connections  
- Channels for message passing  

**Description:**  
Send messages between clients on the same network.  
**Concurrency Enhancement:** Each client uses goroutines and channels to send and receive messages simultaneously.

**Detailed Guide:**  
- [ ] Build a server that accepts multiple client connections.
- [ ] Each client launches one goroutine for reading and one for writing messages.
- [ ] Use channels to coordinate and display received messages.
- [ ] Optionally, add nicknames and private messaging.

---

### 18. Expense Tracker (with file I/O and concurrency)
**Knowledge Requirements:**  
- Structs and slices  
- Basic reporting logic  
- File I/O (for persistence)  
- Goroutines and channels for concurrent report generation (optional)  

**Description:**  
Track expenses, add categories, and show simple reports.

**Detailed Guide:**  
- [ ] Define an `Expense` struct with fields for amount, category, and date.
- [ ] Allow users to add new expenses and list all expenses.
- [ ] Calculate and display totals by category.
- [ ] Save/load expenses from a JSON or CSV file.
- [ ] Optionally, generate multiple reports (e.g., by category, by date) concurrently using goroutines and channels.

---

### 19. Basic Authentication System (with concurrency enhancement)
**Knowledge Requirements:**  
- Maps and structs  
- Password hashing (`crypto/sha256`)  
- User input and validation  
- `sync.RWMutex` for concurrent map access  

**Description:**  
CLI or basic web app for user signup/login (in memory).  
**Concurrency Enhancement:** Use a `sync.RWMutex` to allow concurrent reads and safe writes for user authentication data.

**Detailed Guide:**  
- [ ] Store usernames and hashed passwords in a map, protected by a `sync.RWMutex`.
- [ ] Implement signup (register), login, and logout functions.
- [ ] Use `crypto/sha256` to hash passwords before storage.
- [ ] Optionally, extend to a web interface using `net/http`.

---

### 20. AI-Powered Text Summarizer (OpenAI integration, file I/O, concurrency)
**Knowledge Requirements:**  
- Go HTTP client (`net/http`)  
- JSON encoding/decoding  
- Reading and writing files  
- Environment variables for API keys  
- Goroutines and channels for processing multiple files concurrently  
- OpenAI API basics (find docs at [OpenAI API docs](https://platform.openai.com/docs/api-reference))  

**Description:**  
Summarize text files using OpenAI’s GPT models.  
Supports reading multiple files, summarizing their contents in parallel, and writing results to output files.

**Detailed Guide:**  
- [ ] Sign up for an OpenAI API key and set it as an environment variable.
- [ ] Accept a list of text files from the user.
- [ ] For each file, launch a goroutine to:
    - Read file content.
    - Send a request to the OpenAI API for summarization.
    - Write the summary to a new file (e.g., `filename.summary.txt`).
- [ ] Use channels and a `sync.WaitGroup` to coordinate results and errors.
- [ ] Handle API rate limits and errors gracefully.
- [ ] Optionally, allow user to choose summary length or style.

---

### 21. AI-Powered Chatbot CLI (OpenAI integration, file I/O)
**Knowledge Requirements:**  
- HTTP requests (`net/http`)  
- JSON encoding/decoding  
- Environment variables for API keys  
- Reading and writing chat history to files  
- OpenAI API basics  

**Description:**  
A chatbot interface running in your terminal using OpenAI’s GPT models.  
Chat history is saved to a file, and you can reload previous conversations.

**Detailed Guide:**  
- [ ] Get an OpenAI API key and set it as an environment variable.
- [ ] Implement a CLI loop reading user input.
- [ ] For each input, send it to OpenAI’s API and print the response.
- [ ] Save the conversation to a file after each interaction.
- [ ] On startup, load previous chat history from file if available.
- [ ] Optionally, add a command to clear or export chat history.

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
- [OpenAI API Docs](https://platform.openai.com/docs/api-reference)

---
