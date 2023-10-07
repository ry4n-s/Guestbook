# Guestbook

This is a web-based guestbook system built on a microservices architecture. Users can submit messages to the guestbook and view all previous entries. The application demonstrates the use of Redis for data storage and retrieval, the Go programming language for server-side logic, Flask with Python for analyzing tones of text, and JavaScript/jQuery for client-side interactivity.

## Features:

- **Guestbook Server (Go):** Responsible for data storage and retrieval. Uses the `mux`, `negroni`, and `simpleredis` packages for server routing, middleware, and Redis interactions respectively. 

  - **Endpoints:**
    - `/lrange/{key}`: Retrieves a list of guestbook entries.
    - `/rpush/{key}/{value}`: Appends a message to the guestbook.
    - `/info`: Provides Redis database information.
    - `/env`: Returns environment variable data.
    - `/hello`: Simple Hello endpoint with the app's hostname.

- **Tone Analyzer (Python/Flask):** Uses the IBM Watson Natural Language Understanding API to analyze the tone of the text.

  - **Endpoints:**
    - `/tone`: Analyzes the tone of given input text.
    - `/`: A simple home endpoint.

- **Front-end (JavaScript/jQuery):** Provides an interactive user interface for submitting messages to the guestbook and displays all previous entries. Polls the server every second to update guestbook entries.

- **Styling:** The look and feel are defined using custom CSS.

![needewdit](https://github.com/ry4n-s/Guestbook/assets/132171741/6e2271f8-b0ef-41a9-a0e1-171db9004480)
