
<div align="center">
   <h1>🏡 HomiStay</h1>
   <p>
      <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white"/>
      <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white"/>
      <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white"/>
      <img src="https://img.shields.io/badge/EJS-8C8C8C?style=for-the-badge&logo=ejs&logoColor=white"/>
      <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white"/>
   </p>
   <p><b>Full-stack homestay listing and review platform</b></p>
</div>

# HomiStay [Live Demo](https://homistay-leme.onrender.com)

HomiStay is a full-stack web application designed to facilitate the <b>listing, discovery, and review</b> of homestay accommodations. Inspired by platforms like Airbnb, it allows users to browse, create, and manage property listings, as well as leave reviews for their stays.


## Features

## ✨ Features

- 🔐 **User Authentication:** Secure signup and login functionality for users.
- 🏠 **Listings Management:** Users can create, edit, and delete their own property listings with details and images.
- ⭐ **Reviews:** Guests can leave reviews and ratings for listings they have stayed at.
- 📱 **Responsive UI:** Clean and modern interface with EJS templating and custom CSS.
- 🛡️ **Error Handling:** Robust error handling and user feedback throughout the app.

## Project Structure

## 🗂️ Project Structure

```text
app.js                # Main application entry point
cloudConfig.js        # Cloud storage configuration (e.g., for images)
middleware.js         # Custom middleware for authentication, error handling, etc.
package.json          # Project dependencies and scripts
schema.js             # Data validation schemas

controllers/          # Route controllers for listings, reviews, and users
init/                 # Database seeding and initialization scripts
models/               # Mongoose models for listings, reviews, and users
public/               # Static assets (CSS, JS)
routes/               # Express route definitions
utils/                # Utility classes and functions
views/                # EJS templates for UI rendering
```

## Getting Started
## 🚀 Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/gulshankumar143/HomiStay
   cd HomiStay
   ```
2. **Install dependencies:**
   ```bash
   npm install
   ```
3. **Set up environment variables:**
   - Create a `.env` file for sensitive configuration (e.g., database URI, API keys).
4. **Run the application:**
   ```bash
   npm start
   ```
## Technologies Used

## 🛠️ Technologies Used

- ![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white) Node.js
- ![Express.js](https://img.shields.io/badge/Express.js-000000?logo=express&logoColor=white) Express.js
- ![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?logo=mongodb&logoColor=white) MongoDB & Mongoose
- ![EJS](https://img.shields.io/badge/EJS-8C8C8C?logo=ejs&logoColor=white) EJS (Embedded JavaScript Templates)
- ![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white) CSS (Custom styles)

## Contributing

## 🤝 Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any enhancements or bug fixes.


## API Endpoints Overview

## 📚 API Endpoints Overview

The application follows RESTful conventions. Key endpoints include:

- `GET /listings` — View all listings
- `GET /listings/:id` — View a single listing
- `POST /listings` — Create a new listing (authenticated)
- `PUT /listings/:id` — Edit a listing (owner only)
- `DELETE /listings/:id` — Delete a listing (owner only)
- `POST /listings/:id/reviews` — Add a review (authenticated)
- `DELETE /listings/:id/reviews/:reviewId` — Delete a review (author only)
- `GET /users/login` — Login page
- `POST /users/login` — Login action
- `GET /users/signup` — Signup page
- `POST /users/signup` — Signup action

## User Roles & Permissions

## 👤 User Roles & Permissions

- 👀 **Guest:** Can browse listings and view details.
- 📝 **Registered User:** Can create listings, leave reviews, and manage their own content.
- 🏠 **Listing Owner:** Can edit or delete their own listings.
- ⭐ **Review Author:** Can delete their own reviews.

## Deployment & Environment

## 🚢 Deployment & Environment

To deploy this app:
1. Set up a MongoDB database (e.g., MongoDB Atlas).
2. Configure environment variables in `.env`:
   - `DB_URL` — MongoDB connection string
   - `SECRET` — Session secret
   - `CLOUDINARY_*` — (if using image uploads)
3. Deploy to a Node.js hosting provider (e.g., Render, Vercel, Heroku).
