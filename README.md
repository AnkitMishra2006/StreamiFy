# StreamiFy 🌍💬

**StreamiFy** is a modern language learning social platform that connects language learners worldwide through real-time chat and video calls. Built with the MERN stack and powered by Stream.io, it creates meaningful connections between native speakers and language learners.

## ✨ Features

### 🔐 Authentication & Onboarding

- **Secure Authentication**: JWT-based authentication with HTTP-only cookies
- **Profile Setup**: Complete onboarding with language preferences, bio, and location
- **Random Avatars**: Auto-generated profile pictures for quick setup

### 👥 Social Networking

- **Smart Recommendations**: Find language partners based on native/learning language compatibility
- **Friend System**: Send, receive, and manage friend requests
- **User Profiles**: View detailed profiles with language skills and location

### 💬 Real-time Communication

- **Chat Messaging**: Powered by Stream Chat for instant messaging
- **Video Calls**: HD video calling with Stream Video SDK
- **Channel Management**: Automatic chat channel creation between friends

### 🎨 User Experience

- **Multiple Themes**: 20+ beautiful themes including light, dark, cupcake, and forest
- **Responsive Design**: Optimized for desktop and mobile devices
- **Language Flags**: Visual language indicators for better UX
- **Real-time Notifications**: Live friend request and message notifications

## 🛠️ Tech Stack

### Frontend

- **React 19** - Modern UI library with latest features
- **Vite** - Lightning-fast build tool
- **React Router** - Client-side routing
- **TanStack Query** - Server state management
- **Tailwind CSS** - Utility-first CSS framework
- **DaisyUI** - Beautiful component library
- **Zustand** - Lightweight state management
- **Stream Chat React** - Real-time chat components
- **Stream Video React SDK** - Video calling components

### Backend

- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JSON Web Tokens** - Secure authentication
- **bcryptjs** - Password hashing
- **Stream Chat** - Chat backend infrastructure
- **CORS** - Cross-origin resource sharing

### External Services

- **Stream.io** - Chat and video infrastructure
- **MongoDB Atlas** - Cloud database hosting
- **Iran Avatar API** - Random profile picture generation

## 📁 Project Structure

```
StreamiFy/
├── backend/
│   ├── src/
│   │   ├── controllers/         # Request handlers
│   │   │   ├── auth.controller.js
│   │   │   ├── chat.controller.js
│   │   │   └── user.controller.js
│   │   ├── middleware/          # Custom middleware
│   │   │   └── auth.middleware.js
│   │   ├── models/              # Database schemas
│   │   │   ├── User.js
│   │   │   └── FriendRequest.js
│   │   ├── routes/              # API routes
│   │   │   ├── auth.route.js
│   │   │   ├── chat.route.js
│   │   │   └── user.route.js
│   │   ├── lib/                 # Utilities
│   │   │   ├── db.js
│   │   │   └── stream.js
│   │   └── server.js            # Application entry point
│   └── package.json
├── frontend/
│   ├── src/
│   │   ├── components/          # Reusable UI components
│   │   ├── pages/               # Application pages
│   │   ├── hooks/               # Custom React hooks
│   │   ├── lib/                 # API and utilities
│   │   ├── store/               # State management
│   │   └── constants/           # Application constants
│   └── package.json
└── package.json                 # Root package configuration
```

## 🚀 Getting Started

### Prerequisites

- **Node.js** (v18 or higher)
- **MongoDB** database
- **Stream.io** account (for chat and video features)

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/AnkitMishra2006/StreamiFy.git
   cd StreamiFy
   ```

2. **Install dependencies**

   ```bash
   # Install all dependencies (backend + frontend)
   npm run build
   ```

3. **Environment Variables**

   Create `.env` file in the `backend` directory:

   ```env
   # Database
   MONGO_URI=your_mongodb_connection_string

   # Authentication
   JWT_SECRET=your_jwt_secret_key

   # Stream.io Configuration
   STREAM_API_KEY=your_stream_api_key
   STREAM_API_SECRET=your_stream_api_secret

   # Server Configuration
   PORT=3000
   NODE_ENV=development
   ```

   Create `.env` file in the `frontend` directory:

   ```env
   VITE_STREAM_API_KEY=your_stream_api_key
   ```

4. **Start the development servers**

   **Backend:**

   ```bash
   cd backend
   npm run dev
   ```

   **Frontend:**

   ```bash
   cd frontend
   npm run dev
   ```

5. **Access the application**
   - Frontend: `http://localhost:5173`
   - Backend API: `http://localhost:3000`

