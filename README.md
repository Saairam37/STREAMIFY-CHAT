# ✨ Streamify Chat  
*A full-stack MERN platform for real-time language exchange*  


---

## 🎯 Project Overview  
Streamify Chat is an interactive community platform built for language learners and global communicators. It enables users to:
- Create a detailed profile including their native language and the language they wish to learn  
- Discover and connect with ideal language-partners around the world  
- Chat instantly (text) or hop into HD 1-on-1 video calls  
- Customize the look and feel of the application with **32 unique themes**  
- Leverage a modern, scalable tech stack built for real-time performance  

Designed to be both fun and effective, Streamify delivers a learning space that feels like a social platform and works like a language practice tool.

---

## 🚀 Core Features  
- **Secure Authentication** – signup, login, and JWT-based protected routes  
- **Onboarding Flow** – users define their native and learning languages, bio, location, and preferences  
- **Smart User Discovery** – browse or get recommended other users who speak your target language  
- **Friend-Request System** – build connections by sending, accepting, and managing friend requests  
- **Real-Time Chat** – 1-on-1 messaging with typing indicators, read receipts, and reactions powered by Stream Chat  
- **HD Video Calling** – seamless video calls using Stream Video SDK directly from chat windows  
- **UI Theme Switcher** – choose from 32 custom themes built with Tailwind & DaisyUI (state managed with Zustand)  
- **Modern Tech Stack**  
  - Frontend: React (via Vite), TanStack Query, Zustand, DaisyUI/Tailwind  
  - Backend: Node.js + Express, MongoDB/Mongoose, JWT  
  - Real-time APIs: Stream Chat & Stream Video  

---

## 🧰 Built With  
- Frontend: **React**, **Vite**, **Tailwind CSS**, **DaisyUI**, **Zustand**, **TanStack Query**  
- Backend: **Node.js**, **Express**, **MongoDB**, **Mongoose**, **JWT**  
- Real-time & Communication: **Stream Chat SDK**, **Stream Video SDK**  

---

## 🔧 Getting Started  
### Prerequisites  
- Node.js v18 or newer  
- NPM (or Yarn)  
- MongoDB Atlas account (or local Mongo DB instance)  
- Stream account (to obtain API key & secret)  

### Setup Instructions  
Clone the repository:  
```bash
git clone https://github.com/your-username/STREAMIFY-CHAT.git  
cd STREAMIFY-CHAT
````

#### Backend Setup (`/backend`)

1. Create a `.env` file in `backend` directory.
2. Add the following env variables:

   ```env
   PORT=5001  
   NODE_ENV=development  
   MONGO_URI=<your_mongo_connection_string>  
   STREAM_API_KEY=<your_stream_api_key>  
   STREAM_API_SECRET=<your_stream_api_secret>  
   JWT_SECRET_KEY=<your_super_secret_jwt_key>  
   ```
3. Install dependencies and start the server:

   ```bash
   npm install --prefix backend  
   npm run dev --prefix backend  
   ```

#### Frontend Setup (`/frontend`)

1. Create a `.env` file in `frontend` directory.
2. Add the following:

   ```env
   VITE_STREAM_API_KEY=<your_stream_api_key>  
   ```
3. Install dependencies and start the front-end:

   ```bash
   npm install --prefix frontend  
   npm run dev --prefix frontend  
   ```
4. Open your browser at `http://localhost:5173` (or as indicated) and explore.

---

## 📍 API Endpoints

Here’s a summary of the backend’s major endpoints:

| Method | Endpoint                               | Description                          | Protected |
| ------ | -------------------------------------- | ------------------------------------ | --------- |
| POST   | `/api/auth/signup`                     | Register a new user                  | No        |
| POST   | `/api/auth/login`                      | Login existing user                  | No        |
| POST   | `/api/auth/logout`                     | Logout & clear JWT cookie            | Yes       |
| GET    | `/api/auth/me`                         | Retrieve current user                | Yes       |
| POST   | `/api/auth/onboarding`                 | Complete onboarding profile          | Yes       |
| GET    | `/api/users`                           | Get recommended users                | Yes       |
| GET    | `/api/users/friends`                   | List of user’s friends               | Yes       |
| POST   | `/api/users/friend-request/:id`        | Send a friend request                | Yes       |
| PUT    | `/api/users/friend-request/:id/accept` | Accept a friend request              | Yes       |
| GET    | `/api/users/friend-requests`           | Incoming requests                    | Yes       |
| GET    | `/api/users/outgoing-friend-requests`  | Outgoing requests                    | Yes       |
| GET    | `/api/chat/token`                      | Generate Stream token for chat/video | Yes       |

---

## ✅ Why This Project Matters

*Language learning thrives on communication.* Many learners feel isolated or lack ready partners—Streamify bridges that gap by turning language practice into a social, real-time experience. By combining chat, video, and smart discovery in one clean app, we’ve fast-tracked the “talk to someone” part of language practice. For devs, it’s also a showcase of how to build a modern, full-stack real-time application using third-party APIs.

---

## 🧠 Future Enhancements

Here are some ideas for the next version:

* Group chats & video rooms (multi-participant)
* Voice messages & recordings
* Real-time translation or live caption support
* Gamification: badges, streaks, challenges
* Mobile (iOS/Android) version using React Native or Flutter
* More granular user filters (time zone, proficiency level, interests)
* Dark/light automatic theme based on system settings

---

## 🙌 Contributing

Contributions, issues and feature-requests are welcome!
Feel free to check out the [issues](https://github.com/Saairam37/STREAMIFY-CHAT/issues) page first. When you’re ready:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Open a Pull Request

Please make sure to update tests as appropriate.
Thanks for helping make Streamify even better!

---

Thanks for checking out Streamify Chat — happy coding & happy learning! 🚀
