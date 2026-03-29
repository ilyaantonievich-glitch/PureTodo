# PureTodo

<div align="center">

![PureTodo Banner](https://img.shields.io/badge/PureTodo-Minimalist%20Todo%20App-black?style=for-the-badge)

**A beautiful, minimalist todo application with smooth animations and powerful features**

[![Features](https://img.shields.io/badge/features-6%20awesome-white?style=flat-square)](#features)
[![License](https://img.shields.io/badge/license-MIT-black?style=flat-square)](#license)
[![Vue.js](https://img.shields.io/badge/Vue.js-3-green?style=flat-square&logo=vue.js)](https://vuejs.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.0-cyan?style=flat-square&logo=tailwind-css)](https://tailwindcss.com/)

</div>

---

## Table of Contents

- [About](#about)
- [Features](#features)
- [Screenshots](#screenshots)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Customization](#customization)
- [Browser Support](#browser-support)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

---

## About

**PureTodo** is a modern, minimalist task management application designed for people who value simplicity and elegance. Built as a single-page application (SPA) in a single HTML file, it combines beautiful design with powerful functionality.

The app features a stunning black & white aesthetic with smooth animations, dark/light theme support, and bilingual interface (English/Russian). All your data is stored locally in your browser, ensuring privacy and instant access.

---

## Features

### 🎨 **Beautiful Design**
- Minimalist black & white aesthetic
- Smooth, iOS-like animations
- Glassmorphism effects
- Custom checkbox animations
- Floating background elements

### 🌓 **Theme System**
- Dark mode (default)
- Light mode
- Instant theme switching
- Persistent theme preference
- Animated transitions

### 🌐 **Bilingual Support**
- English interface
- Russian interface (Русский)
- Instant language switching
- Persistent language preference

### ✅ **Task Management**
- Create tasks with custom titles
- Set duration (Days, Weeks, Months, Years)
- Priority rating (1-5 stars)
- Subtasks support
- Mark tasks as complete
- Delete tasks
- Smooth list animations

### 📊 **Progress Tracking**
- Daily productivity rating (1-5)
- Personal journal/notes
- Interactive analytics chart
- Completed tasks counter
- Average rating display
- Journal history

### 💾 **Data Storage**
- LocalStorage-based storage
- No server required
- Complete privacy
- Automatic saving
- User accounts support

### 📱 **Mobile Optimized**
- Fully responsive design
- Touch-friendly interface
- Safe area support (notched devices)
- Instant touch feedback
- No 300ms tap delay

---

## Screenshots

### Dark Mode
```
┌─────────────────────────────────────────┐
│  🌙 PureTodo                    [EN] [🌙]│
├─────────────────────────────────────────┤
│  👤 User                          Tasks │
│     Workspace                   Progress│
├─────────────────────────────────────────┤
│  ┌─────────────────────────────────┐    │
│  │ What needs to be done?          │    │
│  │ ─────────────────────────────── │    │
│  │ 🔘 5  [Days ▼]  ⭐⭐⭐⭐⭐  [Add] │    │
│  └─────────────────────────────────┘    │
│                                          │
│  Total tasks: 3                          │
│  ┌─────────────────────────────────┐    │
│  │ ○ Complete project documentation │    │
│  │   🕐 5 days  ⭐⭐⭐⭐  [Subtasks] │    │
│  └─────────────────────────────────┘    │
└─────────────────────────────────────────┘
```

### Light Mode
Similar layout with inverted colors and soft shadows.

---

## Tech Stack

| Technology | Purpose |
|------------|---------|
| **Vue.js 3** | Reactive framework |
| **Tailwind CSS 3** | Utility-first styling |
| **Chart.js** | Analytics visualization |
| **Phosphor Icons** | Beautiful icon set |
| **Google Fonts (Inter)** | Clean typography |
| **LocalStorage API** | Data persistence |

---

## Getting Started

### Prerequisites

- Any modern web browser
- No build tools required!

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/puretodo.git
   cd puretodo
   ```

2. **Open the application**
   ```bash
   # Simply open index.html in your browser
   # Or use a local server:
   python -m http.server 8000
   # Then visit http://localhost:8000
   ```

3. **Deploy to GitHub Pages** (Optional)
   ```bash
   git push origin main
   # Enable GitHub Pages in repository settings
   ```

---

## Usage

### Creating an Account

1. Open the application
2. Enter a username and password
3. Click "Create Account"
4. You're in! Your credentials are stored locally

### Adding Tasks

1. Type your task in the input field
2. Adjust duration using `+`/`-` buttons or type directly
3. Select duration unit (Days/Weeks/Months/Years)
4. Set priority by clicking stars (1-5)
5. Click "Add" button

### Managing Subtasks

1. Click "Subtasks" on any task
2. Type subtask name and press Enter
3. Check off subtasks individually
4. Delete subtasks with the X button

### Tracking Progress

1. Navigate to "Progress" tab
2. Rate your day (1-5)
3. Add optional journal notes
4. Click "Save"
5. View your analytics chart

### Theme & Language

- Click **🌙/☀️** button (top-right) to toggle theme
- Click **EN/RU** button to switch language
- Preferences are saved automatically

---

## Project Structure

```
puretodo/
├── index.html          # Main application file (everything in one)
├── README.md           # This file
├── LICENSE             # MIT License
└── .gitignore          # Git ignore rules
```

### Inside index.html

```
index.html
├── <head>
│   ├── Tailwind CSS (CDN)
│   ├── Vue.js 3 (CDN)
│   ├── Chart.js (CDN)
│   ├── Phosphor Icons (CDN)
│   ├── Google Fonts
│   └── Custom CSS
├── <body>
│   ├── Auth Screen
│   ├── Main App
│   │   ├── Header
│   │   ├── Tasks Tab
│   │   └── Progress Tab
│   └── Vue.js Application Logic
└── <script>
    ├── Translations (EN/RU)
    ├── Vue App Setup
    ├── Auth Methods
    ├── Task Methods
    └── Progress Methods
```

---

## Customization

### Changing Colors

Edit the `tailwind.config` in `<head>`:

```javascript
tailwind.config = {
    theme: {
        extend: {
            colors: {
                brand: {
                    500: '#your-color', // Main accent color
                },
            }
        }
    }
}
```

### Modifying Animations

Edit CSS variables in `<style>`:

```css
/* Slower animations */
.list-enter-active {
    transition: all 0.8s cubic-bezier(0.16, 1, 0.3, 1);
}
```

### Adding Languages

Add to `dict` object in script:

```javascript
const dict = {
    // ... existing languages
    es: {
        loginSubtitle: 'Bienvenido de nuevo',
        // ... more translations
    }
}
```

---

## Browser Support

| Browser | Version | Support |
|---------|---------|---------|
| Chrome | 90+ | ✅ Full |
| Firefox | 88+ | ✅ Full |
| Safari | 14+ | ✅ Full |
| Edge | 90+ | ✅ Full |
| iOS Safari | 14+ | ✅ Full |
| Android Chrome | 90+ | ✅ Full |

---

## Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Guidelines

- Keep the minimalist aesthetic
- Ensure mobile responsiveness
- Test on both light and dark themes
- Add translations for new text

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2024 PureTodo

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software...
```

---

## Author

**PureTodo** was created with ❤️ for people who appreciate minimalism and productivity.

- GitHub: [@yourusername](https://github.com/yourusername)

---

<div align="center">

**Made with Vue.js & Tailwind CSS**

⭐ Star this repo if you like it!

</div>
