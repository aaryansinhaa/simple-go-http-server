# Simple Go HTTP Server

This project is a basic HTTP server built in Go. It serves static files, processes form submissions, and handles basic routes. 

---

## Features

1. **Static File Server**:
   - Serves files from the `./static` directory on the root (`/`) path.

2. **Routes**:
   - `/hello`: Responds to GET requests with a simple "Hello!" message.
   - `/form`: Processes form submissions and extracts `name` and `address` fields.

3. **Error Handling**:
   - Returns appropriate HTTP status codes for invalid paths or methods.

---

## Getting Started

### Prerequisites
- Go 1.20+ installed on your system.

### Installation
1. Clone this repository.
   ```bash
   git clone https://github.com/aaryansinhaa/simple-go-http-server.git
   cd simple-go-http-server
   ```

2. Create a `static` directory in the project folder and add some files to serve (e.g., `index.html`).

3. Run the server:
   ```bash
   go run main.go
   ```

4. Open your browser and navigate to:
   - Static files: `http://localhost:8080/`
   - Hello route: `http://localhost:8080/hello`
   - Form route: Submit a POST request to `http://localhost:8080/form`.

---

## Example Form Request

To test the `/form` route, you can use a tool like [Postman](https://www.postman.com/) or `curl`.  
Example `curl` command:
```bash
curl -X POST -d "name=John&address=123+Main+St" http://localhost:8080/form
```

---

## Notes

- The static files are served from the `./static` directory relative to the project root.
- To change the port, modify the `":8080"` in the `http.ListenAndServe` function in `main.go`.

---

## Author

- **Aaryan Kumar Sinha**  
  Feel free to reach out for any questions or contributions!  

---

## License

This project is open-source. You can modify and distribute it as needed.