A simple Chrome extension for Gmail that injects an AI reply button into the compose/reply toolbar and generates reply text using a local backend API.

Features
Injects an AI reply button into Gmail compose/reply UI
Reads the current email content from Gmail
Sends content to http://localhost:8080/api/email/generate
Inserts generated reply text into the compose box
Lightweight plain JavaScript content script
