# OAuth 2.0 Authorization Demo 🔐

A local-first OAuth 2.0 authorization flow demo with on-device user authentication. No external servers, no data collection — just a realistic OAuth consent screen built for testing and learning.

## What is OAuth 2.0 Authorization Demo?

This is a fully functional OAuth 2.0 authorization server simulator that demonstrates the authorization code flow. It features:

- **Realistic OAuth consent screen** with permission scopes
- **On-device user database** using IndexedDB
- **Multiple user accounts** with simulated profiles
- **Authorize/Deny flow** with visual feedback
- **Switch accounts** functionality
- **Local-first** with no external dependencies

## Key Features

- **OAuth Consent Screen:** Realistic permission request interface
- **On-Device Database:** Users stored locally in IndexedDB
- **Multiple Users:** Pre-populated with 4 demo accounts
- **Scope Permissions:** View profile, email, calendar (optional), contacts (optional)
- **Authorize Flow:** Simulates authorization code generation
- **Deny Flow:** Handles access denial
- **Switch Accounts:** Login with different users
- **Persistent Storage:** User data persists in browser
- **Responsive Design:** Works on all screen sizes

## How to Use

### Default Users

| User | Email | Password |
|------|-------|----------|
| Jamie Dawson | jamie.dawson@example.com | password123 |
| Alice Smith | alice.smith@example.com | password123 |
| Bob Johnson | bob.johnson@example.com | password123 |
| Carol White | carol.white@example.com | password123 |

### Flow

1. **Open the page** to see the consent screen
2. **Review requested permissions** (profile, email, calendar, contacts)
3. **Switch accounts** if needed using the "Switch" button
4. **Click "Authorize"** to grant access
5. **Or click "Deny"** to reject the request
6. **View the result** with success or error message

### Switching Accounts

1. Click **"Switch"** button
2. Enter email and password (use one of the default accounts above)
3. Click **"Sign In"**
4. The consent screen updates with the new user

## Technology Stack

- **HTML5:** Structure
- **CSS3:** Modern styling with gradients and animations
- **Vanilla JavaScript:** All logic with no frameworks
- **IndexedDB:** Local user database
- **Font Awesome:** Icons

## Project Structure

```
oauth-demo/
├── index.html          # Single-file application
└── README.md           # Project documentation
```

## Browser Support

Works on all modern browsers that support IndexedDB:
- Chrome (desktop + mobile)
- Firefox (desktop + mobile)
- Edge
- Safari (desktop + mobile)

## How the Database Works

The demo uses IndexedDB to store user data locally:

- **Database Name:** `OAuthLocalDB`
- **Store Name:** `users`
- **Index:** `email` (unique)
- **Data:** id, name, email, password, avatar

On first load, the database is seeded with 4 default users. All authentication happens entirely in your browser.
