# Voluntreee

Voluntreee is a comprehensive platform designed to connect volunteers with opportunities, facilitate communication, and manage various aspects of volunteer work. This project is structured into a frontend (React) and a backend (Node.js/Express).

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Application](#running-the-application)
- [Project Structure](#project-structure)
- [Available Scripts](#available-scripts)
- [Contributing](#contributing)
- [License](#license)

## Features

- **User Authentication:** Secure login and signup for volunteers and NGOs.
- **Volunteer Dashboard:** Personalized dashboard for volunteers to view opportunities, track progress, and manage profiles.
- **NGO Portal:** Dedicated portal for NGOs to post opportunities, manage volunteers, and track campaigns.
- **Opportunity Management:** Create, view, and apply for various volunteer opportunities.
- **Communication:** Features for communication between volunteers and NGOs (e.g., WhatsApp chat integration).
- **Payment Integration:** (Stripe) for donations or other financial transactions.
- **Interactive Quizzes:** Geography and Math quizzes for engagement.
- **Chatbot:** Gemini-powered chatbot for assistance.
- **Image Section:** Display of relevant images.
- **Responsive Design:** Optimized for various devices.

## Technologies Used

### Frontend

- **React.js:** A JavaScript library for building user interfaces.
- **Vite:** A fast build tool for modern web projects.
- **Tailwind CSS:** A utility-first CSS framework for rapid UI development.
- **React Router DOM:** For declarative routing in React applications.
- **Axios:** Promise-based HTTP client for making API requests.
- **Firebase:** For backend services like authentication and potentially database.
- **Leaflet & React-Leaflet:** For interactive maps.
- **React Icons:** A collection of popular icon packs.
- **Recharts:** A composable charting library built with React.
- **ESLint:** For code linting.

### Backend

- **Node.js:** JavaScript runtime environment.
- **Express.js:** A fast, unopinionated, minimalist web framework for Node.js.
- **CORS:** Middleware for enabling Cross-Origin Resource Sharing.
- **Dotenv:** Loads environment variables from a `.env` file.
- **Stripe:** For payment processing.
- **Axios:** Promise-based HTTP client.
- **Multer:** Middleware for handling `multipart/form-data`, primarily used for uploading files.
- **Node-fetch:** A light-weight module that brings `window.fetch` to Node.js.
- **@mastra/voice-murf:** (Potentially for voice-related features).
- **@gradio/client:** (Potentially for integrating with Gradio applications).

## Getting Started

To get a local copy up and running, follow these steps.

### Prerequisites

- Node.js (LTS version recommended)
- npm (comes with Node.js)

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/voluntreee.git
    cd voluntreee
    ```

2.  **Install backend dependencies:**
    ```bash
    cd backend
    npm install
    ```

3.  **Install frontend dependencies:**
    ```bash
    cd ../frontend
    npm install
    ```

4.  **Install root dependencies (if any):**
    ```bash
    cd ..
    npm install # This will install firebase if not already installed
    ```

### Running the Application

1.  **Start the backend server:**
    ```bash
    cd backend
    npm start
    ```
    The backend server will typically run on `http://localhost:5000` (or another port specified in your `.env` file or `server.js`).

2.  **Start the frontend development server:**
    ```bash
    cd ../frontend
    npm run dev
    ```
    The frontend application will typically run on `http://localhost:5173` (or another port specified by Vite).

    Open your browser and navigate to the frontend URL to access the application.

### Environment Variables

Both the frontend and backend require environment variables for proper functioning. Create `.env` files in both the `backend` and `frontend` directories.

**`backend/.env` example:**

```
PORT=5000
STRIPE_SECRET_KEY=sk_test_YOUR_STRIPE_SECRET_KEY
# Add any other backend-specific environment variables here
```

**`frontend/.env` example:**

```
VITE_FIREBASE_API_KEY=YOUR_FIREBASE_API_KEY
VITE_FIREBASE_AUTH_DOMAIN=YOUR_FIREBASE_AUTH_DOMAIN
VITE_FIREBASE_PROJECT_ID=YOUR_FIREBASE_PROJECT_ID
VITE_FIREBASE_STORAGE_BUCKET=YOUR_FIREBASE_STORAGE_BUCKET
VITE_FIREBASE_MESSAGING_SENDER_ID=YOUR_FIREBASE_MESSAGING_SENDER_ID
VITE_FIREBASE_APP_ID=YOUR_FIREBASE_APP_ID
VITE_FIREBASE_MEASUREMENT_ID=YOUR_FIREBASE_MEASUREMENT_ID
VITE_STRIPE_PUBLISHABLE_KEY=pk_test_YOUR_STRIPE_PUBLISHABLE_KEY
# Add any other frontend-specific environment variables here
```

Make sure to replace placeholder values with your actual API keys and configurations.

## Project Structure

```
.
├── .gitignore
├── package-lock.json
├── package.json
├── README.md
├── backend/
│   ├── package-lock.json
│   ├── package.json
│   ├── payment.js
│   └── server.js
└── frontend/
    ├── .gitignore
    ├── eslint.config.js
    ├── index.html
    ├── package-lock.json
    ├── package.json
    ├── README.md
    ├── vite.config.js
    ├── public/
    │   └── vite.svg
    └── src/
        ├── App.jsx
        ├── index.css
        ├── main.jsx
        ├── assets/
        │   ├── image.jpg
        │   ├── ... (other images)
        │   └── react.svg
        ├── components/
        │   ├── .env
        │   ├── Communication.jsx
        │   ├── Dashboard.jsx
        │   ├── DonateButton.jsx
        │   ├── Footer.jsx
        │   ├── FrontlineWorker.jsx
        │   ├── GeminiChatbot.jsx
        │   ├── GeographyQuiz.jsx
        │   ├── Herosection.jsx
        │   ├── ImageSection.jsx
        │   ├── Landingpage.jsx
        │   ├── Login.jsx
        │   ├── MathQuiz.jsx
        │   ├── Navbar.jsx
        │   ├── NccPortal.jsx
        │   ├── NGOHome.jsx
        │   ├── OpportunitiesSection.jsx
        │   ├── ParticipantsChart.jsx
        │   ├── PricingSection.jsx
        │   ├── QuizHome.jsx
        │   ├── SignUp.jsx
        │   ├── useSlowConnection.jsx
        │   ├── VolunteerDashboard.jsx
        │   ├── VolunteerHome.jsx
        │   ├── VolunteerOpportunities.jsx
        │   ├── VolunteerOpportunitiesWrapper.jsx
        │   ├── VolunteerProfile.jsx
        │   ├── VolunteerQuiz.jsx
        │   └── WhatsAppChatButton.jsx
        └── config/
            └── firebase.js
```

## Available Scripts

### Backend

In the `backend` directory, you can run:

-   `npm start`: Starts the Node.js server.

### Frontend

In the `frontend` directory, you can run:

-   `npm run dev`: Starts the development server with Vite.
-   `npm run build`: Builds the project for production.
-   `npm run lint`: Runs ESLint to check for code quality issues.
-   `npm run preview`: Serves the production build locally.

## License

This project is licensed under the ISC License. See the `LICENSE` file for details.
