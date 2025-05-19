
# ICAT-2: SmartAttend

SmartAttend is an intelligent attendance management system that leverages face detection and recognition to automate classroom attendance. Built with Python, MongoDB, OpenCV, and a custom GUI, it streamlines the process for teachers and students.

---

## Features

- **Automated Attendance:** Uses a deep learning face detection model (Caffe) and a Random Forest classifier for student recognition.
- **User Authentication:** Secure login and signup for teachers.
- **Class & …Management:** Add, view, and manage classes and students.
- **Sample Collection & Augmentation:** Collects face samples and augments them for robust training.
- **Model Training:** Trains a classifier for each class using collected samples.
- **Attendance Marking:** Detects and recognizes students from images to mark attendance.
- **Reporting:** Generates CSV attendance reports per class.
- **Modern GUI:** Built with CustomTkinter for a sleek, user-friendly interface.

---

## Project Structure

SmartAttend/ │ ├── requirements.txt ├── detection_model/ │ ├── architecture.prototxt │ └── weights.caffemodel └── src/ ├── initialize_db_for_testing.py ├── initialize_folder_structure_for_testing.py ├── main.py └── model_testing.py

---

## Getting Started

### 1. Install Dependencies

Install Python 3.8+ and run:

```sh
pip install -r [requirements.txt](http://_vscodecontentref_/6)
```

2. MongoDB Setup
```sh
Ensure MongoDB is running locally on port 27017.
```

3. Initialize Database and Folders (for testing)
To reset and populate the database with test data:
```sh
python [initialize_folder_structure_for_testing.py](http://_vscodecontentref_/8)
```

To reset the folder structure for classes:
```sh
python [initialize_folder_structure_for_testing.py](http://_vscodecontentref_/8)
```

4. Run the Application
To start the application, run:
```sh
python [main.py](http://_vscodecontentref_/9)
```

---

## Usage
- **Login/Signup:** Start the app and log in or sign up as a teacher.
- **Manage Classes:** Add new classes and view existing ones.
- **Add Students:** Add students to classes and collect face samples.
- **Train Model:** After collecting samples, train the classifier for the class.
- **Mark Attendance:** Use the GUI to upload an image and mark attendance automatically.
- **Generate Reports:** Export attendance records as CSV files.

---

## Model Details
- **Face Detection:** Uses a Caffe model defined in detection_model/architecture.prototxt and detection_model/weights.caffemodel.
- **Face Recognition:** Trains a Random Forest classifier on augmented face samples per class.
- **Sample Augmentation:** Uses Albumentations for robust data augmentation.

---

## Key Scripts
- **initialize_db_for_testing.py:** Resets and seeds the MongoDB database with test teachers, classes, and students.
- **initialize_folder_structure_for_testing.py:** Cleans up the class folders for a fresh start.
- **main.py:** Main application with GUI, database, and all core logic.
- **model_testing.py:** Standalone script for testing face detection and recognition models.

---

##Requirements
- **Python 3.8+**
- **MongoDB (local)**
- **Webcam (for sample collection and testing)**
- **See requirements.txt for Python dependencies.**

---

## Acknowledgements
- **OpenCV**
- **Albumentations**
- **CustomTkinter**
- **MongoDB**

---

## License
This project is for educational purposes.

---

## Contact
For questions or contributions, please open an issue or pull request.
