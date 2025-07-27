# ✈️ Flight Booking System

A modern, full-stack flight booking platform built with React, TypeScript, Node.js, Express, and MongoDB. This application provides a seamless experience for users to search, book, and manage flight reservations with integrated payment processing.

![Flight Booking Banner](https://via.placeholder.com/1200x300/6366f1/ffffff?text=SkyQuest+Flight+Booking+System)

## 🌟 Features

### 🔐 User Authentication
- **User Registration** with email and phone verification
- **OTP-based email verification** for secure account activation
- **JWT-based authentication** with secure token management
- **Login/Logout** functionality with persistent sessions

### ✈️ Flight Management
- **Flight Search** with departure/arrival airports and dates
- **Real-time flight data** integration
- **Flight filtering** by price, duration, and airlines
- **Responsive flight cards** with detailed information

### 💳 Payment Integration
- **Razorpay payment gateway** integration
- **Secure payment processing** with order management
- **Payment verification** and booking confirmation
- **Transaction history** and receipts

### 🎨 Modern UI/UX
- **Responsive design** that works on all devices
- **Smooth animations** with Framer Motion
- **Modern gradient designs** and glass-morphism effects
- **Intuitive navigation** with dynamic routing

### 📱 Additional Features
- **User Profile Management** with booking history
- **About & Contact Pages** with interactive elements
- **Email notifications** for bookings and updates
- **Error handling** with user-friendly messages

## 🛠️ Technology Stack

### Frontend
- **React 18** - Modern React with hooks
- **TypeScript** - Type-safe development
- **Vite** - Fast build tool and development server
- **Tailwind CSS** - Utility-first CSS framework
- **Framer Motion** - Smooth animations and transitions
- **React Router Dom** - Client-side routing
- **React Hook Form** - Form handling with validation
- **Axios** - HTTP client for API requests
- **React Hot Toast** - Beautiful notification system

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JWT** - JSON Web Token authentication
- **bcryptjs** - Password hashing
- **Nodemailer** - Email sending service
- **Razorpay** - Payment gateway integration

## 🚀 Quick Start

### Prerequisites
Make sure you have the following installed:
- **Node.js** (v16 or higher)
- **MongoDB** (v5 or higher)
- **Git**
- **Code Editor** (VS Code recommended)

### 📁 Project Structure
```
FlightBooking/
├── backend_new/                 # Backend API server
│   ├── src/
│   │   ├── config/             # Configuration files
│   │   ├── controllers/        # Route controllers
│   │   ├── middleware/         # Custom middleware
│   │   ├── models/            # Database models
│   │   └── routes/            # API routes
│   ├── tests/                 # Test files
│   └── package.json
├── frontend/                   # React frontend
│   ├── src/
│   │   ├── components/        # Reusable components
│   │   ├── pages/            # Page components
│   │   ├── context/          # React context
│   │   ├── services/         # API services
│   │   ├── types/            # TypeScript types
│   │   └── utils/            # Utility functions
│   └── package.json
└── README.md
```

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/NitinTheGreat/FlightBooking.git
cd FlightBooking
```

### 2. Backend Setup

#### Navigate to backend directory:
```bash
cd backend_new
```

#### Install dependencies:
```bash
npm install
```

#### Create environment file:
Create a `.env` file in the `backend_new` directory with the following variables:

```env
# Database Configuration
MONGO_URI=mongodb://localhost:27017/flightbooking

# JWT Configuration
JWT_SECRET=your_super_secure_jwt_secret_key_here

# Razorpay Configuration (Get from Razorpay Dashboard)
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret

# Email Configuration (Gmail)
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_specific_password

# Server Configuration
PORT=5000
NODE_ENV=development
```

#### Start the backend server:
```bash
npm run dev
```

The backend server will start on `http://localhost:5000`

### 3. Frontend Setup

#### Open a new terminal and navigate to frontend directory:
```bash
cd frontend
```

#### Install dependencies:
```bash
npm install
```

#### Create environment file:
Create a `.env` file in the `frontend` directory:

```env
# API Configuration
VITE_API_URL=http://localhost:5000

# Razorpay Configuration
VITE_RAZORPAY_KEY_ID=your_razorpay_key_id

# Aviation API (Optional - for real flight data)
VITE_AVIATION_API_KEY=your_aviation_api_key
```

#### Start the frontend development server:
```bash
npm run dev
```

The frontend will start on `http://localhost:5173`

## 🔧 Configuration Guide

### Database Setup
1. **Install MongoDB** locally or use MongoDB Atlas
2. **Create a database** named `flightbooking`
3. **Update connection string** in your `.env` file

### Email Setup (Gmail)
1. **Enable 2-factor authentication** on your Gmail account
2. **Generate an app-specific password**:
   - Go to Google Account settings
   - Security → App passwords
   - Generate password for "Mail"
3. **Use this app password** in your `.env` file

### Razorpay Setup
1. **Create Razorpay account** at [razorpay.com](https://razorpay.com)
2. **Get API keys** from Dashboard → Settings → API Keys
3. **Add keys** to both frontend and backend `.env` files

## 📚 API Documentation

### Authentication Endpoints
```
POST /api/auth/register     # User registration
POST /api/auth/verify-otp   # OTP verification
POST /api/auth/login        # User login
GET  /api/auth/me          # Get current user
```

### Payment Endpoints
```
POST /api/payment/create-order    # Create payment order
POST /api/payment/verify-payment  # Verify payment
GET  /api/payment/bookings        # Get user bookings
```

## 🎨 Features Showcase

### Home Page
- **Hero section** with flight search form
- **Popular destinations** carousel
- **Features showcase** with animations
- **Customer testimonials** slider

### Authentication Flow
- **Sign up** with name, email, password, and phone
- **OTP verification** via email
- **Secure login** with JWT tokens
- **Profile management** with booking history

### Flight Search & Booking
- **Search flights** by departure/arrival cities and dates
- **View flight details** with pricing and schedules
- **Select and book** flights with passenger information
- **Payment processing** through Razorpay
- **Booking confirmation** with reference number

## 🧪 Testing

### Backend Testing
```bash
cd backend_new
npm test
```

### Frontend Testing
```bash
cd frontend
npm run test
```

## 🚀 Deployment

### Option 1: Manual Deployment

#### Backend (Node.js hosting)
1. Deploy to platforms like **Heroku**, **Railway**, or **DigitalOcean**
2. Set environment variables on your hosting platform
3. Ensure MongoDB connection string points to cloud database

#### Frontend (Static hosting)
1. Build the frontend:
   ```bash
   npm run build
   ```
2. Deploy `dist` folder to **Netlify**, **Vercel**, or **GitHub Pages**

### Option 2: Docker Deployment
```bash
# Build and run with Docker Compose
docker-compose up --build
```

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. **Fork the repository**
2. **Create a feature branch**:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make your changes** and add tests if applicable
4. **Commit your changes**:
   ```bash
   git commit -m "Add your feature description"
   ```
5. **Push to your branch**:
   ```bash
   git push origin feature/your-feature-name
   ```
6. **Create a Pull Request**

## 📝 Environment Variables Reference

### Backend (.env)
| Variable | Description | Required |
|----------|-------------|----------|
| `MONGO_URI` | MongoDB connection string | ✅ |
| `JWT_SECRET` | Secret key for JWT tokens | ✅ |
| `RAZORPAY_KEY_ID` | Razorpay public key | ✅ |
| `RAZORPAY_KEY_SECRET` | Razorpay secret key | ✅ |
| `EMAIL_USER` | Gmail email address | ✅ |
| `EMAIL_PASS` | Gmail app password | ✅ |
| `PORT` | Server port (default: 5000) | ❌ |

### Frontend (.env)
| Variable | Description | Required |
|----------|-------------|----------|
| `VITE_API_URL` | Backend API URL | ✅ |
| `VITE_RAZORPAY_KEY_ID` | Razorpay public key | ✅ |
| `VITE_AVIATION_API_KEY` | Aviation API key | ❌ |

## 🐛 Troubleshooting

### Common Issues

#### Backend won't start:
- ✅ Check if MongoDB is running
- ✅ Verify all environment variables are set
- ✅ Ensure port 5000 is not in use

#### Frontend build errors:
- ✅ Delete `node_modules` and reinstall
- ✅ Check Node.js version (v16+)
- ✅ Verify environment variables

#### Payment issues:
- ✅ Confirm Razorpay keys are correct
- ✅ Check if test mode is enabled for development

## 📄 License

This project is licensed under the **ISC License** - see the [LICENSE](LICENSE) file for details.

## 🎯 Future Enhancements

- [ ] **Multi-city flights** support
- [ ] **Real-time flight tracking**
- [ ] **Seat selection** interface
- [ ] **Mobile app** with React Native
- [ ] **Admin dashboard** for flight management
- [ ] **Loyalty program** integration
- [ ] **Social login** (Google, Facebook)
- [ ] **Multi-language** support
- [ ] **Push notifications**
- [ ] **Advanced search filters**

## 👥 Team

- **Frontend Development**: React, TypeScript, Tailwind CSS
- **Backend Development**: Node.js, Express, MongoDB
- **UI/UX Design**: Modern, responsive design
- **Payment Integration**: Razorpay gateway
- **Email Services**: Nodemailer with Gmail

## 📞 Support

If you encounter any issues or have questions:

1. **Check the documentation** above
2. **Search existing issues** on GitHub
3. **Create a new issue** with detailed information
4. **Contact the development team**

---

<div align="center">

**Made with ❤️ by the SkyQuest Team**

[![GitHub stars](https://img.shields.io/github/stars/NitinTheGreat/FlightBooking)](https://github.com/NitinTheGreat/FlightBooking/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/NitinTheGreat/FlightBooking)](https://github.com/NitinTheGreat/FlightBooking/network)
[![GitHub issues](https://img.shields.io/github/issues/NitinTheGreat/FlightBooking)](https://github.com/NitinTheGreat/FlightBooking/issues)

</div>