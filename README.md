# hadiubaidillah.com

Personal portfolio website of Hadi Ubaidillah — showcasing resume, projects, demo apps, and certifications.

## Tech Stack

- HTML, CSS, JavaScript
- Bootstrap 3
- PHP (contact form)
- Nginx (web server)

## Project Structure

```
├── index.html          # Main single-page portfolio
├── css/                # Stylesheets
├── js/                 # JavaScript files
├── images/             # Images and portfolio assets
├── fonts/              # Icon and web fonts
├── contact_form/       # PHP contact form handler
│   ├── contact_form.php
│   └── config.php      # Sensitive credentials (ignored by git)
└── .github/workflows/
    └── deploy.yml      # GitHub Actions CI/CD
```

## CI/CD

Pushing to `main` automatically deploys to the server via GitHub Actions using SSH.

Required GitHub repository secrets:

| Secret | Description |
|---|---|
| `SSH_HOST` | Server IP or domain |
| `SSH_USER` | SSH username |
| `SSH_PRIVATE_KEY` | SSH private key (without passphrase) |
| `SSH_PORT` | SSH port (default: 22) |

## Local Development

No build step required. Open `index.html` directly in a browser or serve with any static file server.

## Contact Form

The contact form is handled by PHP at `contact_form/contact_form.php`. Create `contact_form/config.php` locally with the required credentials (see `config.php.example` if available). This file is excluded from git via `.gitignore`.
