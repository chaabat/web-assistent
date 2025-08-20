# Web Assistant

A self-contained, bilingual web assistant that runs entirely from a single `index.html` file, loading its phrase library from JSON. Includes an `admin.html` tool to manage (create, edit, delete, save) the JSON phrase files. 

---

## Features

- Single-page main interface in `index.html`  
- Two JSON libraries at the root:  
  - `en.json` for English phrases  
  - `it.json` for Italian phrases  
- Bilingual UI: toggle between English and Italian at runtime  
- SEO-ready metadata in English only  
- Admin interface in `admin.html` for live editing of both JSON files  
- No external dependencies or build step—just HTML, CSS, and vanilla JavaScript  
- Responsive and mobile-first design  

---

## File Structure

| Path          | Description                                                                 |
|---------------|-----------------------------------------------------------------------------|
| index.html    | Main assistant interface; loads `en.json` or `it.json` based on locale       |
| admin.html    | JSON editor for adding, modifying, deleting, and saving phrase entries       |
| en.json       | English phrase library                                                       |
| it.json       | Italian phrase library                                                       |

---

## Getting Started

1. Clone the repository  
   ```
   git clone https://github.com/bocaletto-luca/web-assistent.git
   cd web-assistent
   ```

2. Run a simple local server (to allow JSON fetches)  
   ```
   python3 -m http.server 8000
   ```
   or any static file server of your choice.

3. Open `http://localhost:8000/index.html` for the assistant, or  
   `http://localhost:8000/admin.html` for the admin editor.

---

## Usage

- **Switch Language:** Click the language toggle in the header to switch between English and Italian interfaces.  
- **Ask a Question:** Type your query in the input box and press Send. The assistant looks up the key in the loaded JSON and returns the matching phrase or a default fallback.  
- **Manage Phrases:** Navigate to `admin.html`, select the target language file (EN or IT), and use the on-page form to add, edit, or remove entries. Click Save to update the JSON file on the server.

---

## Data Model

Each JSON file uses a simple key/value structure:

```json
{
  "greeting": {
    "title": "Hello",
    "response": "Welcome! How can I assist you today?"
  },
  "farewell": {
    "title": "Goodbye",
    "response": "See you soon!"
  }
}
```

- **Key:** lookup string (lowercased)  
- **title:** user-facing prompt or label  
- **response:** assistant reply  

The admin UI ensures this schema is respected and validates before saving.

---

## SEO and Metadata

`index.html` includes:

- English-only `<meta>` tags for title, description, Open Graph, and Twitter Cards  
- A JSON-LD script describing the website and author  
- Canonical URL pointing to the live English-only landing page  

The Italian UI does not expose separate SEO metadata.

---

## Contributing

- Open issues for bugs or feature requests  
- Submit pull requests against the `main` branch  
- Follow the existing HTML/CSS/JS style and JSON schema  
- Include meaningful commit messages  

---

## License

MIT License

---

## Author

Bocaletto Luca  
GitHub: https://github.com/bocaletto-luca  
Repository: web-assistent
