# 🏥 Hospital Bed Booking System

This is a **Flask-based Hospital Bed Booking System** developed to help hospitals and patients manage the availability of hospital beds during emergencies like the COVID-19 pandemic.

## 📌 Features

- 🔐 **User & Hospital Login**
- 📝 **User Signup**
- 🏥 **Admin Dashboard for Hospital Registration**
- 📋 **Hospital Bed Availability Entry & Management**
- ✅ **Patient Slot Booking**
- 👤 **Patient Booking Details View**
- 📊 **Bed Update and Trigger Logs**

## 🛠️ Tech Stack

- Python 3
- Flask
- Flask-Login
- SQLAlchemy
- MySQL
- HTML/CSS (Jinja Templates)
- Bootstrap

## 🚀 Getting Started

### Prerequisites

- Python 3.x installed
- MySQL Server
- Git

### Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/VIKASCDR183/hospital-bed-booking.git
   cd hospital-bed-booking
   ```

2. **Set Up Virtual Environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Create Database**
   - Open MySQL and create a database named `covid`:
     ```sql
     CREATE DATABASE covid;
     ```

5. **Configure Database**
   - In the Python file, ensure this line is configured correctly:
     ```python
     app.config['SQLALCHEMY_DATABASE_URI'] = 'mysql://root:@localhost/covid'
     ```
   - If needed, replace `root` and password accordingly.

6. **Run the App**
   ```bash
   python app.py
   ```
   - Open [http://127.0.0.1:5000](http://127.0.0.1:5000) in your browser.

## 👨‍⚕️ User Roles

### 1. Admin
- Login: `admin` / `admin`
- Can register hospitals with a unique hospital code and password.

### 2. Hospital User
- Can log in using provided credentials.
- Add or update bed availability.

### 3. Patient/User
- Sign up using SRF ID, Email, and DOB.
- Book bed slots by providing SPO2 and personal details.

## 🧪 Test Database Connection
- Visit: `/test` route to verify if the database is properly connected.

## 📂 File Structure

- `templates/`: Contains all HTML templates (Jinja2)
- `static/`: (Optional) For CSS/JS
- `app.py`: Main application file
- `config.json`: (Optional) For sensitive configs
- `README.md`: Project overview and setup instructions

## 📌 Important Notes

- The app does not currently use password hashing in the hospital login section for simplicity.
- You can uncomment email sending functionality if needed (`Flask-Mail`).
- Admin panel is simple, protected via session.


## 🙋 Author

**VIKASCDR183**  
GitHub: [github.com/VIKASCDR183](https://github.com/VIKASCDR183)

---
