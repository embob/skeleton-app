# Skeleton App

A modern, production-ready React starter template with TypeScript, Vite, Tailwind CSS, and comprehensive tooling for development, testing, and code quality.

## ✨ Features

- ⚡ **Vite** - Lightning-fast build tool and dev server with Hot Module Replacement (HMR)
- ⚛️ **React 19** - Latest React with modern hooks and features
- 🎨 **Tailwind CSS v4** - Utility-first CSS framework for rapid UI development
- 🔷 **TypeScript** - Full type safety for better developer experience
- ✅ **Vitest** - Fast unit testing framework with React Testing Library
- 🔍 **Biome** - Fast code linter, formatter, and analyzer (replaces ESLint)
- 📦 **Minimal Dependencies** - Lean and focused project setup

## 🚀 Quick Start

### Prerequisites
- Node.js 16+ (recommended 18+)
- npm or yarn

### Installation

```bash
# Clone the repository
git clone <repository-url>
cd skeleton-app

# Install dependencies
npm install

# Start development server
npm run dev
```

The app will be available at `http://localhost:5173`

## 📚 Available Scripts

```bash
# Development
npm run dev          # Start development server with HMR

# Production
npm run build        # Build for production (outputs to dist/)
npm run preview      # Preview production build locally

# Code Quality
npm run lint         # Check code with Biome linter
npm run format       # Format code with Biome formatter
npm test             # Run tests with Vitest

# Watch Mode
npm test -- --watch  # Run tests in watch mode
```

## 🗂️ Project Structure

```
skeleton-app/
├── src/
│   ├── App.tsx           # Main App component
│   ├── App.css           # App styles
│   ├── App.test.tsx      # App tests
│   ├── main.tsx          # Application entry point
│   ├── index.css         # Global styles (imports Tailwind)
│   ├── assets/           # Static assets
│   └── test/
│       └── setup.ts      # Vitest configuration
├── public/               # Public static files
├── index.html            # HTML template
├── vite.config.ts        # Vite configuration
├── tsconfig.json         # TypeScript configuration
├── biome.json            # Biome linting/formatting config
└── package.json          # Project dependencies
```

## 🛠️ Tech Stack

### Core
- **React 19.1** - UI library
- **TypeScript 5.9** - Type-safe JavaScript
- **Vite 7** - Build tool and dev server

### Styling
- **Tailwind CSS 4** - Utility-first CSS
- **Tailwind CSS Vite Plugin** - Vite integration

### Testing
- **Vitest 3** - Unit testing framework
- **React Testing Library** - Component testing utilities
- **jsdom** - DOM implementation for tests

### Code Quality
- **Biome 2** - All-in-one toolchain for code quality
  - Fast linting
  - Code formatting
  - Import organization

## 📝 Development Guidelines

### Code Style

This project uses **Biome** for all code quality needs:

- **Linting**: Catch potential bugs and enforce best practices
- **Formatting**: Keep code style consistent
- **Import sorting**: Automatically organize imports

Run before committing:
```bash
npm run lint     # Check for issues
npm run format   # Auto-fix formatting
```

### Component Structure

Keep components simple and focused:

```typescript
// src/components/Button.tsx
interface ButtonProps {
  label: string;
  onClick: () => void;
}

export default function Button({ label, onClick }: ButtonProps) {
  return (
    <button
      onClick={onClick}
      className="px-4 py-2 bg-blue-500 text-white rounded hover:bg-blue-600"
    >
      {label}
    </button>
  );
}
```

### Testing

Write tests for your components:

```typescript
// src/components/Button.test.tsx
import { render, screen } from "@testing-library/react";
import Button from "./Button";

test("renders button with label", () => {
  render(<Button label="Click me" onClick={() => {}} />);
  expect(screen.getByText("Click me")).toBeInTheDocument();
});
```

Run tests with:
```bash
npm test
npm test -- --watch  # Watch mode
```

### Styling

Use Tailwind CSS classes for styling:

```typescript
<div className="min-h-screen grid place-items-center bg-gradient-to-br from-blue-50 to-indigo-100">
  <h1 className="text-4xl font-bold text-gray-900">Welcome</h1>
</div>
```

See [Tailwind CSS Documentation](https://tailwindcss.com/docs) for available utilities.

## 🔧 Configuration

### Biome Settings (`biome.json`)

- **Formatter**: 2-space indentation, 100-character line width
- **Linter**: Recommended rules enabled
- **VCS Integration**: Git integration enabled
- **Build Output**: `dist/` folder excluded from linting

### TypeScript Settings (`tsconfig.json`)

- **Target**: ES2022
- **Module**: ESNext
- **Strict Mode**: Enabled for better type safety
- **JSX**: React 17+ automatic runtime

### Vite Settings (`vite.config.ts`)

- **HMR**: Hot Module Replacement enabled
- **React Plugin**: Fast Refresh support
- **Tailwind**: Automatic CSS processing
- **Tests**: jsdom environment, global test APIs

## 🎯 Best Practices

1. **Use TypeScript** - Define types for props, state, and functions
2. **Keep Components Small** - Aim for single responsibility
3. **Test Critical Logic** - Write tests for important components
4. **Format Before Committing** - Run `npm run format` before git commit
5. **Check Lint Issues** - Run `npm run lint` and fix warnings
6. **Use Tailwind Classes** - Avoid inline styles when possible
7. **Optimize Imports** - Keep import statements organized

## 📦 Dependency Management

This project has been optimized to include only necessary dependencies:

**Runtime Dependencies** (3):
- react
- react-dom
- tailwindcss (with Vite plugin)

**Dev Dependencies** (10):
- Build: vite, @vitejs/plugin-react
- Testing: vitest, jsdom, @testing-library/react, @testing-library/jest-dom
- Code Quality: @biomejs/biome
- Types: typescript, @types/react, @types/react-dom

## 🚀 Deployment

### Build for Production

```bash
npm run build
```

This creates an optimized build in the `dist/` folder.

### Deploy Options

- **Vercel**: Connect your Git repo, automatic deployments
- **Netlify**: Drag and drop `dist/` folder or connect Git
- **GitHub Pages**: Push `dist/` folder to `gh-pages` branch
- **Docker**: Create a Dockerfile to containerize the app

## 📖 Resources

- [React Documentation](https://react.dev)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- [Vite Guide](https://vitejs.dev/)
- [Tailwind CSS Docs](https://tailwindcss.com/docs)
- [Vitest Documentation](https://vitest.dev/)
- [Biome Documentation](https://biomejs.dev/)

## 📄 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

---

**Happy coding!** 🎉
