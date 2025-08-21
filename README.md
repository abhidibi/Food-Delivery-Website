# 🍔 Full-Stack Food Delivery Application

A complete **full-stack food delivery service application** featuring a **Node.js + Express backend API** and a **React (Vite) admin dashboard frontend**.  
It supports user authentication, menu management, order processing with **Stripe payments**, and an admin panel to track/manage orders.

---

## 🚀 Key Features

- 🔐 **User Authentication** – Secure login & registration with JWT, bcrypt, and input validation.  
- 📝 **Menu Management** – Admins can add, list, and remove food items with image uploads.  
- 💳 **Order Processing** – Customers can place orders, pay via Stripe or Cash on Delivery, and track status.  
- 📊 **Admin Dashboard** – Dedicated React dashboard for administrators to manage menu & monitor orders in real time.  
- 📦 **File Upload Support** – Food images uploaded via Multer.  
- ⚡ **Modern UI** – Built with Vite + React Router + Toastify notifications.  

---

## 🛠️ Tech Stack

### **Backend**
- **Server**: Node.js, Express.js  
- **Database**: MongoDB (Mongoose)  
- **Authentication**: JWT, bcrypt, validator  
- **File Uploads**: Multer  
- **Payment Gateway**: Stripe  
- **Env Management**: dotenv  

### **Frontend**
- **Framework**: React (Vite)  
- **Routing**: React Router DOM  
- **API Calls**: Axios  
- **Notifications**: React Toastify  
- **Payment Integration**: Stripe.js  

---

## 📂 Project Structure

```

food-del/
│── backend/       # Node.js backend API
│── frontend/      # React admin dashboard
│── admin/         # (Optional extra panel if used)
│── How To Run Project.pdf

````

---

## ⚙️ Setup Instructions

### 🔹 Backend Setup
1. Navigate to backend folder:
   ```bash
   cd backend
````

2. Install dependencies:

   ```bash
   npm install
   ```
3. Create a `.env` file:

   ```env
   MONGO_URI=<Your MongoDB Connection String>
   JWT_SECRET=<A_Random_Secret_String>
   STRIPE_SECRET_KEY=<Your_Stripe_Secret_Key>
   ```
4. Start server:

   ```bash
   npm start
   ```

   Runs on: **[http://localhost:4000](http://localhost:4000)**

---

### 🔹 Frontend Setup

1. Navigate to frontend folder:

   ```bash
   cd frontend
   ```
2. Install dependencies:

   ```bash
   npm install
   ```
3. Start dev server:

   ```bash
   npm run dev
   ```

   Runs on: **[http://localhost:5173](http://localhost:5173)**

---

## 📡 API Endpoints

Base URL: `http://localhost:4000/api/`

| Endpoint            | Method | Description                       | Auth |
| ------------------- | ------ | --------------------------------- | ---- |
| `/user/register`    | POST   | Register new user                 | ❌    |
| `/user/login`       | POST   | User login                        | ❌    |
| `/food/add`         | POST   | Add new food item + image         | ❌    |
| `/food/list`        | GET    | Get all food items                | ❌    |
| `/food/remove`      | POST   | Remove food item                  | ❌    |
| `/cart/add`         | POST   | Add item to user cart             | ✅    |
| `/cart/remove`      | POST   | Remove item from cart             | ✅    |
| `/cart/get`         | POST   | Get user’s cart                   | ✅    |
| `/order/place`      | POST   | Place order via Stripe            | ✅    |
| `/order/placecod`   | POST   | Place order with Cash on Delivery | ✅    |
| `/order/userorders` | POST   | Get user’s order history          | ✅    |
| `/order/list`       | GET    | Get all orders (admin only)       | ❌    |
| `/order/status`     | POST   | Update order status               | ❌    |

---

## 📊 Admin Dashboard Features

* **Navbar + Sidebar** navigation
* **Add Items**: Form with image preview & upload
* **List Items**: Display menu with delete option
* **Orders Page**: View all customer orders, update status (Processing → Out for Delivery → Completed)

---

## 📝 Notes

* Never push `.env` to GitHub — add it to `.gitignore`.
* You can create a `.env.example` with placeholder values for collaborators.

---

## 👨‍💻 Author

Developed by **Abhishek Yadav** 🚀

```



