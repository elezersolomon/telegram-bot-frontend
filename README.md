# Telegram Bot Frontend Portal


This is the frontend for the VisionFund (VFMFI) Telegram Bot management portal. It provides a comprehensive web interface for administrators and users to manage bot interactions, users, customers, content, and view reports. The application is built with React, TypeScript, and Material-UI.

## Key Features

*   **Role-Based Access Control**: Separate dashboards and functionalities for `Admin` and `User` roles.
*   **Admin Dashboard**:
    *   Statistical overview of portal users by role and status, and new user creation trends.
    *   Full CRUD (Create, Read, Update, Delete) functionality for portal users.
    *   View and manage all customer leads from the Telegram bot.
    *   View customer feedback.
    *   Dynamically edit bot content, including "About Us," "Contact Us," product information, and FAQs.
    *   Generate and view reports on customer registration, portal users, and leads with date and status filters.
*   **User Dashboard**:
    *   Statistical overview of customer leads by their status (New, InProgress, Contacted).
    *   View and manage assigned customer leads.
    *   Update the status and assigned area for customer leads.
    *   View customer feedback and generate reports.
    *   Head office users have additional permissions to edit bot content.
*   **Secure Authentication**: JWT-based login system for portal users.
*   **State Management**: Centralized state management using Redux Toolkit, with encrypted state persistence via `redux-persist`.

## Tech Stack

*   **Framework**: React
*   **Language**: TypeScript
*   **UI Library**: Material-UI (MUI)
*   **Styling**: Tailwind CSS
*   **Routing**: React Router
*   **State Management**: Redux Toolkit & Redux Persist
*   **API Communication**: Axios
*   **Data Visualization**: Recharts
*   **Build Tool**: Create React App (with `react-app-rewired`)

## Getting Started

Follow these instructions to get a local copy of the project up and running for development and testing purposes.

### Prerequisites

*   Node.js (v16 or later)
*   npm or yarn

### Installation

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/elezersolomon/telegram-bot-frontend.git
    cd telegram-bot-frontend
    ```

2.  **Install dependencies:**
    ```sh
    npm install
    # or
    yarn install
    ```

3.  **Create an environment file:**

    Create a `.env` file in the root of the project and add the following environment variables.

    ```env
    # The base URL for the backend API
    REACT_APP_SERVER_BASE_URL=http://localhost:5000/api

    # A secret key for encrypting the persisted Redux state
    REACT_APP_REDUX_PERSIST_KEY=your-secret-key-here
    ```

4.  **Run the development server:**
    ```sh
    npm start
    ```
    The application will be available at `http://localhost:3000`.

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in development mode.
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.
The page will reload when you make changes. You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.

### `npm run build`

Builds the app for production to the `build` folder.
It correctly bundles React in production mode and optimizes the build for the best performance. The build is minified and the filenames include hashes.
Your app is ready to be deployed!

## Project Structure

The project follows a standard React application structure:

```
.
├── public/              # Static assets and index.html
└── src/
    ├── assets/          # Images and other static files
    ├── components/      # Reusable React components (Layout, Modals, etc.)
    ├── models/          # TypeScript interfaces and type definitions
    ├── pages/           # Page components for each route
    ├── redux/           # Redux store, slices, and persistence configuration
    ├── services/        # API calls and data fetching logic
    ├── utils/           # Utility functions (axios instance, date formatting)
    ├── App.tsx          # Main application component
    ├── index.tsx        # Application entry point
    └── routes.tsx       # Routing configuration using React Router
