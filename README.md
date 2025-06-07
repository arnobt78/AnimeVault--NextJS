# AnimeVault--NextJS

![project25](https://github.com/user-attachments/assets/08b14faa-3e9a-4fb2-a794-2e82c35980ac) ![Screenshot 2024-09-16 at 13 57 39](https://github.com/user-attachments/assets/b0ea18a0-e6cd-4d69-b222-018de87b8fe9)

---

## Project Overview

AnimeVault is a modern anime listing and browsing platform built with **Next.js 14**. It leverages server-side rendering, Server Actions, infinite scroll, and smooth Framer Motion animations. The application fetches anime data in real time from a robust server-side API, delivering a seamless and interactive experience for anime enthusiasts.

**Live Demo:** https://anime-vault-arnob.vercel.app/

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
- [Key Commands](#key-commands)
- [API & References](#api--references)
- [Keywords](#keywords)
- [Contributing](#contributing)
- [License](#license)

---

## Features

- **Next.js 14** with Server Actions
- Fully server-side rendered pages for maximum performance
- **Infinite Scroll** for seamless anime browsing
- **Framer Motion** for smooth UI animations
- Responsive, mobile-friendly design
- Real-time data fetching from public anime API
- Modern UI/UX with dynamic routing and transitions
- Easy to deploy (Vercel ready)

---

## Project Structure

```
AnimeVault--NextJS/
├── app/                # Main Next.js app folder (pages, layouts, components)
│   ├── page.js         # Main landing page
│   └── ...             # Other app-specific files
├── public/             # Static assets
├── styles/             # Global and modular CSS
├── package.json        # Project dependencies and scripts
├── README.md           # Project documentation
└── ...
```

> **Note:** The main entry point for editing the landing page is `app/page.js`.

---

## Technology Stack

- **Next.js 14** – React Framework for SSR/SSG
- **React** – UI Library
- **Framer Motion** – Animations
- **react-intersection-observer** – Infinite Scroll
- **Node.js** – Runtime
- **Vercel** – Deployment

---

## Screenshots

Look above

---

## Getting Started

### Prerequisites

- **Node.js** (Recommended version: LTS). [Download Node.js](https://nodejs.org/en/)
- **npm**, **yarn**, **pnpm**, or **bun** package manager (one is enough)

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

   You may need to install project-specific packages:

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

> The app supports hot-reloading; any changes you make to the code will reflect instantly.

---

## Key Commands

| Command                 | Action                      |
| ----------------------- | -------------------------- |
| `npm run dev`           | Start development server    |
| `npm run build`         | Create production build     |
| `npm start`             | Start production server     |

---

## API & References

- **Anime Data Source:**  
  [Shikimori API Documentation](https://shikimori.one/api/doc/1.0/animes/index)
- **Tutorial Reference:**  
  [YouTube Walkthrough](https://www.youtube.com/watch?v=FKZAXFjxlJI)

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

- This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) for optimized font loading.
- Bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

---
