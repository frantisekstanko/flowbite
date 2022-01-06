---
layout: home
title: Tailwind CSS Vue - Flowbite
description: Learn how to install and set up Tailwind CSS with Flowbite for your Vue project and start developing modern web applications with interactive components
group: getting-started
toc: true

previous: React
previousLink: getting-started/react/
next: Angular
nextLink: getting-started/angular/
---

Vue is a popular front-end library used by websites such as Behance, Nintendo, Gitlab, Font Awesome, and more that you can use to build modern web applications. By installing Tailwind CSS and Flowbite you can build your project even faster using the utility-first approach from Tailwind and the interactive components from Flowbite.

## Install Tailwind CSS and Flowbite with Vue 3 and Vite

Follow the next steps to install and set up Tailwind CSS and Flowbite for your Vue 3 project using Vite.

1. Create a new Vite project running the following commands in your terminal:

```bash
npm init vite my-project
cd my-project
```

2. Install Tailwind CSS:

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

3. Configure the template paths inside the `tailwind.config.js` file:

```javascript
module.exports = {
  content: [
    "./index.html",
    "./src/**/*.{vue,js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

4. Create a new `./src/index.css` file and add the Tailwind directives:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

5. Import the newly created CSS file inside your `./src/main.js` file:

```javascript
import { createApp } from 'vue'
import App from './App.vue'

// add this
import './index.css'

createApp(App).mount('#app')
```

6. Install Flowbite by running the following command in your terminal:

```bash
npm install -D @themesberg/flowbite
```

7. Require Flowbite as a plugin inside your `tailwind.config.js` file:

```javascript
module.exports = {

    plugins: [
        require('@themesberg/flowbite/plugin')
    ]

}

```
8. Import the Flowbite JavaScript file inside your main `./src/main.js` file:

```bash
import '@themesberg/flowbite';
```

Now you can start the local server by running `npm run dev` in your terminal.

## Working with Flowbite components in Vue
