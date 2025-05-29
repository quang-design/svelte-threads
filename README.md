# Svelte Threads (WIP)

A modern, responsive social media application built with SvelteKit 5, Supabase, and Tailwind CSS v4.

## Features

- **Real-time Updates**: Experience instant interactions with real-time messaging and notifications
- **Responsive Design**: Fully responsive UI that works beautifully on all devices
- **Authentication**: Secure user authentication with Supabase Auth
- **Rich Content**: Support for text, images, and interactive content
- **Modern UI**: Clean, intuitive interface styled with Tailwind CSS v4
- **Performance Optimized**: Fast loading times and smooth interactions

## Tech Stack

- **Frontend**: SvelteKit 5 with TypeScript
- **Styling**: Tailwind CSS v4
- **Backend**: Supabase (Authentication, Database, Storage)
- **Deployment**: Vercel/Netlify

## Getting Started

### Prerequisites

- Node.js 18+ and npm/pnpm/yarn
- Supabase account (for backend services)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/quang-design/svelte-threads.git
   cd svelte-threads
   ```

2. Install dependencies:

   ```bash
   npm install
   # or
   pnpm install
   # or
   yarn
   ```

3. Set up environment variables:
   Create a `.env` file in the root directory with your Supabase credentials:

   ```env
   PUBLIC_SUPABASE_URL=your_supabase_url
   PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

4. Start the development server:

   ```bash
   pnpm dev
   # or
   pnpm dev -- --open
   ```

## Development

### Project Structure

```text
svelte-threads/
├── src/
│   ├── lib/
│   │   ├── components/
│   │   ├── stores/
│   │   ├── utils/
│   │   └── supabase.ts
│   ├── routes/
│   └── app.html
├── static/
├── tests/
└── package.json
```

### Building for Production

```bash
pnpm build
```

Preview the production build:

```bash
pnpm preview
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- [SvelteKit](https://kit.svelte.dev/)
- [Supabase](https://supabase.io/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Svelte-Shadcn](https://www.shadcn-svelte.com/)
