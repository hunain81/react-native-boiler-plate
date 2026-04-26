# ReactNative Boilerplate

A ready-to-use boilerplate with Typescript for rapid development, featuring built-in global state management, colors, and dark light theme configurations with persistence, RTK query with reauth and token management.
## 🧩 Tech Stack

| Tool              | Purpose                                  |
| ----------------- | ---------------------------------------- |
| Expo              | React Native framework for building apps |
| TypeScript        | Static type-checking                     |
| Redux Toolkit     | Global state management                  |
| RTK Query         | API data fetching and caching            |
| Expo Secure Store | Secure Token key/value storage           |
| Expo Router       | Screen and stack navigation              |
| ESLint            | Linting and code quality                 |
| Prettier          | Code formatting                          |

## Folder Structure

```
AppName/
│
├── app/             # Contains screen routes
├── assets/          # Fonts, images, lottie etc.
├── components/      # Reusable UI components
├── constants/       # Theme colors, fonts, font sizes, error messages, and global constants
├── hooks/           # Custom React hooks
├── redux/           # Redux slices + RTK Query + Store configuration
│   ├── features/    # Redux state slices
│   └── api/         # RTK Query API + API slice with token manager and configuration
├── styles/          # Screen-specific and shared styles
└── utils/           # Centralized validation and helper functions
```

## 🚀 Features

### ✅ Pre-configured Essentials

- **Global Loader With State** — Use a loading spinner globally across screens using Redux state.
- **Dark & Light Theme With Persistence** — Dark and Light theme preconfigured Automatically persists user-selected theme across app restarts.
- **Auth Guard With Authentication Flow** — Includes the auth guard protected routes with basic authentication flow setup.
- **Token Management with Auto Re-auth**
    - Reauth when token expires with Refresh token logic for **RTK Query**.
    - Handles **race conditions** when multiple API calls happen simultaneously during token expiry.

### 🧠 State Management

- Uses **Redux Toolkit** for scalable and modular state management.
- Stores tokens securely using **Expo Secure Store** and injects them into Redux at app initialization.

### 🛠️ API Integration

- Fully set up **RTK Query** for declarative API handling.
- Token refresh interceptor and headers are injected automatically.
- Publi routes config file that exclude the auth bearer header.
- `useApiErrorHandler` custom hook for standardized API error management.

### 🎨 Theme and Fonts

- Custom hook to manage fonts — Just drop your font file and register it in `useAppFont.ts`.
- Easily switch between light and dark themes.
- Configure the colors in constant/colors file.

### ✔️ Validation System

- Centralized, reusable form field validations in `utils/validation`.

### 🧹 Code Quality Tools

- ESLint configured with standard rules.

# Project Setup Guide

This is a comprehensive guide to setting up and running the project locally using Expo. Follow the instructions below to get started.

## 🚀 Getting Started

Follow the steps below to set up and run the project locally.

---

### 1. 📥 Clone the Repository

Clone the boilerplate to your local machine:

```bash
git clone https://github.com/hunain81/react-native-boiler-plate.git
cd your-repo-name
```

### 2. 📦 Install Dependencies

Install all required packages using Yarn (recommended):

```bash
yarn install
```

Or use npm:

```bash
npm install
```

### 3. ⚙️ Start the Development Server

Start the Expo development server:

```bash
yarn expo
```

This will open the Expo Developer Tools in your browser. From there, you can launch the app on:

- Android emulator or Expo Go
- iOS simulator (Mac only) or Expo Go
- Web browser

### 4. 🧼 Clear Expo Cache (Optional)

If you run into unexpected issues, clear the cache:

```bash
npx expo start -c
```

### 5. 📝 Rename the App

Update the app name by editing `app.json`:

```json
{
    "name": "YourAppName",
    "slug": "your-app-name"
}
```

### 6. 📲 Run the App on Emulator or Device

To run on Android:

```bash
yarn android
```

To run on iOS (Mac only):

```bash
yarn ios
```

To run in a browser:

```bash
yarn web
```

### 7. 🆙 Upgrade Dependencies (Optional)

Upgrade to the latest Expo SDK and compatible versions:

```bash
npx expo upgrade
```

Then install recommended dependencies:

```bash
npx expo install
```

### 8. 💅 Configure VS Code (Recommended)

This boilerplate includes a pre-configured `.vscode/extensions.json` file that automatically recommends essential VS Code extensions when you open the project.

When prompted in VS Code, simply **click “Install All”** to set up the recommended development tools.

#### Recommended Extensions:

- ✅ **ESLint** — `dbaeumer.vscode-eslint`
- ✅ **Prettier - Code Formatter** — `esbenp.prettier-vscode`
- ✅ **Indent Rainbow** — `oderwat.indent-rainbow`
- ✅ **VSCode Icons** — `vscode-icons-team.vscode-icons`

> ℹ️ If the recommendation prompt doesn't appear, you can install them manually from the Extensions panel by searching the names above.

### 9. 🛠 VS Code Settings (Auto Formatting, ESLint, and Imports)

The project includes pre-defined settings in `.vscode/settings.json` to enforce consistent formatting and code quality.

These settings enable auto-formatting with Prettier, auto-fix ESLint issues, and automatically organize/sort imports and class members on save.

#### Included Settings:

```json
{
    "editor.tabSize": 4,
    "editor.formatOnSave": true,
    "eslint.enable": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.codeActionsOnSave": {
        "source.fixAll": "explicit",
        "source.sortMembers": "explicit"
    }
}
```

### 10. ✅ Verify Everything Works

Run the app:

```bash
yarn expo
```
- Prettier for consistent formatting.
- `.vscode/` settings included for smooth integration with recommended extensions.

---
