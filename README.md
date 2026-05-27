<div align="center">
  <br/>
  <img src="https://img.shields.io/badge/-%F0%9F%8F%A5%20PRESCRIPTO-6C63FF?style=for-the-badge&labelColor=1a1a2e&color=6C63FF" alt="Prescripto" height="50"/>
  <br/>
  <h3>Book Appointments With Trusted Doctors</h3>
  <p><i>A full-stack healthcare platform connecting patients with doctors — seamlessly.</i></p>

  <br/>

  <a href="https://prescripto-frontend.vercel.app">
    <img src="https://img.shields.io/badge/🌐 Patient App-Live Demo-6C63FF?style=for-the-badge&logoColor=white" />
  </a>
  &nbsp;
  <a href="https://prescripto-admin-pink.vercel.app">
    <img src="https://img.shields.io/badge/⚙️ Admin Panel-Live Demo-0F3460?style=for-the-badge&logoColor=white" />
  </a>
  &nbsp;
  <a href="https://github.com/Sahil-Mansuri-15/Prescripto">
    <img src="https://img.shields.io/badge/GitHub-Source Code-181717?style=for-the-badge&logo=github" />
  </a>

  <br/><br/>

  <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
  <img src="https://img.shields.io/badge/Tailwind CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" />
  <img src="https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white" />
  <img src="https://img.shields.io/badge/Cloudinary-3448C5?style=flat-square&logo=cloudinary&logoColor=white" />
  <img src="https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white" />
  <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white" />
  <img src="https://img.shields.io/badge/Render-46E3B7?style=flat-square&logo=render&logoColor=black" />

  <br/><br/>

</div>

---

## 📌 Overview

**Prescripto** is a production-ready, full-stack doctor appointment booking web application. It offers three separate interfaces — a **patient portal**, a **doctor dashboard**, and an **admin control panel** — all powered by a single RESTful backend API.

Patients can discover doctors by speciality, pick available time slots, and complete payments securely via Stripe. Doctors manage their schedules and earnings. Admins control the entire platform from one place.

---

---

## ⚡ Features At a Glance

<table>
  <tr>
    <td valign="top" width="33%">

### 👤 Patient
- Register & login securely
- Browse doctors by speciality
- View doctor profiles & fees
- Book available time slots
- Pay via **Stripe**
- View & cancel appointments
- Upload & update profile photo

    </td>
    <td valign="top" width="33%">

### 🩺 Doctor
- Dedicated doctor login
- Personal earnings dashboard
- Accept / complete / cancel appointments
- Update availability & fees
- Manage profile photo

    </td>
    <td valign="top" width="33%">

### ⚙️ Admin
- Add doctors with image upload
- Manage all doctors & availability
- View all platform appointments
- Cancel any appointment
- Platform-wide dashboard stats

    </td>
  </tr>
</table>

---

## 🛠️ Tech Stack

| Category | Technology |
|----------|-----------|
| **Frontend** | React.js 18, Vite, Tailwind CSS, Context API, React Router DOM v6 |
| **Backend** | Node.js, Express.js |
| **Database** | MongoDB Atlas, Mongoose ODM |
| **Auth** | JSON Web Tokens (JWT), bcrypt password hashing |
| **Payments** | Stripe Checkout Sessions |
| **File Storage** | Cloudinary, Multer |
| **Deployment** | Vercel (Frontend + Admin), Render (Backend) |

---

## 🗂️ Project Structure

```
Prescripto/
│
├── 📁 frontend/                        # Patient-facing React app (Port 5173)
│   ├── src/
│   │   ├── assets/                     # Images, icons, SVGs
│   │   ├── components/                 # Navbar, Footer, DoctorCard, etc.
│   │   ├── context/
│   │   │   └── AppContext.jsx          # Global state — doctors, user, token
│   │   └── pages/
│   │       ├── Home/                   # Landing page
│   │       ├── Doctors/                # Browse by speciality
│   │       ├── Appointment/            # Book appointment
│   │       ├── MyAppointments/         # Patient's bookings
│   │       ├── MyProfile/              # Profile management
│   │       ├── About/
│   │       ├── Contact/
│   │       └── Verify/                 # Payment verification
│   ├── vercel.json
│   └── .env
│
├── 📁 admin/                           # Admin + Doctor panel (Port 5174)
│   ├── src/
│   │   ├── context/
│   │   │   ├── AdminContext.jsx        # Admin state & API calls
│   │   │   └── DoctorContext.jsx       # Doctor state & API calls
│   │   └── pages/
│   │       ├── Admin/
│   │       │   ├── Dashboard.jsx
│   │       │   ├── AllAppointments.jsx
│   │       │   ├── AddDoctor.jsx
│   │       │   └── DoctorsList.jsx
│   │       └── Doctor/
│   │           ├── DoctorDashboard.jsx
│   │           ├── DoctorAppointments.jsx
│   │           └── DoctorProfile.jsx
│   ├── vercel.json
│   └── .env
│
├── 📁 backend/                         # Express REST API (Port 4000)
│   ├── config/
│   │   ├── mongodb.js                  # MongoDB Atlas connection
│   │   └── cloudinary.js              # Cloudinary setup
│   ├── controllers/
│   │   ├── adminController.js
│   │   ├── doctorController.js
│   │   └── userController.js
│   ├── middlewares/
│   │   ├── authAdmin.js
│   │   ├── authDoctor.js
│   │   └── authUser.js
│   ├── models/
│   │   ├── userModel.js
│   │   ├── doctorModel.js
│   │   └── appointmentModel.js
│   ├── routes/
│   │   ├── adminRoute.js
│   │   ├── doctorRoute.js
│   │   └── userRoute.js
│   ├── server.js
│   └── .env
│
└── .gitignore
```

