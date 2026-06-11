# Flask Website Visitor Tracking using Firebase Realtime Database

## 📌 Overview

This project is a simple Flask web application that tracks page visits and stores visitor data in Firebase Realtime Database.

Whenever a user visits a page (`Home`, `About`, or `Contact`), the application records the page name in Firebase. This demonstrates the integration of Flask with Firebase Admin SDK for backend data storage and analytics.

---

## 🚀 Features

* Flask-based web application
* Firebase Realtime Database integration
* Tracks visits to multiple pages
* Stores page visit records in real-time
* Simple and beginner-friendly implementation
* Demonstrates backend logging and analytics

---

## 🛠️ Technologies Used

* Python
* Flask
* Firebase Admin SDK
* Firebase Realtime Database
* HTML Templates

---

## 📂 Project Structure

```text
project/
│
├── app.py
├── templates/
│   ├── index.html
│   ├── about.html
│   └── contact.html
│
├── firebase-adminsdk.json
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/flask-firebase-visitor-tracker.git
cd flask-firebase-visitor-tracker
```

### 2. Create Virtual Environment (Optional)

```bash
python -m venv venv
```

Activate:

**Windows**

```bash
venv\Scripts\activate
```

**Linux / macOS**

```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install flask firebase-admin
```

---

## 🔥 Firebase Setup

### Step 1: Create Firebase Project

1. Open Firebase Console.
2. Create a new project.
3. Enable Realtime Database.

### Step 2: Generate Service Account Key

1. Go to Project Settings.
2. Open Service Accounts tab.
3. Click **Generate New Private Key**.
4. Download the JSON file.

### Step 3: Update Credentials Path

Replace:

```python
credentials.Certificate("path/to/serviceAccountKey.json")
```

with the path to your downloaded Firebase credentials file.

### Step 4: Update Database URL

Replace:

```python
databaseURL = "https://your-project-id-default-rtdb.firebaseio.com/"
```

with your Firebase Realtime Database URL.

---

## ▶️ Running the Application

Start the Flask server:

```bash
python app.py
```

Output:

```text
* Running on http://127.0.0.1:5000
```

Open your browser:

```text
http://127.0.0.1:5000
```

---

## 📊 How Visitor Tracking Works

When a user visits:

### Home Page

```python
ref.push({'page':'home'})
```

Firebase stores:

```json
{
  "page": "home"
}
```

### About Page

```python
ref.push({'page':'about'})
```

Firebase stores:

```json
{
  "page": "about"
}
```

### Contact Page

```python
ref.push({'page':'contact'})
```

Firebase stores:

```json
{
  "page": "contact"
}
```

---

## 📈 Example Database Structure

```json
{
  "visits": {
    "-Nabc123": {
      "page": "home"
    },
    "-Nabc124": {
      "page": "about"
    },
    "-Nabc125": {
      "page": "contact"
    }
  }
}
```

---

## 🎯 Learning Outcomes

This project helps understand:

* Flask Routing
* Template Rendering
* Firebase Realtime Database
* Firebase Admin SDK
* Backend Data Logging
* Web Analytics Basics

---

## 🔮 Future Improvements

* Count total page visits
* Store visitor timestamps
* Track unique visitors
* Add dashboard for analytics
* Store IP addresses (with privacy considerations)
* Display visit statistics on admin page
* Deploy application on cloud platforms

---

## 👨‍💻 Author

**Pranay Jadhao**

Electronics & Telecommunication Engineer

Aspiring Software & Embedded Systems Engineer

GitHub: https://github.com/

LinkedIn: [www.linkedin.com/in/pranayjadhao](http://www.linkedin.com/in/pranayjadhao)

---

## 📄 License

This project is open-source and available for educational and learning purposes.


![Screenshot 2025-04-28 112037](https://github.com/user-attachments/assets/ddd653f2-b60a-404f-9760-6f7541dfe8d0)
