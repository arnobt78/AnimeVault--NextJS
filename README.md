# AnimeVault Server Action - NextJS

![project25](https://github.com/user-attachments/assets/08b14faa-3e9a-4fb2-a794-2e82c35980ac) ![Screenshot 2024-09-16 at 13 57 39](https://github.com/user-attachments/assets/b0ea18a0-e6cd-4d69-b222-018de87b8fe9)

---

## Project Summary

AnimeVault is a modern, fully server-rendered anime listing and browsing platform built with **Next.js 14**. Its main purpose is to provide a beautiful, performant, and interactive interface for anime enthusiasts to discover and browse anime, leveraging up-to-date data from open APIs. This project demonstrates advanced Next.js features such as Server Actions, infinite scroll, dynamic routing, Framer Motion animations, and seamless deployment with Vercel.

Whether you want to learn how to build a fast React application with the latest Next.js features, or are looking for a skeleton to launch your own content-driven site, this repository is an excellent starting point.

- **Live Demo:** https://anime-vault-arnob.vercel.app/

---

## Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Technology Stack](#technology-stack)
- [Screenshots](#screenshots)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Project](#running-the-project)
- [Project Structure Walkthrough](#project-structure-walkthrough)
- [Key Commands](#key-commands)
- [API & References](#api--references)
- [Main Functionalities & How It Works](#main-functionalities--how-it-works)
- [Keywords](#keywords)
- [Contributing](#contributing)
- [License](#license)
- [Additional Notes](#additional-notes)

---

## Features

- **Next.js 14 with Server Actions:** Utilizes the latest Next.js features for server-side logic and high performance.
- **Server-Side Rendering (SSR):** All pages are rendered on the server for SEO and speed.
- **Infinite Scroll:** Seamless data loading as the user browses through the anime list.
- **Framer Motion Animations:** Smooth, modern transitions and UI effects.
- **Responsive and Mobile-Friendly:** Works perfectly on desktops, tablets, and phones.
- **Live Data Fetching:** Connects to public anime APIs (such as Shikimori) for real-time anime information.
- **Modern UI/UX:** Clean, attractive interface with dynamic routing and animated transitions.
- **Easy Deployment:** Ready to deploy on Vercel or any Node.js-supported hosting.
- **Extensible Structure:** Modular codebase, ideal for learning, modification, and extension.

---

## Project Structure

```
AnimeVault--NextJS/
├── app/                # Main Next.js app folder (pages, layouts, server actions, API handlers)
│   ├── page.js         # Main landing page
│   └── ...             # Other app-specific files (routes, layouts, etc.)
├── components/         # Reusable UI or logic building blocks (Cards, Lists, etc.)
├── public/             # Static assets (images, icons, etc.)
├── styles/             # Global and modular CSS/Tailwind files
├── .eslintrc.json      # ESLint configuration
├── .gitignore          # Files & folders to ignore in git
├── next.config.js      # Next.js configuration
├── package.json        # Project dependencies and scripts
├── package-lock.json   # Dependency lock file
├── postcss.config.js   # PostCSS configuration (for Tailwind, etc.)
├── tailwind.config.ts  # Tailwind CSS configuration
├── tsconfig.json       # TypeScript configuration
├── README.md           # Project documentation
└── ...
```

> **Note**: This structure is based on top-level results. For a complete file/folder list, visit the [GitHub UI](https://github.com/arnobt78/AnimeVault-Sever-Action--NextJS/tree/main).

---

## Technology Stack

- **Next.js 14** – React-based framework for SSR/SSG, server actions, and routing
- **React** – Component-based UI library
- **Framer Motion** – Animation and transition library
- **react-intersection-observer** – For implementing infinite scroll
- **Tailwind CSS** – Utility-first CSS framework (configured via tailwind.config.ts)
- **Node.js** – JavaScript runtime for server execution
- **Vercel** – Cloud deployment platform
- **TypeScript** – For type safety (configured via tsconfig.json)

---

## Screenshots

See images at the top of this README for a visual preview!

---

## Getting Started

### Prerequisites

- **Node.js** (Recommended: Latest LTS) – [Download Node.js](https://nodejs.org/en/)
- **A package manager**: npm, yarn, pnpm, or bun

### Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/arnobt78/AnimeVault--NextJS.git
    cd AnimeVault--NextJS
    ```

2. **Install all dependencies:**

    ```bash
    npm install
    # or
    yarn install
    # or
    pnpm install
    # or
    bun install
    ```

    You may also want to install project-specific dependencies (if not auto-installed):

    ```bash
    npm i framer-motion react-intersection-observer
    ```

### Running the Project

Start the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to view the app.

> The app supports hot-reloading; any code changes will reflect instantly.

---

## Project Structure Walkthrough

Here is a walkthrough of the key folders and files:

- **/app/**: The main Next.js app folder. Includes page routes, layouts, and server actions.
  - `page.js`: Entry point for the main landing page. This is where most homepage logic resides.
  - Other files: Additional route files (e.g., `/app/anime/[id]/page.js` for anime details), layouts, and API handlers.
- **/components/**: Contains reusable UI components (e.g., AnimeCard, Loader, Navbar). Helps keep code modular and DRY.
- **/public/**: All static assets like images, icons, and favicon.
- **/styles/**: CSS or Tailwind files for global and modular styling.
- **Config files**: `.eslintrc.json`, `next.config.js`, `tailwind.config.ts`, `postcss.config.js`, `tsconfig.json` for project setup and linting.

---

## Key Commands

| Command                 | Action                         |
|-------------------------|-------------------------------|
| `npm run dev`           | Start development server       |
| `npm run build`         | Build production assets        |
| `npm start`             | Start production server        |

---

## API & References

- **Anime Data Source:**  
  [Shikimori API Documentation](https://shikimori.one/api/doc/1.0/animes/index)
- **Tutorial Reference:**  
  [YouTube Walkthrough](https://www.youtube.com/watch?v=FKZAXFjxlJI)

---

## Main Functionalities & How It Works

### 1. Server-Side Rendering and Server Actions

AnimeVault uses Next.js 14’s server components and server actions for fetching anime data and handling user actions. This ensures fast page load, SEO optimization, and secure data fetching.

**Example server action (pseudo-code):**
```js
// In app/page.js (or a server action file)
export async function fetchAnimeList(page = 1) {
  const res = await fetch(`https://shikimori.one/api/animes?page=${page}`);
  return res.json();
}
```

---

### 2. Infinite Scroll

Utilizing `react-intersection-observer`, the app detects when the user scrolls near the bottom and loads more anime entries on-the-fly.

**Example usage:**
```js
import { useInView } from 'react-intersection-observer';

const { ref, inView } = useInView();

useEffect(() => {
  if (inView) {
    // Fetch next page
  }
}, [inView]);
```

---

### 3. Framer Motion Animations

Smooth transitions and UI effects are implemented using Framer Motion.

```js
import { motion } from 'framer-motion';

<motion.div
  initial={{ opacity: 0 }}
  animate={{ opacity: 1 }}
  transition={{ duration: 0.5 }}
>
  {/* Anime Card Content */}
</motion.div>
```

---

### 4. Routing and Dynamic Pages

Next.js routing lets each anime have its own detail page (e.g., `/anime/123`). Dynamic routes are defined in `/app/anime/[id]/page.js`.

---

### 5. Modern UI/UX

- Clean and mobile-friendly design using Tailwind CSS.
- Responsive layouts for all devices.
- Loading indicators and error handling for better UX.

---

### 6. Deployment

The app is Vercel-ready. Simply connect the repo to Vercel and deploy!

---

## Keywords

`Next.js` `React` `SSR` `Anime API` `Infinite Scroll` `Framer Motion` `Server Actions` `Vercel` `Node.js` `react-intersection-observer` `Modern Web App`

---

## Contributing

Pull requests and contributions are welcome! Please fork the repository and submit your PR.

---

## License

This project is for educational and demo purposes. For more information, contact the repository owner.

---

## Additional Notes

- Uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) for optimized font loading.
- Bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).
- For a more detailed file/folder list, visit the [GitHub Repository](https://github.com/arnobt78/AnimeVault-Sever-Action--NextJS/tree/main).

---
