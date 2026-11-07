<div align="center">

# Granite AI Playground

A **React + Vite** playground for experimenting with **IBM Granite** models — a chat interface with global loading-state management.

[![Status](https://img.shields.io/badge/status-prototype-orange?style=flat-square)](#)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=flat-square&logo=react&logoColor=black)](https://react.dev)
[![Vite](https://img.shields.io/badge/Vite-5-646CFF?style=flat-square&logo=vite&logoColor=white)](https://vitejs.dev)
[![Tailwind](https://img.shields.io/badge/Tailwind%20CSS-4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)](https://tailwindcss.com)
[![IBM Granite](https://img.shields.io/badge/IBM-Granite-0F62FE?style=flat-square&logo=ibm&logoColor=white)](https://www.ibm.com/granite)

**English** · [Bahasa Indonesia](README.id.md)

</div>

---

## About

A chat-interface experiment for **IBM Granite** models. It exists to test what interacting with Granite over an API actually feels like, and to practise the **global loading state** pattern in React using Context.

The code is deliberately kept small so it can serve as a starting point for other projects.

## Features

- **Chat interface** — send a prompt and render the model's response.
- **Global loading state** — a `LoadingContext` plus a `useLoading` hook, so every component shows the same indicator.
- **Auto-scroll** — the message list scrolls as new data arrives.
- **Tailwind CSS 4** through the Vite plugin (`@tailwindcss/vite`).
- **Deploy-ready** — a Netlify config is included.

## Tech Stack

| Layer | Technology |
| --- | --- |
| Framework | React 18 |
| Bundler | Vite |
| Styling | Tailwind CSS 4 (`@tailwindcss/vite`) |
| HTTP | Axios |
| Lint | ESLint 9 (flat config) |
| Deployment | Netlify |

## Getting Started

### 1. Clone and install

```bash
git clone https://github.com/Ilhamaji/granite-ai-playground.git
cd granite-ai-playground
npm install
```

### 2. Environment

```env
VITE_GRANITE_API_URL=your_endpoint_here
VITE_GRANITE_API_KEY=your_key_here
```

### 3. Run

```bash
npm run dev          # development
npm run build        # production build to dist/
npm run preview      # preview the build
npm run lint         # ESLint
```

## Project Layout

```
src/
  main.jsx                     # React entrypoint
  App.jsx                      # app composition
  context/LoadingContext.jsx   # provider + useLoading hook
  pages/Home.jsx               # main page (input and message list)
public/
index.html
netlify.toml                   # deploy config + SPA redirect
```

## Notes

This is an **experiment**, not a production app — there is no chat history persistence, no authentication, and no thorough error handling. The code documentation lives in `README.md` because the project doubles as practice in describing an architecture.

## License

MIT.

---

<div align="center">
Built by <a href="https://github.com/Ilhamaji">Ilham Aji</a>
</div>