---

## 🚀 Local Setup

### Prerequisites

Before you begin, make sure you have:

- ✅ [Node.js](https://nodejs.org/) v18 or higher
- ✅ A [MongoDB Atlas](https://www.mongodb.com/atlas) free cluster
- ✅ A [Stripe](https://stripe.com) account (test mode keys)
- ✅ A [Cloudinary](https://cloudinary.com) free account

---

### Step 1 — Clone the repo

```bash
git clone https://github.com/Sahil-Mansuri-15/Prescripto.git
cd Prescripto
```

---

### Step 2 — Backend

```bash
cd backend
npm install
```

Create `backend/.env`:

```env
MONGODB_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/prescripto
JWT_SECRET=your_super_secret_jwt_key

# Admin Credentials
ADMIN_EMAIL=admin@example.com
ADMIN_PASSWORD=your_admin_password

# Cloudinary
CLOUDINARY_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_SECRET_KEY=your_api_secret

# Stripe
STRIPE_SECRET_KEY=sk_test_your_key

# Currency
CURRENCY=INR
```

```bash
npm run server     # Starts on http://localhost:4000
```

---

### Step 3 — Frontend (Patient Portal)

```bash
cd frontend
npm install
```

Create `frontend/.env`:

```env
VITE_BACKEND_URL=http://localhost:4000
```

```bash
npm run dev        # Starts on http://localhost:5173
```

---

### Step 4 — Admin Panel

```bash
cd admin
npm install
```

Create `admin/.env`:

```env
VITE_BACKEND_URL=http://localhost:4000
```

```bash
npm run dev        # Starts on http://localhost:5174
```

---

## 📡 API Reference

<details>
<summary><b>👤 User Routes</b> — <code>/api/user</code></summary>

| Method | Endpoint | Auth | Description |
|--------|----------|------|-------------|
| `POST` | `/register` | ❌ | Register new patient |
| `POST` | `/login` | ❌ | Login patient |
| `GET` | `/get-profile` | ✅ | Get user profile |
| `POST` | `/update-profile` | ✅ | Update name, photo, dob, etc. |
| `POST` | `/book-appointment` | ✅ | Book a time slot |
| `GET` | `/appointments` | ✅ | Get all appointments |
| `POST` | `/cancel-appointment` | ✅ | Cancel an appointment |
| `POST` | `/payment-stripe` | ✅ | Initiate Stripe payment |
| `POST` | `/verify-stripe` | ✅ | Verify payment status |

</details>

<details>
<summary><b>🩺 Doctor Routes</b> — <code>/api/doctor</code></summary>

| Method | Endpoint | Auth | Description |
|--------|----------|------|-------------|
| `POST` | `/login` | ❌ | Doctor login |
| `GET` | `/list` | ❌ | Get all doctors (public) |
| `POST` | `/appointments` | ✅ | Get doctor's appointments |
| `POST` | `/complete-appointment` | ✅ | Mark as completed |
| `POST` | `/cancel-appointment` | ✅ | Cancel appointment |
| `GET` | `/dashboard` | ✅ | Earnings & stats |
| `GET` | `/profile` | ✅ | Get profile data |
| `POST` | `/update-profile` | ✅ | Update fees, availability |

</details>

<details>
<summary><b>⚙️ Admin Routes</b> — <code>/api/admin</code></summary>

| Method | Endpoint | Auth | Description |
|--------|----------|------|-------------|
| `POST` | `/login` | ❌ | Admin login |
| `POST` | `/add-doctor` | ✅ | Add doctor with image |
| `GET` | `/all-doctors` | ✅ | List all doctors |
| `POST` | `/change-availability` | ✅ | Toggle doctor availability |
| `GET` | `/appointments` | ✅ | All platform appointments |
| `POST` | `/cancel-appointment` | ✅ | Cancel any appointment |
| `GET` | `/dashboard` | ✅ | Platform-wide stats |

</details>

---

## 💳 Test Payments

Use Stripe's test card to simulate payments:

```
Card Number  →  4242 4242 4242 4242
Expiry       →  Any future date  (e.g. 12/27)
CVV          →  Any 3 digits     (e.g. 123)
ZIP          →  Any 5 digits     (e.g. 12345)
```

---

## ☁️ Deployment Guide

| Service | Platform | Config |
|---------|----------|--------|
| **Patient Frontend** | [Vercel](https://vercel.com) | Root: `frontend`, add `VITE_BACKEND_URL` |
| **Admin Panel** | [Vercel](https://vercel.com) | Root: `admin`, add `VITE_BACKEND_URL` |
| **REST API** | [Render](https://render.com) | Root: `backend`, Start: `node server.js` |
| **Database** | [MongoDB Atlas](https://www.mongodb.com/atlas) | Free M0 cluster |
| **Image CDN** | [Cloudinary](https://cloudinary.com) | Free tier (25 GB) |

> 💡 **Tip:** Add your Render backend URL to [UptimeRobot](https://uptimerobot.com) (free) to prevent cold starts on Render's free tier.

---

## 🤝 Contributing

Contributions are always welcome!

```bash
# 1. Fork the project
# 2. Create your feature branch
git checkout -b feature/YourFeature

# 3. Commit your changes
git commit -m "feat: add YourFeature"

# 4. Push and open a Pull Request
git push origin feature/YourFeature
```

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for more information.

---

<div align="center">

<br/>

**Built with passion by Sahil Mansuri**

[![GitHub Follow](https://img.shields.io/github/followers/Sahil-Mansuri-15?label=Follow&style=social)](https://github.com/Sahil-Mansuri-15)

<br/>

*If this project helped you, consider giving it a* ⭐

</div>
