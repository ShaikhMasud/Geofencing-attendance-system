# 📍 GeoAttendance - Geofenced Attendance Management System

An intelligent attendance tracking system that ensures students mark their presence only within a specified geofenced area. Built with **Django**, integrated with **Mapbox API** for location validation, and enhanced by **OpenCV** and **QuaggaJS** for secure and efficient **barcode scanning**, this system promotes transparency, accuracy, and automation in educational attendance workflows.

---

## 🚀 Key Features

* 🗺️ **Geofencing with Mapbox API**: Ensures attendance can only be marked within a predefined location radius.
* 🔍 **Barcode Scanning**: Uses OpenCV and JavaScript's Quagga library for fast and secure barcode recognition.
* 🧑‍💼 **User Role Management**: Multiple user roles including Admin, Faculty, and Student with respective access levels.
* 📊 **Analytics Dashboard**: Visual insights into attendance trends and downloadable reports for administrators.
* 🔐 **Secure & Accurate**: Combines location-based validation with real-time barcode verification to prevent proxy attendance.

---

## 🧑‍🏫 User Roles

### 🎓 Student

* Can log in and mark attendance using their **barcode** and **current geolocation**.
* Can view their **attendance records** for each subject in real-time.
* Limited to viewing and interacting with their own data.

### 👩‍🏫 Teacher

* Can manage attendance for their respective subjects.
* Able to **manually mark attendance** if needed (e.g., for students with technical issues).
* Can view complete **attendance records** of their class and each student.
* Facilitates validation and oversight at the classroom level.

### 🛠️ Admin

* Has full access to the system and **manages user accounts**.
* Can **add or remove** students and teachers from the database.
* Can view and export **institution-wide attendance statistics**.
* Serves as the central authority for configuring the system and user permissions.

---

## 🛠️ Tech Stack

* **Backend**: Django (Python)
* **Frontend**: HTML, CSS, JavaScript
* **Location Services**: Mapbox API
* **Barcode Scanning**: OpenCV (Python) + QuaggaJS (JavaScript)
* **Database**: MySQL

---

## 💡 How It Works

1. 🎓 **Student Login**: Students log in to the portal and open the attendance page.
2. 📍 **Location Verification**: The app verifies if the student is within the geofence using Mapbox.
3. 🧾 **Barcode Scan**: Students scan their unique ID card using webcam (QuaggaJS + OpenCV).
4. ✅ **Mark Attendance**: If both geolocation and barcode scan are valid, attendance is recorded.

---

## 📦 Setup Instructions

1. **Clone the Repository**

```bash
git clone https://github.com/your-username/geoattendance.git
cd geoattendance
```

2. **Install Dependencies**

```bash
pip install -r requirements.txt
```

3. **Configure Database**

Update `settings.py` with your MySQL database credentials:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'geoattendance_db',
        'USER': 'your_mysql_user',
        'PASSWORD': 'your_mysql_password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```

4. **Run Migrations**

```bash
python manage.py makemigrations
python manage.py migrate
```

5. **Start the Server**

```bash
python manage.py runserver
```

6. **Access the App**

```
http://localhost:8000/
```

---
