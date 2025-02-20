#Face Recognition Attendance & Visitor Management System
This project is a real-time face recognition system designed to manage employee attendance and visitor logging using OpenCV, dlib, and face_recognition libraries.

**🚀 Key Features:**
Employee Attendance: Automatically recognizes employees and logs their entry time with visit count.
Visitor Logging: Detects visitors and tracks their visits over time.
Liveness Detection: Prevents spoofing using:
Blink Detection
Head Movement Tracking
Texture Analysis (Blur Check)
Duplicate Entry Prevention:
Employees and visitors are logged only once within a set time (e.g., 30 minutes).
Visit count increases if they return after the time limit.
CSV Logs: Attendance and visitor logs are stored in CSV files.
🛠️ How to Set Up:
Install the required libraries:

bash
Copy
Edit
pip install opencv-python dlib face_recognition pandas
Place employee images in the employee/ folder.

Name the images as EmployeeName.jpg (e.g., JohnDoe.jpg).
Download Dlib Face Landmark Model:

shape_predictor_68_face_landmarks.dat – Download Here
Extract and place it in the project folder.
▶️ How to Run:
bash
Copy
Edit
python main.py
Press q to quit the application.
📂 Folder Structure:
bash
Copy
Edit
face_recognition_system/
│
├── main.py
├── face_utils.py
├── attendance_logger.py
├── config.py
├── employee/            # Employee images
├── visitor_photos/      # Visitor images (Optional)
├── shape_predictor_68_face_landmarks.dat
├── attendance_log.csv   # Auto-generated
├── visitor_log.csv      # Auto-generated
📝 CSV Logs:
Employee Log (attendance_log.csv): Name | Timestamp | Type | VisitCount
Visitor Log (visitor_log.csv): VisitorName | Timestamps | VisitCount
⚠️ Common Issues:
If you see EmptyDataError, delete the CSV files and re-run the program. They will be auto-created.

👨‍💻 Developed By:
Tech Titans
