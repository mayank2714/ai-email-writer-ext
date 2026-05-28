# AI Email Writer Extension

A lightweight Chrome extension that injects an AI-powered reply button into Gmail and generates reply drafts using a backend API.

## Overview

This extension detects the Gmail compose/reply toolbar, inserts an `AI reply` button, reads the current email content, sends it to a configured backend, and inserts the generated reply text into Gmail's compose editor.

## Features

- Adds an `AI reply` button to Gmail's compose and reply UI
- Extracts email content from the active Gmail message view
- Sends the content to a backend service for reply generation
- Inserts the generated reply into Gmail's compose box
- Minimal setup and lightweight JavaScript implementation

## Backend Configuration

The extension is configured to use this backend:

- `https://ai-email-writer-backend-3waa.onrender.com`

The API endpoint used by the extension is:

- `POST https://ai-email-writer-backend-3waa.onrender.com/api/email/generate`

### Request payload

```json
{
  "emailContent": "<extracted email text>",
  "tone": "professional"
}
```

## Project Structure

- `manifest.json` — Chrome extension manifest
- `content.js` — content script that injects the button and handles Gmail DOM logic
- `README.md` — project documentation

## Installation

1. Open Chrome and go to `chrome://extensions`
2. Enable `Developer mode`
3. Click `Load unpacked`
4. Select the project folder: `e:\springboot\email-writer-ext`
5. Reload the extension after code changes

## Usage

1. Open Gmail
2. Create a new message or reply to an existing email
3. Wait for the `AI reply` button to appear in the toolbar
4. Click `AI reply`
5. The generated reply text will be inserted into the compose box

## Notes

- Works only on Gmail pages (`*://mail.google.com/*`)
- The backend must be available and reachable from the browser
- Gmail UI updates may require selector updates in `content.js`
- `content.css` is available for future styling improvements

## Development

- Edit `content.js` to adjust button behavior or selectors
- Reload the extension in `chrome://extensions` after making changes

## Future Improvements

- Add user-visible loading and error handling
- Support tone selection or custom prompt options
- Add settings for backend URL and tone choice
