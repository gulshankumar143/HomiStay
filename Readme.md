# HomiStay

HomiStay is a full-stack web application designed to facilitate the listing, discovery, and review of homestay accommodations. Inspired by platforms like Airbnb, it allows users to browse, create, and manage property listings, as well as leave reviews for their stays.

## Features

- **User Authentication:** Secure signup and login functionality for users.
- **Listings Management:** Users can create, edit, and delete their own property listings with details and images.
- **Reviews:** Guests can leave reviews and ratings for listings they have stayed at.
- **Responsive UI:** Clean and modern interface with EJS templating and custom CSS.
- **Error Handling:** Robust error handling and user feedback throughout the app.

## Project Structure

```
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

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
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

- Node.js
- Express.js
- MongoDB & Mongoose
- EJS (Embedded JavaScript Templates)
- CSS (Custom styles)

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any enhancements or bug fixes.

## API Endpoints Overview

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

- **Guest:** Can browse listings and view details.
- **Registered User:** Can create listings, leave reviews, and manage their own content.
- **Listing Owner:** Can edit or delete their own listings.
- **Review Author:** Can delete their own reviews.

## Deployment & Environment

To deploy this app:
1. Set up a MongoDB database (e.g., MongoDB Atlas).
2. Configure environment variables in `.env`:
   - `DB_URL` — MongoDB connection string
   - `SECRET` — Session secret
   - `CLOUDINARY_*` — (if using image uploads)

## License

This project is licensed under the MIT License.
