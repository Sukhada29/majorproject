# 🏡 WanderLust – Full-Stack Property Booking Platform

A full-stack web application inspired by Airbnb, enabling users to list, discover, and book properties with a secure and intuitive experience. Built with Node.js, Express, MongoDB, and EJS using an MVC architecture.

---

## 🌐 Live Demo

> https://majorproject-cdai.onrender.com

---

## 📸 Screenshots

> _Add 2–3 screenshots of your app here after uploading them to the repo_
> Example:
> <img width="1916" height="1006" alt="Screenshot 2026-06-04 182329" src="https://github.com/user-attachments/assets/d786754f-e434-46f8-899c-baee74200729" />

> <img width="1919" height="946" alt="Screenshot 2026-06-04 181220" src="https://github.com/user-attachments/assets/998360e1-3ffd-4010-a2e8-77e7eda5ac02" />


---

## ✨ Features

- 🔐 **User Authentication** – Secure sign up, login, and logout using Passport.js with session management
- 🏠 **Property Listings** – Create, read, update, and delete property listings with image uploads
- ☁️ **Cloud Image Storage** – Property images stored and served via Cloudinary
- 🗺️ **Map Integration** – Location-based property display using Mapbox
- ✍️ **Reviews & Ratings** – Authenticated users can post and delete reviews on listings
- 🛡️ **Authorization** – Only listing/review owners can edit or delete their content
- ✅ **Input Validation** – Server-side schema validation using Joi
- 📱 **Responsive Design** – Mobile-friendly UI built with Bootstrap 5

---

## 🛠️ Tech Stack

| Layer | Technology |
|------------|--------------------------------------|
| Backend | Node.js, Express.js |
| Frontend | EJS (Embedded JavaScript Templates) |
| Database | MongoDB, Mongoose |
| Auth | Passport.js, express-session |
| Storage | Cloudinary, Multer |
| Maps | Mapbox GL JS |
| Validation | Joi |
| Styling | Bootstrap 5, Custom CSS |

---

## 📁 Project Structure

```
majorproject/
├── controllers/       # Route handler logic (MVC controllers)
├── models/            # Mongoose schemas (User, Listing, Review)
├── routes/            # Express route definitions
├── views/             # EJS templates
│   ├── listings/      # Listing pages (index, show, new, edit)
│   ├── users/         # Login & signup pages
│   └── layouts/       # Shared layout (boilerplate)
├── public/            # Static assets (CSS, JS, images)
├── utils/             # Helper utilities (ExpressError, wrapAsync)
├── init/              # Database seed data
├── middleware.js      # Custom middleware (auth checks, etc.)
├── cloudConfig.js     # Cloudinary configuration
├── schema.js          # Joi validation schemas
└── app.js             # Main Express app entry point
```

---

## ⚙️ Getting Started

### Prerequisites

Make sure you have the following installed:
- [Node.js](https://nodejs.org/) (v16+)
- [MongoDB](https://www.mongodb.com/) (local or Atlas)
- A [Cloudinary](https://cloudinary.com/) account
- A [Mapbox](https://www.mapbox.com/) account

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Sukhada29/majorproject.git
   cd majorproject
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**

   Create a `.env` file in the root directory:
   ```env
   ATLASDB_URL=your_mongodb_connection_string
   SECRET=your_session_secret_key

   CLOUD_NAME=your_cloudinary_cloud_name
   CLOUD_API_KEY=your_cloudinary_api_key
   CLOUD_API_SECRET=your_cloudinary_api_secret

   MAP_TOKEN=your_mapbox_token
   ```

4. **(Optional) Seed the database**
   ```bash
   node init/index.js
   ```

5. **Start the server**
   ```bash
   node app.js
   ```

6. Open your browser and visit `http://localhost:8080`

---

## 🔑 Key Implementation Details

- **MVC Architecture** – Clean separation of concerns with dedicated controllers, models, and views
- **Error Handling** – Centralized async error handling via `wrapAsync` utility and custom `ExpressError` class
- **Flash Messages** – User feedback on actions using `connect-flash`
- **Secure Sessions** – Session stored in MongoDB using `connect-mongo` for persistence
- **Cloudinary Integration** – Images uploaded via Multer and stored on Cloudinary CDN

---

## 🚀 Deployment

This app is configured for cloud deployment. Steps for deploying on **Render**:

1. Push your code to GitHub
2. Create a new Web Service on [Render](https://render.com)
3. Set all environment variables from your `.env` file in the Render dashboard
4. Set the start command to `node app.js`
5. Deploy!

---

## 👩‍💻 Author

**Sukhada Harsulkar**

- GitHub: [@Sukhada29](https://github.com/Sukhada29)
- LinkedIn: [sukhada-harsulkar-221592258](https://linkedin.com/in/sukhada-harsulkar-221592258)
- Email: sukhadasharsulkar@gmail.com

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
