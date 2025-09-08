# RoomEase - Hotel Listing and Booking Application

A full-stack hotel listing and booking application built with React, Node.js, Express, and MongoDB. RoomEase allows users to list their properties, browse available accommodations, and manage bookings seamlessly.

## 🚀 Features

### User Authentication
- **User Registration & Login** - Secure authentication with JWT tokens
- **Role-based Access** - Support for both regular users and admin roles
- **Session Management** - Persistent login sessions with cookies

### Property Management
- **Add Properties** - Hotel owners can list their properties with detailed information
- **Edit Properties** - Update property details, photos, and amenities
- **Delete Properties** - Remove properties from listings
- **Photo Upload** - Cloudinary integration for image storage and management
- **Property Details** - Comprehensive property information including:
  - Title, address, and description
  - Amenities and perks
  - Check-in/check-out times
  - Maximum guest capacity
  - Pricing information

### Booking System
- **Browse Properties** - View all available accommodations
- **Property Details** - Detailed view of individual properties
- **Make Bookings** - Book properties with check-in/check-out dates
- **Booking Management** - View, accept, reject, and cancel bookings
- **Booking Status Tracking** - Track booking status (pending, accepted, rejected)

### User Interface
- **Responsive Design** - Modern, mobile-friendly interface
- **Beautiful UI** - Gradient backgrounds and glassmorphism effects
- **Interactive Components** - Smooth animations and transitions
- **Toast Notifications** - Real-time feedback for user actions

## 🛠️ Tech Stack

### Frontend
- **React 19** - Modern React with hooks and functional components
- **Redux Toolkit** - State management for authentication and data
- **React Router DOM** - Client-side routing
- **Tailwind CSS** - Utility-first CSS framework
- **Axios** - HTTP client for API requests
- **React Toastify** - Toast notifications
- **React Icons** - Icon library
- **Vite** - Fast build tool and development server

### Backend
- **Node.js** - JavaScript runtime environment
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JWT** - JSON Web Tokens for authentication
- **bcryptjs** - Password hashing
- **Cloudinary** - Cloud-based image storage
- **Multer** - File upload handling
- **CORS** - Cross-origin resource sharing
- **Cookie Parser** - Cookie parsing middleware

## 📁 Project Structure

```
RoomEase-Hotel-Listing-and-Booking-Application/
├── backend/
│   ├── src/
│   │   ├── controller/          # API route handlers
│   │   │   ├── auth.controller.js
│   │   │   ├── booking.controller.js
│   │   │   └── place.controller.js
│   │   ├── lib/                 # Utility functions
│   │   │   ├── connectdb.js
│   │   │   ├── jwtVerify.js
│   │   │   └── protectRoute.js
│   │   ├── models/              # Database schemas
│   │   │   ├── auth.model.js
│   │   │   ├── booking.model.js
│   │   │   └── place.model.js
│   │   ├── routes/              # API routes
│   │   │   ├── auth.route.js
│   │   │   ├── booking.route.js
│   │   │   └── place.route.js
│   │   └── server.js            # Main server file
│   ├── package.json
│   └── package-lock.json
├── frontend/
│   ├── src/
│   │   ├── app/
│   │   │   └── store.js         # Redux store configuration
│   │   ├── components/          # Reusable UI components
│   │   │   ├── AccountNav.jsx
│   │   │   ├── AddPlace.jsx
│   │   │   ├── BookingForm.jsx
│   │   │   ├── BookingPage.jsx
│   │   │   ├── BookingReq.jsx
│   │   │   ├── EditPlace.jsx
│   │   │   ├── Footer.jsx
│   │   │   ├── Navbar.jsx
│   │   │   ├── PhotoUploader.jsx
│   │   │   ├── PlaceForm.jsx
│   │   │   ├── ProfileComp1.jsx
│   │   │   └── ProfileSection.jsx
│   │   ├── features/            # Redux slices
│   │   │   ├── auth/
│   │   │   │   └── authSlice.js
│   │   │   ├── booking/
│   │   │   │   └── bookingSlice.js
│   │   │   └── place/
│   │   │       └── placeSlice.js
│   │   ├── lib/
│   │   │   └── axiosInstance.js # Axios configuration
│   │   ├── pages/               # Page components
│   │   │   ├── BookingInfoPage.jsx
│   │   │   ├── HomePage.jsx
│   │   │   ├── HotelPage.jsx
│   │   │   ├── LandingPage.jsx
│   │   │   ├── Login.jsx
│   │   │   ├── ProfilePage.jsx
│   │   │   └── SignUp.jsx
│   │   ├── App.jsx              # Main app component
│   │   ├── Layout.jsx           # Layout wrapper
│   │   └── main.jsx             # App entry point
│   ├── public/                  # Static assets
│   ├── package.json
│   └── vite.config.js
└── Readme.md
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (local or cloud instance)
- Cloudinary account (for image storage)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd RoomEase-Hotel-Listing-and-Booking-Application
   ```

