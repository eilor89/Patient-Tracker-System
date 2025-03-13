Patient Tracker System
A comprehensive healthcare management solution for appointment booking and medical records management.
Overview
The Patient Tracker System is a streamlined application designed to manage healthcare appointments and patient medical records efficiently. The system provides two main functionalities:

Patient Appointment Booking: Allows patients to log in, select a date, view available time slots, and book appointments.
Medical Record Management: Enables healthcare staff to access and update patient medical records with diagnoses, treatment plans, medications, and notes.

System Features
Patient Appointment Booking

User authentication for patients
Display of available appointment slots
Appointment booking with automatic confirmation
Notification system for appointment confirmations

Medical Record Management

Secure access for healthcare staff
Ability to view patient medical history
Update patient records with new medical information
Chronological tracking of patient's medical history

Technical Details
Data Models

Patient: Stores patient information (ID, username, password, name, email, phone)
HealthcareStaff: Manages staff information (ID, username, password, name, role)
Appointment: Tracks appointment details (ID, patient ID, date, duration, status, notes)
MedicalRecord: Contains medical information (ID, patient ID, updated by, update date, diagnosis, treatment plan, medications, notes)

System Components

DatabaseManager: Handles database operations and data persistence
AppointmentSystem: Manages the appointment booking workflow
MedicalRecordsSystem: Handles medical record operations
NotificationSystem: Sends notifications for appointment confirmations
PatientTrackerApp: Main application that coordinates all systems

Database Schema
The system uses SQLite with the following tables:

patients
healthcare_staff
appointments
medical_records

Installation

Ensure you have Python 3.6+ installed
Clone the repository
Install the required dependencies:
Copypip install -r requirements.txt


Usage
Run the main script to start the application:
Copypython patient_tracker.py
The system will present you with a menu to choose between:

Patient Appointment Booking
Update Medical Records
Exit

Demo Accounts
For demonstration purposes, the system comes pre-loaded with sample accounts:
Patients:

Username: patient1, Password: pass1 (John Doe)
Username: patient2, Password: pass2 (Jane Smith)

Healthcare Staff:

Username: doctor1, Password: pass1 (Dr. Robert Johnson)
Username: nurse1, Password: pass2 (Nurse Sarah Williams)

Development
Adding New Features
To extend the system with new features:

Update the appropriate data models
Extend the database schema in DatabaseManager
Implement the business logic in respective system components
Update the main PatientTrackerApp to include the new functionality

Security Considerations

The current implementation uses plain text passwords for simplicity
In a production environment, passwords should be hashed
API endpoints should implement proper authentication and authorization
Input validation should be added to prevent SQL injection

Future Enhancements

Web interface for easier access
Mobile application for patients
Integration with other healthcare systems
Advanced notification systems (email, SMS)
Data export/import capabilities
Analytics dashboard for healthcare administrators
