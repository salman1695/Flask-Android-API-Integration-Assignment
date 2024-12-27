
# Flask-Android API Integration Assignment

## Project Overview
This project demonstrates the integration of a Flask-based backend with an Android application using Kotlin. The backend provides APIs for user authentication and data management, which are consumed by the Android app to perform operations like user registration, login, password recovery, and data retrieval.

---

## Features
### Backend (Flask)
- **User Registration API**: Allows new users to register.
- **Login API**: Authenticates existing users.
- **Forgot Password API**: Handles user password recovery.
- **User Data Retrieval API**: Fetches all user details.

### Frontend (Android)
- **Kotlin-Based App**:
  - **Sign-Up Screen**: Allows users to create a new account.
  - **Login Screen**: Facilitates user authentication.
  - **Forgot Password Screen**: Sends recovery options to users.
  - **User List Screen**: Displays all users in a RecyclerView.
- **API Integration**:
  - Data is retrieved from Flask APIs using Retrofit.
  - Error handling for failed requests.
- **Network Security Configuration**:
  - Supports HTTP communication using `network_security_config`.

---

## Prerequisites
### Backend Requirements
- Python 3.8 or above
- Flask
- SQLite3

### Android Requirements
- Android Studio (Latest version)
- Minimum SDK: 21
- Retrofit and Gson libraries added to `build.gradle`.

---

## Setup Guide
### Backend (Flask)
1. Clone the repository:
   ```bash
   git clone https://github.com/salman1695/Flask-Android-API-Integration-Assignment
   ```
2. Install dependencies:
   ```bash
   pip install flask
   ```
3. Run the Flask server:
   ```bash
   python app.py
   ```
4. Flask server will run at `http://192.168.0.112:5000`.

### Android (Kotlin)
1. Open the project in Android Studio.
2. Update the `BASE_URL` in the API client:
   ```kotlin
   const val BASE_URL = "http://192.168.0.112:5000"
   ```
3. Build and run the application on a device or emulator.

---

## APIs
| Endpoint           | Method | Description                       |
|--------------------|--------|-----------------------------------|
| `/signup`          | POST   | Register a new user              |
| `/login`           | POST   | Authenticate an existing user    |
| `/forgot`          | POST   | Recover user password            |
| `/all_users`       | GET    | Retrieve all user data           |

---

## Folder Structure
```
📦 Project
├── 📂 Backend
│   ├── app.py             # Flask server code
│   ├── users.db           # SQLite database
│   └── requirements.txt   # Flask dependencies
├── 📂 AndroidApp
│   ├── 📂 app
│   │   ├── 📂 src
│   │   │   ├── 📂 main
│   │   │   │   ├── 📂 java
│   │   │   │   ├── 📂 res
│   │   │   │   ├── 📜 AndroidManifest.xml
│   │   │   │   └── 📂 network_security_config
│   │   ├── 📂 build.gradle
```

---

## Usage
1. **Run Flask Server**:
   - Ensure the server is running on the same network as your mobile device.
2. **Run Android App**:
   - Test the APIs using the app.
3. **Use Postman**:
   - Test API endpoints using `http://192.168.0.112:5000`.

---

## Challenges Faced
1. **Cleartext Communication Issue**:
   - Solved by adding a `network_security_config` file.
2. **Cross-Origin Requests**:
   - Ensured same network connectivity for backend and app.
3. **Retrofit Integration**:
   - Handled network timeouts and error responses effectively.

---

## Author
**M.Salman**

Feel free to contribute or raise issues if you find any bugs!