2. **Backend Setup**
   ```bash
   cd backend
   npm install
   ```

3. **Frontend Setup**
   ```bash
   cd ../frontend
   npm install
   ```

### Environment Variables

Create a `.env` file in the backend directory with the following variables:

```env
# Database
MONGO_URI=your_mongodb_connection_string

# Server
PORT=5000
CLIENT_URL=http://localhost:5173

# JWT
JWT_SECRET=your_jwt_secret_key

# Cloudinary
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
```

Create a `.env` file in the frontend directory:

```env
VITE_API_URL=http://localhost:5000
```

### Running the Application

1. **Start the Backend Server**
   ```bash
   cd backend
   npm start
   ```
   The server will run on `http://localhost:5000`

2. **Start the Frontend Development Server**
   ```bash
   cd frontend
   npm run dev
   ```
   The application will be available at `http://localhost:5173`

## 📱 Usage

### For Property Owners
1. **Register/Login** - Create an account or sign in
2. **Add Property** - Navigate to "Add Place" to list your property
3. **Manage Bookings** - View and respond to booking requests
4. **Edit Properties** - Update property information as needed

### For Guests
1. **Browse Properties** - View all available accommodations on the homepage
2. **View Details** - Click on any property to see detailed information
3. **Make Booking** - Select dates and book your stay
4. **Track Bookings** - View your booking history and status

## 🔧 API Endpoints

### Authentication
- `POST /auth/signup` - User registration
- `POST /auth/login` - User login
- `POST /auth/logout` - User logout
- `GET /auth/check` - Check authentication status

### Places
- `GET /` - Get all places
- `POST /addplace` - Add a new place
- `GET /showplaces` - Get user's places
- `PUT /editplace/:id` - Update a place
- `POST /deleteplace/:id` - Delete a place
- `GET /place/:id` - Get single place details

### Bookings
- `POST /booking/:id` - Create a booking
- `GET /bookings` - Get user's bookings
- `GET /bookingreq` - Get booking requests (for owners)
- `POST /acceptbooking/:id` - Accept a booking
- `POST /rejectbooking/:id` - Reject a booking
- `POST /deletebooking/:id` - Delete a booking
- `GET /booking/:id` - Get booking details

### File Upload
- `POST /upload` - Upload images to Cloudinary

## 🎨 UI/UX Features

- **Modern Design** - Clean, professional interface with gradient backgrounds
- **Responsive Layout** - Works seamlessly on desktop, tablet, and mobile
- **Interactive Elements** - Hover effects, smooth transitions, and animations
- **Glassmorphism Effects** - Modern glass-like UI components
- **Toast Notifications** - Real-time feedback for all user actions
- **Loading States** - Proper loading indicators for better UX

## 🔒 Security Features

- **JWT Authentication** - Secure token-based authentication
- **Password Hashing** - bcrypt for secure password storage
- **Protected Routes** - Route protection for authenticated users
- **CORS Configuration** - Proper cross-origin resource sharing
- **Input Validation** - Server-side validation for all inputs

## 🚀 Deployment

### Backend Deployment
1. Deploy to platforms like Heroku, Railway, or DigitalOcean
2. Set up MongoDB Atlas for cloud database
3. Configure environment variables on the hosting platform

### Frontend Deployment
1. Build the production version: `npm run build`
2. Deploy to platforms like Vercel, Netlify, or GitHub Pages
3. Update the API URL in environment variables

**RoomEase** - Making hotel booking simple and elegant! 🏨✨
