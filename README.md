# Road Accident Reporting API & Mobile App

A geo-location powered emergency reporting system that allows users to quickly report road accidents. The platform alerts nearby emergency responders in real-time to reduce response delays and save lives.

---

## 📌 Features

* 🚨 **One‑tap accident reporting**
* 📍 **Automatic geo‑location tagging using GPS**
* 📸 **Upload images and videos** of the accident scene
* 🗣️ Optional **voice note descriptions**
* 📡 **Real-time alerts** to ambulance, police, and fire stations
* 🗺️ **Interactive map** showing accident locations and nearby emergency units
* 🔐 **Anonymous reporting** supported
* 🧭 **View nearest hospitals and police stations**
* 📊 **Admin dashboard** with analytics and incident logs

---

## 🔧 Requirements

Make sure you have the following installed:

### **Backend**

* Rust / Node.js / Django (based on chosen tech stack)
* PostgreSQL or MySQL
* Google Maps API Key / OpenStreetMap
* Firebase Cloud Messaging (FCM) for push notifications

### **Mobile App**

* Flutter or React Native
* Android Studio / Xcode

### **Recommended Tools**

* VS Code + REST Client / Thunder Client
* Postman for API testing
* Git & GitHub

---

## 🚀 Setup Instructions

### 1️⃣ Clone the repository

```bash
git clone <your-repo-url>
cd accident_reporting_app
```

### 2️⃣ Setup environment variables

Create a `.env` file:

```
DB_URL=postgres://user:password@localhost/accidents\NMAPS_API_KEY=your_google_maps_key
FCM_KEY=your_firebase_key
```

### 3️⃣ Install dependencies & run backend

Example (Node.js backend):

```bash
npm install
npm run dev
```

Server runs at:
👉 **[http://127.0.0.1:8000](http://127.0.0.1:8000)**

### 4️⃣ Run the Mobile App

```bash
flutter pub get
flutter run
```

---

## 🌐 API Endpoints

### ➕ POST `/accidents`

Submit a new accident report.

#### Request Body

```json
{
  "reporterId": 12,
  "location": { "lat": -1.2841, "lng": 36.8156 },
  "severity": "high",
  "description": "Two vehicles collision",
  "mediaUrls": ["image1.jpg", "video1.mp4"]
}
```

#### Response

**201 Created**

---

### 📄 GET `/accidents`

Retrieve all reported accidents.

#### Example Response

```json
[
  {
    "id": 1,
    "location": { "lat": -1.2841, "lng": 36.8156 },
    "severity": "high",
    "status": "dispatched"
  }
]
```

---

## ❗ Common Issues & Solutions

| Error                          | Solution                                                            |
| ------------------------------ | ------------------------------------------------------------------- |
| **GPS not working**            | Confirm that the device has location permissions enabled.           |
| **Push notifications failing** | Ensure correct Firebase keys and device tokens.                     |
| **API returning 500 errors**   | Check database connection and required environment variables.       |
| **Map not showing**            | Verify Google Maps API key restrictions.                            |
| **Uploads failing**            | Confirm media storage bucket (Firebase/AWS) is configured properly. |

---

## 📚 References

* Google Maps API Docs
* Firebase Cloud Messaging Docs
* Flutter / React Native Docs
* Node.js / Rust / Django (depending on backend choice)

---

## 👤 Author

**Your Name Here**

*(Tell me if you want this converted into a PDF, expanded, or formatted like a full GitHub README.)*
