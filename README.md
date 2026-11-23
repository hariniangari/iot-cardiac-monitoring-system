# An Efficient IoT-Based Platform for Remote Real-Time Cardiac Activity Monitoring

A web-based healthcare and IoT monitoring platform built with Java, JSP, and MySQL that enables remote real-time tracking of patient ECG and cardiac activity across Patients, Doctors, ECG Devices, and Cloud administrators.

## Key Features

- **Patient Portal (`Patient.jsp`, `UserReg.jsp`):** Allows patients to register, log in, view their cardiac monitoring status, and access doctor recommendations.
- **Doctor Portal (`Doctor.jsp`, `DoctorUserReg.jsp`):** Enables doctors to register, monitor assigned patients' real-time ECG data, evaluate cardiac conditions (`ECGCardiacCondition.jsp`), and provide timely medical feedback.
- **ECG Device Module (`ECGDevice.jsp`, `ECGHome.jsp`):** Simulates and transmits real-time cardiac signals and patient health parameters to the cloud server.
- **Cloud Management (`Cloud.jsp`):** Centralizes incoming cardiac data streams, manages user/doctor approvals, and maintains secure records.

## Tech Stack

- **Backend:** Java (Servlets & JDBC)
- **Frontend:** JSP, HTML5, CSS3, JavaScript
- **Database:** MySQL (`com.database.Dbconnection`)
- **Server:** Apache Tomcat

## Project Structure

```text
├── java/com/
│   ├── database/
│   │   ├── Dbconnection.java     # Database connection configuration
│   │   └── Queries.java          # SQL query helpers
│   └── upload/
│       ├── DoctorRegAction.java  # Doctor registration & file handling
│       └── UserRegAction.java    # Patient registration & file handling
├── WEB-INF/                      # Deployment descriptors & libraries
├── META-INF/                     # Application manifest & context
├── images/                       # UI graphics and assets
├── layout/                       # CSS stylesheets and layout templates
└── *.jsp                         # Frontend views for Patient, Doctor, ECG & Cloud modules
```

## How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com
   ```
2. **Import into an IDE:** Open the project in **NetBeans** or **Eclipse** as a Java Web Application.
3. **Configure the Database:**
   - Create a MySQL database and import the project's SQL schema.
   - Update your database credentials (URL, username, password) inside `java/com/database/Dbconnection.java`.
4. **Deploy & Run:**
   - Start **Apache Tomcat** and run the project.
   - Open `http://localhost:8080/<project-name>/index.htm` in your browser.
