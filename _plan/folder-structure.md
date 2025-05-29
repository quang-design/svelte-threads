# Svelte Threads - Folder Structure

```plain
/svelte-threads
├── src/
│ ├── app.html # Main HTML shell
│ ├── app.d.ts # Global TypeScript definitions for SvelteKit
│ ├── app.postcss # Global CSS, Tailwind configuration with @theme
│ │
│ ├── lib/ # Library code, utilities, components
│ │ ├── assets/ # Static assets (images, fonts, etc.)
│ │ │ └── icons/ # SVG icons
│ │ ├── components/ # Reusable Svelte components
│ │ │ ├── layout/ # Layout components (e.g., navbar, sidebar)
│ │ │ │ ├── main-layout.svelte
│ │ │ │ └── bottom-navbar.svelte
│ │ │ ├── ui/ # UI primitives (buttons, inputs, cards - potentially from shadcn-svelte)
│ │ │ │ ├── button.svelte
│ │ │ │ └── avatar.svelte
│ │ │ └── features/ # Feature-specific components
│ │ │ ├── thread-card.svelte
│ │ │ ├── create-thread-form.svelte
│ │ │ └── user-profile-header.svelte
│ │ ├── stores/ # Svelte stores for global state (if needed beyond Svelte 5 runes)
│ │ ├── types/ # TypeScript interfaces and types
│ │ │ └── index.ts
│ │ └── utils/ # Utility functions (e.g., date formatting, API helpers)
│ │ └── index.ts
│ │
│ ├── routes/ # Application routes and API endpoints
│ │ ├── (app)/ # Route group for main application (e.g., authenticated routes)
│ │ │ ├── +layout.svelte # Layout for the (app) group
│ │ │ ├── +page.svelte # Home page (feed)
│ │ │ ├── thread/
│ │ │ │ └── [id]/
│ │ │ │ └── +page.svelte # Single thread view
│ │ │ ├── profile/
│ │ │ │ └── [username]/
│ │ │ │ └── +page.svelte # User profile page
│ │ │ ├── activity/
│ │ │ │ └── +page.svelte # Activity feed
│ │ │ ├── search/
│ │ │ │ └── +page.svelte # Search page
│ │ │ └── create-thread/
│ │ │ └── +page.svelte # Page to create a new thread
│ │ ├── (auth)/ # Route group for authentication pages
│ │ │ ├── login/
│ │ │ │ └── +page.svelte
│ │ │ └── signup/
│ │ │ └── +page.svelte
│ │ ├── +layout.svelte # Root layout for all pages
│ │ ├── +page.server.ts # Server-load functions for the root page (if any)
│ │ └── +error.svelte # Global error page (customized)
│ │
│ ├── hooks.server.ts # Server-side hooks
│ └── hooks.client.ts # Client-side hooks (if needed)
│
├── static/ # Static assets (favicon, robots.txt, etc.)
│ ├── favicon.png
│ └── robots.txt
│
├── tests/ # Unit and integration tests
│ └── setup.ts # Test setup (e.g., Vitest config)
│
├── .env # Environment variables (gitignored)
├── .env.example # Example environment variables
├── .gitignore
├── .prettierrc.json # Prettier configuration
├── package.json # Project dependencies and scripts
├── svelte.config.js # SvelteKit configuration
├── tsconfig.json # TypeScript configuration
├── vite.config.ts # Vite configuration
└── README.md # Project documentation
```
