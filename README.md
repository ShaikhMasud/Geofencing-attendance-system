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
### Screenshots 

Admin UI:
![image](https://github.com/user-attachments/assets/85b3e048-d610-4c8d-883a-cb94b8476aa2)
![image](https://github.com/user-attachments/assets/ef01c45a-cb0f-47da-8bbd-39085fd3721e)
![image](https://github.com/user-attachments/assets/49a69bf5-aa82-43df-bf33-92752df7e08a)
![image](https://github.com/user-attachments/assets/96826b31-32c0-4bf3-a6ce-678abc6eef45)
![image](https://github.com/user-attachments/assets/73c12d9e-f17f-4a5a-aaf1-23723b1f05c1)
![image](https://github.com/user-attachments/assets/1661ff85-3624-4bc4-8f14-a7c8e83248d8)
![image](https://github.com/user-attachments/assets/dd35a7b9-0358-4f5e-a939-17bdd73f42b2)

Student UI:
![image](https://github.com/user-attachments/assets/6e1c3ce7-bb1d-4924-899c-455443620d71)
![image](https://github.com/user-attachments/assets/46399832-366d-449e-8d96-7b685b5e9c58
![image](https://github.com/user-attachments/assets/f5a83530-21cb-483d-b7f0-eba8cb43680f)

Staff/Teacher UI:
![image](https://github.com/user-attachments/assets/149f8a10-2008-4986-b264-0a6c02a78f69)
Manual attendance
![image](https://github.com/user-attachments/assets/12eb0a99-b4e2-4f86-a19d-a7f2ed0a6b4e)







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
5 **Create a SuperUser**

```bash
python manage.py createsuperuser
```

6. **Start the Server**

```bash
python manage.py runserver
```

7. **Access the App**

```
http://localhost:8000/
```

---
