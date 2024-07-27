# Minimal Setup Project with Vite, React, and Tailwind CSS

This README will guide you through setting up a minimal project with Vite, React, and Tailwind CSS.

## Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v20.12.1 or higher)
- [npm](https://www.npmjs.com/) (v10.8.1 or higher) or [yarn](https://yarnpkg.com/) (v1.22.10 or higher)

## Getting Started

### 1. Create a Vite Project

First, create a new Vite project. You can do this using npm, yarn, or pnpm.

Using npm:

```sh
npm create vite@latest my-vite-app --template react
```

Using yarn:

```sh
yarn create vite my-vite-app --template react
```

Using pnpm:

```sh
pnpm create vite my-vite-app --template react
```

Navigate to the project directory:

```sh
cd my-vite-app
```

### 2. Install Tailwind CSS

Install Tailwind CSS and its dependencies:

npm

```sh
npm install -D tailwindcss postcss autoprefixer
```

yarn

```sh
yarn add -D tailwindcss postcss autoprefixer
```

Initialize Tailwind CSS configuration:

```sh
npx tailwindcss init -p
```

This will create `tailwind.config.js` and `postcss.config.js` files in your project.

### 3. Configure Tailwind CSS

Update `tailwind.config.js` with the paths to all of your template files:

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./index.html", "./src/**/*.{js,ts,jsx,tsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

### 4. Add Tailwind Directives to CSS

Create a new CSS file (if it doesn't exist) in the `src` directory, e.g., `src/index.css`, and add the Tailwind directives:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Ensure this CSS file is imported in your `src/main.jsx` file:

```jsx
import React from "react";
import ReactDOM from "react-dom";
import App from "./App";
import "./index.css"; // Import the Tailwind CSS file

ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById("root"),
);
```

### 5. Start the Development Server

Run the development server to see your project in action:

```sh
npm run dev
```

If you encounter any issues, ensure your configurations and file paths are correct.

## Folder Structure

Your project structure should look like this:

```
my-vite-app/
├── node_modules/
├── public/
│   └── vite.svg
├── src/
│   ├── App.jsx
│   ├── index.css
│   ├── main.jsx
│   └── ...
├── .gitignore
├── index.html
├── package.json
├── postcss.config.js
├── tailwind.config.js
└── vite.config.js
```

## Customizing Tailwind CSS

You can customize your Tailwind CSS setup by editing the `tailwind.config.js` file. For more details on customization, refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs/configuration).

## Building for Production

To build your project for production, run:

```sh
npm run build
```

This will create an optimized build in the `dist` directory.

## Conclusion

You now have a minimal setup with Vite, React, and Tailwind CSS. You can start building your application with these powerful tools. For further reading and advanced configuration, refer to the respective documentation:

- [Vite Documentation](https://vitejs.dev/)
- [React Documentation](https://reactjs.org/)
- [Tailwind CSS Documentation](https://tailwindcss.com/)

Happy coding! 🚀
