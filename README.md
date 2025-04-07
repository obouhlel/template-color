# Template Color

![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Next.js](https://img.shields.io/badge/next.js-%23000000.svg?style=for-the-badge&logo=next.js&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)

A versatile template project featuring dynamic theme switching capabilities with multiple color schemes and dark/light mode support.

## 🚀 Project Structure

```
template-color/
├── eslint.config.mjs        # ESLint configuration
├── next.config.ts           # Next.js configuration
├── package.json             # Project dependencies
├── postcss.config.mjs       # PostCSS configuration for Tailwind
├── tsconfig.json            # TypeScript configuration
├── src/
│   ├── app/                 # Next.js App Router
│   │   ├── layout.tsx       # Root layout with ThemeProvider
│   │   └── page.tsx         # Home page
│   ├── components/          # React components
│   │   ├── Header.tsx       # Header with theme controls
│   │   ├── ThemeProvider.tsx # Theme context provider
│   │   └── ThemeScript.tsx  # Script for FOUC prevention
│   ├── styles/              # CSS styles
│   │   ├── colors/          # Theme color CSS files
│   │   │   ├── amber.css    # Individual color theme
│   │   │   ├── blue.css     # Individual color theme
│   │   │   └── ...          # Other theme colors
│   │   └── globals.css      # Global styles
│   └── utils/               # Utility functions
│       └── colors.ts        # Color theme definitions
```

## ⚙️ Tech Stack

- **Next.js**: The latest version of Next.js for React framework with powerful features for production
- **Tailwind CSS v4**: The newest version of Tailwind for utility-first CSS
- **React Context API**: For global state management of theme settings
- **FOUC Prevention**: Custom solution to prevent Flash of Unstyled Content during page loads

## 🎨 Features

- **Dynamic Theme Switching**: Switch between light and dark modes
- **Multiple Color Schemes**: Choose from various color themes (blue, red, green, amber, etc.)
- **Persistent Preferences**: User theme choices stored in localStorage
- **System Preference Detection**: Automatically detects system dark/light preference

## 🏁 Getting Started

1. Clone the repository:

   ```
   git clone https://github.com/obouhlel/template-color.git
   ```

2. Install dependencies:

   ```
   npm install
   ```

3. Start the development server:
   ```
   npm run dev
   ```

## 📱 How it Works

The theme system works through several key components:

1. **ThemeScript.tsx**: Injects a script into the HTML head that runs before React hydration to set initial theme classes based on localStorage or system preferences
2. **ThemeProvider.tsx**: A React context provider that manages theme state and provides methods to change theme settings
3. **Header.tsx**: UI components that allow users to toggle between themes
4. **CSS Files**: Theme-specific CSS variables in the `/styles/colors/` directory

This architecture prevents the Flash of Unstyled Content (FOUC) that commonly happens with theme switching in React applications.

## 👤 Author

- GitHub: [@obouhlel](https://github.com/obouhlel)

---

Feel free to fork and customize this template for your own projects!
