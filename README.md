
## MySQL Appointment System

This project is a database design and implementation for an appointment system. 
The system supports multiple users booking appointments with doctors across various clinics. 
The database schema includes tables for users, doctors, clinics, doctor-clinic relationships, and appointments.

### Database Schema

1. **Users Table**:
    - `user_id` (Primary Key)
    - `name`
    - `email`
    - `birthdate`

2. **Clinics Table**:
    - `clinic_id` (Primary Key)
    - `clinic_name`
    - `address`

3. **Doctors Table**:
    - `doctor_id` (Primary Key)
    - `name`
    - `specialization`

4. **Doctor_Clinics Table**:
    - `doctor_id` (Foreign Key)
    - `clinic_id` (Foreign Key)

5. **Appointments Table**:
    - `appointment_id` (Primary Key)
    - `user_id` (Foreign Key)
    - `doctor_id` (Foreign Key)
    - `clinic_id` (Foreign Key)
    - `appointment_date` (DateTime)
    - `booking_date` (DateTime)
    - `status` (Enum: 'scheduled', 'cancelled')



### Queries

The following queries are provided and explained in the project:

1. All appointments booked in the last 7 days for a doctor.
2. All appointments booked in the last 2 days and scheduled within the next 5 hours for a doctor.
3. Users who have at least 1 appointment and have their birthday coming in the next 5 days.
4. Appointments for a particular patient in the last 7 days.
5. Appointment cancellation percentage for a doctor by clinic.

### ER Diagram

An ER diagram is provided to visualize the database schema and relationships between the tables. 
