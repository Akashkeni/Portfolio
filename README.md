# Portfolio

A personal portfolio website built with React, Vite, and Tailwind CSS. Features a dark/light theme toggle and an animated star + meteor background.

## Tech Stack

- **React 19** — UI library
- **Vite 8** — build tool and dev server
- **Tailwind CSS v4** — utility-first styling (via `@tailwindcss/vite` plugin)
- **React Router DOM v7** — client-side routing
- **Radix UI** — accessible UI primitives (toast)
- **Lucide React** — icon set
- **clsx + tailwind-merge** — conditional class name utilities

## Project Structure

```
src/
├── components/
│   ├── StarBackground.jsx   # Animated stars and meteors canvas
│   └── ThemeToggle.jsx      # Dark/light mode toggle (persisted to localStorage)
├── pages/
│   ├── Home.jsx             # Main landing page
│   └── NotFound.jsx         # 404 fallback page
├── lib/
│   └── utils.js             # cn() helper (clsx + twMerge)
├── assets/                  # Static images and SVGs
├── App.jsx                  # Router setup
├── main.jsx                 # App entry point
└── index.css                # Global styles and Tailwind base
public/
├── favicon.svg
└── icons.svg
```

## Getting Started

### Prerequisites

- Node.js 18+
- npm

### Installation

```bash
npm install
```

### Development

```bash
npm run dev
```

Opens at `http://localhost:5173` by default.

### Build

```bash
npm run build
```

Output goes to the `dist/` folder.

### Preview Production Build

```bash
npm run preview
```

### Lint

```bash
npm run lint
```

## Features

- **Theme toggle** — switches between dark and light mode; preference saved in `localStorage`
- **Star background** — dynamically generated stars (density based on viewport size) with subtle pulse animation
- **Meteor showers** — randomized meteor animations layered over the star field
- **Responsive** — theme toggle is hidden on small screens (`max-sm:hidden`)
- **Path alias** — `@` resolves to `./src` for clean imports
