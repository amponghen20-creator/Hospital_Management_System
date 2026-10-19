# Hospital_Management_System

A role-based hospital records and scheduling system. The core is a C++ console program; a C# (Blazor) web front end sits on top of the same data files.

## About

This project manages the day-to-day records of a small hospital: patient information, doctors on staff, and appointments between the two. Three kinds of staff log in, and each one only sees the actions that belong to their job:

### Role	What they do
Administrator	Update and view patients, register and update doctors, view appointments
Doctor	Update and view patients, record a diagnosis and prescription, view appointments
Receptionist	Admit patients, book appointments, look up patient details

The system has two interfaces that share the same records:

### C++ console app (the core system): four classes (patient, doctor, appointments, user) handle their own data, display, and saving/loading.
##C# Blazor web app (an extension): the same roles and workflows in a browser.

Records are stored in plain, readable text files (patients.txt, doctors.txt, appointments.txt) in a Label : value format, so no database is needed.

## Current Features
Login with three roles (Administrator, Doctor, Receptionist)
Admit a patient with personal, medical, and visit information
Update patient records and look up a patient by ID
Register doctors, update doctor details, and view the doctor list
Book appointments between a patient and a doctor
Record a diagnosis and prescription, which moves an appointment from Booked to Completed
Data saved to text files after every change and reloaded at startup
Web version: role dashboards, searchable patient list, expandable record details, status badges for appointments, and a layout that adapts to small screens
## Getting Started
C++ console app
Open the project in Code::Blocks (H3.cbp) or compile the .cpp files with any C++ compiler.
Run the program and log in with one of the demo accounts below.
Web front end (Blazor)
Install the .NET SDK.
In the HospitalManagementSystem folder, run:
   dotnet restore
   dotnet run
Open the localhost address shown in the terminal.
## Demo accounts

| Role | Username | Password |
| :--- | :--- | :--- |
| Administrator | admin | admin14 |
| Doctor | doctor | doc415 |
| Receptionist | reception | recep185 |

These are hardcoded demo credentials for coursework, not for real use.

## Roadmap / Future Features
### Database integration: 
replace the text files with a database such as SQLite or PostgreSQL
### No record limit: 
the C++ version caps each list at 100 records; switch to std::vector or a database
### Duplicate-ID checks: 
the C++ version does not yet stop two records sharing an ID
### Assign a doctor to a patient: 
the doctor and appointmentDate fields exist on patient but are not yet filled in by any form
### Appointment management:
edit, reschedule, and cancel appointments; prevent double-booking a doctor
### Search and filtering: 
find appointments by date, doctor, or status
### Input validation: 
check dates, phone numbers, and required fields
### Automated tests: 
unit tests for each class
### Shared Person base class:
move fields common to patient and doctor (name, gender, address) into one parent class
## AI Assistance Disclosure

The core system (the C++ classes, the role-based menus, and the text-file storage) is my own work, written for my OOP coursework at the University of Mines and Technology (UMaT).

The C# (Blazor) web front end was built with the help of an AI assistant (Claude, by Anthropic) as an extension beyond the course requirements. It reads and writes the same data files and follows the same roles and rules as the C++ program.

Author

Ampong Stephen— Computer Science and Engineering, University of Mines and Technology (UMaT)