## 📚 API Endpoints

### Authentication

- `POST /api/auth/signup` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `POST /api/auth/onboarding` - Complete user profile
- `GET /api/auth/me` - Get current user

### User Management

- `GET /api/users` - Get recommended users
- `GET /api/users/friends` - Get user's friends
- `POST /api/users/friend-request/:id` - Send friend request
- `PUT /api/users/friend-request/:id/accept` - Accept friend request
- `GET /api/users/friend-requests` - Get friend requests
- `GET /api/users/outgoing-friend-requests` - Get outgoing requests

### Chat & Video

- `GET /api/chat/token` - Get Stream authentication token

## 🎯 Key Features Explained

### Language Matching System

The platform intelligently matches users based on complementary language skills:

- **Native speakers** are recommended to those learning their language
- **Language learners** can find native speakers for practice
- **Mutual learning** opportunities for users with compatible language pairs

### Friend Request System

- Send friend requests to interesting language partners
- Accept/decline incoming requests with detailed user profiles
- Track outgoing requests to avoid duplicates
- Real-time notifications for new connections

### Integrated Communication

- **Chat**: Instant messaging with rich features powered by Stream Chat
- **Video Calls**: High-quality video calls using Stream Video SDK
- **Call Integration**: Start video calls directly from chat conversations

### Theme Customization

Choose from 20+ carefully designed themes:

- Light/Dark modes for different preferences
- Colorful themes like Cupcake, Forest, Emerald
- Consistent styling across all components

## 🔧 Development Scripts

### Root Directory

```bash
npm run build    # Install dependencies for both frontend and backend
npm start        # Start production backend server
```

### Backend

```bash
npm run dev      # Start development server with nodemon
npm start        # Start production server
```

### Frontend

```bash
npm run dev      # Start Vite development server
npm run build    # Build for production
npm run preview  # Preview production build
npm run lint     # Run ESLint
```

## 🌟 Contributing

We welcome contributions! Please follow these steps:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/amazing-feature`)
3. **Commit your changes** (`git commit -m 'Add amazing feature'`)
4. **Push to the branch** (`git push origin feature/amazing-feature`)
5. **Open a Pull Request**

### Development Guidelines

- Follow the existing code style and conventions
- Write clear commit messages
- Test your changes thoroughly
- Update documentation when necessary

## 📄 License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Ankit Kumar Mishra**

- GitHub: [@AnkitMishra2006](https://github.com/AnkitMishra2006)
- Project: [StreamiFy](https://github.com/AnkitMishra2006/StreamiFy)

## 🙏 Acknowledgments

- **Stream.io** for providing excellent chat and video infrastructure
- **MongoDB** for reliable database services
- **Vercel/Netlify** for deployment platform
- **Iran Avatar API** for profile picture generation
- **DaisyUI** for beautiful UI components

## 🔮 Future Enhancements

- [ ] **Group Chat Rooms** - Language-specific group conversations
- [ ] **Voice Messages** - Audio message support in chats
- [ ] **Language Progress Tracking** - Learning progress analytics
- [ ] **Scheduled Meetings** - Plan language exchange sessions
- [ ] **Mobile App** - React Native implementation
- [ ] **AI Language Assistant** - Integrated language learning tools
- [ ] **Cultural Exchange** - Share cultural insights and experiences
- [ ] **Language Challenges** - Gamified learning activities

---

**Happy Language Learning! 🎉**

Connect with learners worldwide and master new languages together on StreamiFy!
