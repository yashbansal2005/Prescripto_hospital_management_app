<div align="center">
  
# 🏥 Prescripto - Doctor Appointment Web App

*A full-stack web application designed to make healthcare more accessible by simplifying the process of booking doctor appointments*

[Features](#-key-features) • [Tech Stack](#-tech-stack) • [Screenshots](#-screenshots) • [Setup](#-project-setup)

</div>

---

##  About

**Prescripto** is a comprehensive healthcare platform built using the **MERN stack** (MongoDB, Express.js, React.js, and Node.js) that provides an efficient, user-friendly experience for both patients and healthcare providers. It offers three levels of authentication: **Patient**, **Doctor**, and **Admin**, each with distinct features tailored to their roles. The app integrates **online payment gateways (Stripe and Razorpay)** to facilitate seamless and secure payments.

##  Tech Stack

- **Frontend**: React.js with Vite
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Payment Gateways**: Stripe, Razorpay
- **Authentication**: JSON Web Token (JWT)
- **Image Storage**: Cloudinary
- **Styling**: Tailwind CSS



### 🏠 Homepage - Book Appointments
![Homepage Hero](./portal/home%20page.png)
Landing page featuring easy appointment booking with trusted doctors. Users can search for doctors and explore top-rated healthcare professionals.

### 🔍 Browse Doctors by Specialty
![Find Doctors](./portal/doctors%20page.png)
Explore doctors across various specialties including General Physician, Gynecologist, Dermatologist, Pediatricians, Neurologist, and Gastroenterologist. View top doctors to book with detailed profiles.

### 👤 User Registration
![Create Account](./portal/login%20page.png)
Simple and secure account creation to book appointments and manage health records. Users need to create an account before booking appointments.

## Key Features

### 1. Three-Level Authentication

####  **Patient Login**
- Sign up and log in to book appointments with doctors
- Manage appointments (view, cancel, or reschedule)
- Secure online payment options (Cash, Stripe, Razorpay)
- Editable user profile (name, email, address, gender, birthday, profile picture)
- View upcoming and past appointments

####  **Doctor Login**
- Manage appointments and patient consultations
- Dashboard displays:
  - Total earnings from completed appointments
  - Number of patients
  - Number of appointments
  - Latest bookings
- Update profile details (description, fees, address, availability status)
- View appointment details (patient info, payment mode, appointment status)
- Mark appointments as completed or cancel them

####  **Admin Login**
- Create and manage doctor profiles
- Dashboard with comprehensive analytics:
  - Total doctors registered
  - Total appointments
  - Total patients
  - Recent bookings
- Add new doctors (image, specialty, degree, experience, address, fees, etc.)
- View and manage all appointments (cancel or mark as completed)
- Edit or delete doctor profiles

##  Application Pages

###  Home Page
- User-friendly layout with search functionality
- View top doctors and their profiles
- Browse doctors by specialty
- Explore additional sections:
  - About Us
  - Delivery Information
  - Privacy Policy
  - Get in Touch
- Footer includes navigation links

###  All Doctors Page
- Lists all available doctors
- Filter doctors by specialty
- Click on doctor profile to book appointment

###  About Page
- Information about Prescripto's vision and mission
- **Why Choose Us** section:
  - **Efficiency**: Streamlined appointment process
  - **Convenience**: Online booking and payment
  - **Personalization**: Tailored experience based on preferences

###  Contact Page
- Office address and contact details
- Job opportunities section
- Footer navigation links

###  Doctor Appointment Page
- Detailed doctor information:
  - Profile picture, qualification, experience
  - Brief description and fees
- Appointment booking form:
  - Choose date and time
  - Select payment method (Cash, Stripe, Razorpay)
- Related doctors section
- Login required to book appointments

###  User Profile
- View and edit profile information:
  - Upload profile picture
  - Update name, email, address, gender, and birthday
- View list of upcoming and past appointments
- Logout option

##  Admin Panel Features

###  Dashboard
- Statistics overview:
  - Number of doctors
  - Total appointments
  - Total patients
  - Latest bookings
- Quick actions to cancel bookings

###  Add Doctor
- Comprehensive form to add new doctors:
  - Profile image upload
  - Specialty selection
  - Email and password
  - Degree and experience
  - Address and fees
  - Description

###  Doctor List
- View all registered doctors
- Edit or delete doctor profiles

###  Appointments Management
- View all appointments:
  - Patient name and age
  - Appointment date and time
  - Doctor name
  - Fees and payment mode
- Admin actions: Cancel or Mark as Completed

##  Doctor Dashboard Features

###  Earnings Overview
- Track total earnings from completed appointments

###  Appointments List
- Detailed patient appointment information:
  - Patient name and age
  - Date and time
  - Payment mode
  - Appointment status
- Actions: Complete or Cancel appointments

###  Profile Management
- Update profile information:
  - Description
  - Consultation fees
  - Address
  - Availability status

##  Payment Integration

Prescripto supports multiple secure payment methods:
- **Cash Payment** - Pay at the clinic
- **Stripe Integration** - International card payments
- **Razorpay Integration** - Indian payment gateway
- Ensures a secure and smooth payment experience

##  Project Setup

### Prerequisites

- Node.js (v14 or higher)
- MongoDB (local or Atlas)
- Git
- Cloudinary account (for image storage)
- Stripe and Razorpay API keys (for payments)

### Installation Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/meniraj07/Prescripto-Hospital_Management_System.git
   cd Prescripto-Hospital_Management_System
   ```

2. **Install Dependencies**
   ```bash
   # Backend
   cd backend
   npm install

   # Frontend
   cd ../frontend
   npm install

   # Admin Panel
   cd ../admin
   npm install
   ```

3. **Environment Variables**

   Create `.env` files in respective directories:

   **Backend** (`backend/.env`)
   ```env
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   CLOUDINARY_NAME=your_cloudinary_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_SECRET_KEY=your_cloudinary_secret_key
   STRIPE_API_KEY=your_stripe_api_key
   RAZORPAY_API_KEY=your_razorpay_api_key
   ```

   **Frontend** (`frontend/.env`)
   ```env
   VITE_BACKEND_URL=http://localhost:4000
   ```

   **Admin** (`admin/.env`)
   ```env
   VITE_BACKEND_URL=http://localhost:4000
   ```

4. **Run the Application**

   Open three separate terminals:

   ```bash
   # Terminal 1 - Backend Server
   cd backend
   npm run server

   # Terminal 2 - Patient Frontend
   cd frontend
   npm run dev

   # Terminal 3 - Admin/Doctor Panel
   cd admin
   npm run dev
   ```

5. **Access the Application**
   - Patient Portal: http://localhost:5173
   - Admin/Doctor Panel: http://localhost:5174
   - Backend API: http://localhost:4000

## Folder Structure

```plaintext
Prescripto-Hospital_Management_System/
├── frontend/              # Patient Portal (React.js)
│   ├── src/
│   │   ├── components/   # Reusable UI components
│   │   ├── pages/        # Page components
│   │   ├── context/      # Context API for state management
│   │   └── assets/       # Images and static files
│   └── package.json
│
├── admin/                # Admin/Doctor Panel (React.js)
│   ├── src/
│   │   ├── components/   # Sidebar, Navbar
│   │   ├── pages/        # Admin and Doctor dashboards
│   │   ├── context/      # Admin, Doctor, App contexts
│   │   └── assets/       # Images and static files
│   └── package.json
│
├── backend/              # Backend API (Node.js, Express.js)
│   ├── config/           # Database and Cloudinary config
│   ├── controllers/      # API Controllers (Admin, Doctor, User)
│   ├── models/           # MongoDB Schemas
│   ├── routes/           # API Routes
│   ├── middleware/       # Authentication and Multer
│   └── server.js         # Entry point
│
└── screenshots/          # Application screenshots
```

##  Acknowledgements

- Thanks to the developers and contributors of MongoDB, Express.js, React.js, Node.js, Stripe, and Razorpay for their fantastic tools and libraries.
- Special thanks to Cloudinary for image storage solutions.

##  Author

**Niraj Kumar**

- GitHub: [@meniraj07](https://github.com/meniraj07)
- LinkedIn: [Niraj Kumar](https://www.linkedin.com/in/nirajkumar-nk/)


##  Contributing

Contributions, issues, and feature requests are welcome! Feel free to:
- Fork the repository
- Create your feature branch
- Submit pull requests
- Open issues for bugs or suggestions

##  Show your support

Give a ⭐️ if this project helped you!

---


