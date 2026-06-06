# Simple Go HTTP Web Server

A lightweight, concurrent HTTP web server written in Go using the standard library (`net/http`). This server hosts a static website and provides a couple of basic endpoints for demonstration purposes.

## 🚀 Features

*   **Static File Server:** Serves files from the [`static/`](file:///Users/yugjain/Documents/Golang/go_projects/go_server/static) directory (e.g., `index.html`, `form.html`) at the root URL `/`.
*   **Simple GET Endpoint:** A `/hello` endpoint that responds with a friendly text greeting.
*   **Form POST Endpoint:** A `/form` endpoint that processes incoming POST requests containing form data.

---

## 📁 Directory Structure

```text
go_server/
├── main.go          # Main Go application entry point containing HTTP route handlers
├── static/          # Directory containing static HTML files
│   ├── index.html   # Main homepage HTML file
│   └── form.html    # Simple user submission form HTML
└── README.md        # Project documentation
```

---

## 🛠️ Getting Started

### Prerequisites

Ensure you have [Go](https://go.dev/doc/install) installed on your system.

### Running the Server

1. Navigate to the project root directory.
2. Run the server using:
   ```bash
   go run main.go
   ```
3. The server will start on port `8080`. You should see the following output:
   ```text
   Starting server at port 8080
   ```

---

## 🔌 API Endpoints & Routes

| Path | Allowed Method(s) | Description |
| :--- | :--- | :--- |
| `/` | `GET` | Serves static assets from the `static/` folder (default is `index.html`) |
| `/hello` | `GET` | Responds with a simple "Hello!" plain text message |
| `/form` | `POST` | Parses and processes submitted form inputs |

### Testing the Endpoints

*   **Home Page:** Open your browser and navigate to [http://localhost:8080](http://localhost:8080).
*   **Hello Page:** Open your browser and navigate to [http://localhost:8080/hello](http://localhost:8080/hello).
*   **Form Page:** Open your browser and navigate to [http://localhost:8080/form.html](http://localhost:8080/form.html), fill out the form, and click **Submit**.
