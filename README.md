
# Patient Tracker System

A comprehensive healthcare management solution for appointment booking and medical records management.

## Overview

The Patient Tracker System is a streamlined application designed to manage healthcare appointments and patient medical records efficiently. It offers functionalities for patient appointment booking and medical record management, providing secure and user-friendly access for both patients and healthcare staff.

## Features

### Patient Appointment Booking

- **User Authentication**: Secure login for patients.
- **Appointment Slots Display**: Shows available times for booking.
- **Appointment Booking**: Patients can book appointments with automatic confirmation.
- **Notification System**: Sends confirmations for booked appointments.

### Medical Record Management

- **Secure Access**: Only authorized healthcare staff can access medical records.
- **View Patient History**: Staff can view a patient's comprehensive medical history.
- **Update Records**: Ability to update medical information with new diagnoses and treatments.
- **Chronological Tracking**: Maintains a chronological order of the medical history updates.

## Technical Details

### Data Models

- **Patient**: Stores patient information (ID, username, password, name, email, phone).
- **HealthcareStaff**: Manages information about healthcare staff (ID, username, password, name, role).
- **Appointment**: Details about appointments (ID, patient ID, date, duration, status, notes).
- **MedicalRecord**: Contains records of medical history (ID, patient ID, updated by, update date, diagnosis, treatment plan, medications, notes).

### System Components

- **DatabaseManager**: Manages database operations and data persistence.
- **AppointmentSystem**: Coordinates the appointment booking workflow.
- **MedicalRecordsSystem**: Manages operations related to medical records.
- **NotificationSystem**: Handles sending notifications for appointments.
- **PatientTrackerApp**: Main application that integrates all components.

## Database Schema

The system uses SQLite with tables for:
- `patients`
- `healthcare_staff`
- `appointments`
- `medical_records`

## Installation

Ensure you have Python 3.6+ installed:
1. Clone the repository.
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

Run the main script to start the application:
```bash
python patient_tracker.py
```
The system will present you with a menu to choose between:
- Patient Appointment Booking
- Update Medical Records
- Exit

## Demo Accounts

For demonstration purposes, the system comes pre-loaded with sample accounts:

### Patients:
- Username: patient1, Password: pass1 (John Doe)
- Username: patient2, Password: pass2 (Jane Smith)

### Healthcare Staff:
- Username: doctor1, Password: pass1 (Dr. Robert Johnson)
- Username: nurse1, Password: pass2 (Nurse Sarah Williams)

## Development

To extend the system with new features:
- Update the appropriate data models.
- Extend the database schema in DatabaseManager.
- Implement the business logic in respective system components.
- Update the main PatientTrackerApp to include the new functionality.

## Security Considerations

- The current implementation uses plain text passwords for simplicity.
- In a production environment, passwords should be hashed.
- API endpoints should implement proper authentication and authorization.
- Input validation should be added to prevent SQL injection.

## Future Enhancements

- Web interface for easier access.
- Mobile application for patients.
- Integration with other healthcare systems.
- Advanced notification systems (email, SMS).
- Data export/import capabilities.
- Analytics dashboard for healthcare administrators.
