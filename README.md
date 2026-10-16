# WP AI Assistant

A custom WordPress plugin that adds an AI-powered question and answer box to any page or post using the OpenAI API.

## Features

- Simple shortcode: `[wp_ai_assistant]`
- Nonce verification to protect the form
- Input sanitization and a 2000 character limit
- Output escaping to prevent XSS
- API key kept out of the code, stored in `wp-config.php`
- Error handling for missing keys, failed requests, invalid responses, and empty answers
- Server-side error logging for API failures

## Requirements

- WordPress 5.8 or higher
- PHP 7.4 or higher
- An OpenAI API key

## Installation

1. Copy the `wp-ai-assistant` folder to `wp-content/plugins/`.
2. Activate **WP AI Assistant** from the WordPress admin under **Plugins**.
3. Add your API key to `wp-config.php`, above the line that says "That's all, stop editing":

   ```php
   define( 'OPENAI_API_KEY', 'your-api-key-here' );
   ```

4. Add the shortcode to any page or post:

   ```
   [wp_ai_assistant]
   ```

## Usage

1. Open the page where you added the shortcode.
2. Type a question in the text box.
3. Click **Ask AI** to see the response on the same page.

## Project Structure

```
wp-ai-assistant/
├── wp-ai-assistant.php
├── assets/
│   ├── css/
│   │   └── ai-assistant.css
│   └── js/
│       └── ai-assistant.js
└── README.md
```

## Tech Stack

- PHP
- WordPress Plugin API (shortcodes, nonces, HTTP API)
- OpenAI Responses API

## Security Notes

- Never commit your API key to version control.
- Set a monthly spending limit in your OpenAI account.
- Nonces, sanitization, and escaping are used throughout.

## Roadmap

- [ ] REST API endpoint with AJAX (no page reload)
- [ ] Per-IP rate limiting
- [ ] Conversation history
- [ ] Settings page for model and system prompt
- [ ] Admin option to store the API key securely

## Screenshots

Add screenshots here:

```
![Plugin form](screenshots/form.png)
![AI response](screenshots/response.png)
```

## Author

**Pankaj Kamle**
Laravel and WordPress Developer | AI Integration | Indore, India
LinkedIn: https://www.linkedin.com/in/pankaj-kamle-1150b51

## License

GPL-2.0-or-later
