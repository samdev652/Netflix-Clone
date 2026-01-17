# 🎬 Netflix Clone

A modern, fully-functional Netflix clone built with React and Firebase, featuring user authentication, dynamic content browsing, and video playback capabilities using The Movie Database (TMDb) API.

![Netflix Clone](https://img.shields.io/badge/React-19.1.0-blue)
![Firebase](https://img.shields.io/badge/Firebase-12.0.0-orange)
![Vite](https://img.shields.io/badge/Vite-6.3.5-purple)
![License](https://img.shields.io/badge/license-MIT-green)

## ✨ Features

### 🔐 Authentication
- **User Sign Up & Sign In** - Create new accounts or log in with existing credentials
- **Firebase Authentication** - Secure email/password authentication
- **Protected Routes** - Automatic redirection based on authentication state
- **Session Management** - Persistent login sessions with Firebase

### 🎥 Content Browsing
- **Dynamic Movie Categories**
  - Popular on Netflix
  - Blockbuster Movies
  - Top Rated
  - Upcoming Releases
  - Now Playing
- **TMDb API Integration** - Real-time movie data and images
- **Horizontal Scrolling** - Smooth carousel navigation through movie categories
- **Movie Thumbnails** - High-quality backdrop images from TMDb

### 🎞️ Video Player
- **Embedded YouTube Trailers** - Watch movie trailers directly in the app
- **Dynamic Video Loading** - Automatic trailer fetching based on movie selection
- **Player Controls** - Full-screen support and standard video controls
- **Back Navigation** - Easy return to browsing interface

### 🎨 User Interface
- **Netflix-Inspired Design** - Authentic Netflix look and feel
- **Responsive Layout** - Optimized for desktop, tablet, and mobile devices
- **Dynamic Navbar** - Scroll-triggered background color change
- **Hero Banner** - Eye-catching hero section with featured content
- **Profile Dropdown** - Quick access to sign out functionality
- **Dark Theme** - Comfortable viewing experience

### 🔔 User Experience
- **Toast Notifications** - Real-time feedback for user actions
- **Loading Spinners** - Visual feedback during authentication
- **Smooth Animations** - Polished transitions and hover effects
- **Error Handling** - User-friendly error messages

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:
- **Node.js** (v14 or higher)
- **npm** or **yarn**
- **Git**

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/samdev652/Netflix-Clone.git
   cd Netflix-Clone
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up Firebase**
   - Create a Firebase project at [Firebase Console](https://console.firebase.google.com/)
   - Enable Email/Password authentication
   - Create a Firestore database
   - Copy your Firebase configuration
   - Update `src/firebase.js` with your credentials: 
     ```javascript
     const firebaseConfig = {
       apiKey: "YOUR_API_KEY",
       authDomain: "YOUR_AUTH_DOMAIN",
       projectId:  "YOUR_PROJECT_ID",
       storageBucket: "YOUR_STORAGE_BUCKET",
       messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
       appId: "YOUR_APP_ID"
     };
     ```

4. **Set up TMDb API**
   - Get an API key from [The Movie Database](https://www.themoviedb.org/settings/api)
   - Replace the Bearer token in `src/components/TitleCards/TitleCards.jsx` and `src/pages/Player/Player.jsx`

5. **Start the development server**
   ```bash
   npm run dev
   ```

6. **Open your browser**
   - Navigate to `http://localhost:5173`

## 🛠️ Tech Stack

### Frontend
- **React 19.1.0** - UI library for building interactive interfaces
- **React Router DOM 7.6.3** - Client-side routing
- **Vite 6.3.5** - Fast build tool and development server
- **CSS3** - Custom styling with responsive design

### Backend & Services
- **Firebase 12.0.0** - Backend-as-a-Service
  - Authentication
  - Firestore Database
- **TMDb API** - Movie data and images

### Additional Libraries
- **react-firebase-hooks 5.1.1** - React hooks for Firebase
- **react-toastify 11.0.5** - Toast notifications
- **ESLint** - Code linting and quality

## 📁 Project Structure

```
Netflix-Clone/
├── public/               # Static assets
├── src/
│   ├── assets/          # Images, icons, and media files
│   │   └── cards/       # Card data
│   ├── components/      # Reusable components
│   │   ├── Footer/      # Footer component
│   │   ├── Navbar/      # Navigation bar
│   │   └── TitleCards/  # Movie cards carousel
│   ├── pages/           # Page components
│   │   ├── Home/        # Home page
│   │   ├── Login/       # Authentication page
│   │   └── Player/      # Video player page
│   ├── App.jsx          # Main app component with routing
│   ├── firebase.js      # Firebase configuration and methods
│   ├── main.jsx         # Application entry point
│   └── index.css        # Global styles
├── index.html           # HTML template
├── package.json         # Dependencies and scripts
├── vite.config.js       # Vite configuration
└── eslint.config.js     # ESLint configuration
```

## 🎯 Key Components

### Authentication Flow
- Users are redirected to login page if not authenticated
- Firebase `onAuthStateChanged` monitors authentication state
- Automatic navigation after successful login/signup

### Movie Categories
- **Now Playing** - Currently showing movies
- **Top Rated** - Highest-rated films
- **Popular** - Most popular content
- **Upcoming** - Soon-to-be-released movies

### Routing
- `/` - Home page (protected)
- `/login` - Authentication page
- `/player/:id` - Video player with movie trailer

## 📱 Responsive Design

The application is fully responsive with breakpoints:
- **Desktop** - Full layout with all features
- **Tablet** (≤1024px) - Optimized spacing and layout
- **Mobile** (≤800px) - Simplified navigation and compact design
- **Small Mobile** (≤500px) - Minimal layout for small screens

## 🔒 Security Notes

⚠️ **Important**: The current implementation has hardcoded API keys and tokens in the source code. For production:

1. **Move sensitive data to environment variables**
   ```javascript
   const apiKey = import.meta.env.VITE_TMDB_API_KEY;
   ```

2. **Create a `.env` file**
   ```env
   VITE_FIREBASE_API_KEY=your_api_key
   VITE_TMDB_API_KEY=your_tmdb_key
   ```

3. **Add `.env` to `.gitignore`**

## 📝 Available Scripts

```bash
npm run dev      # Start development server
npm run build    # Build for production
npm run preview  # Preview production build
npm run lint     # Run ESLint
```

## 🎨 Features in Detail

### Home Page
- Hero banner with featured content
- Multiple horizontal scrolling movie categories
- Sticky navigation bar with scroll effects
- Footer with social links

### Login Page
- Toggle between Sign In and Sign Up
- Form validation
- Loading states
- Error handling with toast notifications

### Player Page
- Embedded YouTube trailers
- Movie information display
- Back navigation to previous page

## 🤝 Contributing

Contributions are welcome! Feel free to:
1. Fork the project
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is created for educational purposes. Netflix and its logo are trademarks of Netflix, Inc. 

## 🙏 Acknowledgments

- [Netflix](https://netflix.com) - Design inspiration
- [The Movie Database (TMDb)](https://www.themoviedb.org/) - Movie data and images
- [Firebase](https://firebase.google.com/) - Authentication and database
- [React](https://react.dev/) - UI framework
- [Vite](https://vite.dev/) - Build tool

## 📧 Contact

**Your Name** - [@samdev652](https://github.com/samdev652)

**Project Link:** [https://github.com/samdev652/Netflix-Clone](https://github.com/samdev652/Netflix-Clone)

---

⭐ If you found this project helpful, please give it a star! 
