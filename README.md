# Foodie — Restaurant Website Extension Project

A React practice project demonstrating how an existing restaurant website can be extended with an administrator area for menu management.

## Existing website selected

This project is based on the assignment concept of extending the public React restaurant template **Foodie** by `chthonn`:

- Original repository: https://github.com/chthonn/Foodie
- Original live demo: https://foodie01.netlify.app/
- The repository describes a React restaurant website with a menu, food imagery, ordering interface, about section and contact information. Its repository states that it is licensed under the MIT License.

**Important provenance note:** This downloadable package is a complete, self-contained React implementation of the extension concept, prepared because the original repository could not be fetched into this workspace. It is not a patch or a copy of the original repository files. For a strict assignment submission requiring direct edits to the exact upstream source, clone the original repository and port the `Admin`, `Login`, menu state and styles from this package into it. Keep the original licence and attribution when reusing upstream code.

## Features added for the extension

- `/admin` administrator entry point and login screen
- Admin overview with menu counts and availability statistics
- Create, read, update and delete (CRUD) menu items
- Search menu items
- Toggle item availability
- Changes made in the admin dashboard update the public menu immediately
- Menu changes persist after refresh using browser LocalStorage
- Responsive customer website and admin layout

## Run locally

Requirements: Node.js 18 or later and npm.

```bash
npm install
npm run dev
```

Open the local URL printed by Vite (usually `http://localhost:5173`).

To create a production build:

```bash
npm run build
npm run preview
```

## Demo administrator login

- URL: `http://localhost:5173/admin`
- Email: `admin@foodie.com`
- Password: `admin123`

These are demonstration credentials only. Authentication is simulated in the browser and is **not secure for a real production website**. LocalStorage is browser-specific and is not a shared database. A real deployment requires server-side authentication, authorization and a database/API.

## How to demonstrate CRUD

1. Open `/admin` and sign in with the demo credentials.
2. Select **Menu items**.
3. Click **Add new item**, complete the form and save.
4. Edit the new item and change its price or description.
5. Toggle its availability to hide/show it on the public menu.
6. Delete the item.
7. Open the public homepage and show that the menu reflects the changes.
8. Refresh the page to demonstrate LocalStorage persistence.

## Suggested folder structure

```text
foodie-extension/
├── index.html
├── package.json
├── README.md
└── src/
    ├── App.jsx       # Public site, admin, login and CRUD logic
    ├── main.jsx      # React entry point
    └── styles.css    # Responsive styling
```

## Technology

- React 18
- JavaScript (ES6+)
- CSS3
- Vite
- Browser LocalStorage for demonstration persistence
