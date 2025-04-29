### NAME: MOHANRAJ.S
### REGISTER NO: 212224100036

# Experiment 1: Entity-Relationship (ER) Diagram

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.
- Students have admission number, name, DOB, contact info.
- Instructors with staff number, contact info, etc.
- Courses have number, name, credits.
- Track course enrollments by students and enrollment date.
- Add support for prerequisites (some courses require others).

---

### 🔹 Scenario 2: Hospital Database
Design a database for patient management, appointments, medical records, and billing.

**User Requirements:**
- Patient details including contact and insurance.
- Doctors and their departments, contact info, specialization.
- Appointments with reason, time, patient-doctor link.
- Medical records with treatments, diagnosis, test results.
- Billing and payment details for each appointment.

---

## 📝 Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for University OR Billing for Hospital
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites or billing.

# ER Diagram Submission - Student Name

## Scenario Chosen:
### Hospital Database:

## ER Diagram:
![Screenshot 2025-04-29 084010](https://github.com/user-attachments/assets/c629f368-94e7-4d7c-8268-7f412b97723a)


## Entities and Attributes:
 Entity1: Patients
 Entity2: Employee
 Entity3: Doctor
 Entity4: Nurse
 Entity5: Receptionalist
 Entity6: Records
 Entity7: Bills
 Entity8: Test Reports
 Entity9: Rooms
...

## Relationships and Constraints:
- Relationship1 (Patients, Doctors)
- Relationship2 (Cardinality, Participation)
...

### Extension (Prerequisite / Billing):
This ER diagram represents a hospital management system, detailing the relationships between various entities involved in hospital operations. The central entity is the Patient, identified by attributes such as patient ID, name, age, gender, date of birth, and mobile number. Patients consult Doctors, who are specialized Employees with additional attributes like department and qualification. Doctors, along with Nurses and Receptionists, fall under the general Employee entity through an "ISA" relationship, which includes shared attributes such as employee ID, name, gender, salary, mobile number, and address details (city, state, pin code).

Patients are assigned to Rooms, which have attributes like room ID, type, capacity, and availability. A "Governs" relationship indicates that one room can host multiple patients. Additionally, each patient can receive Bills (identified by bill ID and amount) and undergo various Test Reports, which include test type, result, and reference ID, and are linked back to the patient through their ID.

Receptionists are responsible for maintaining Records, which include record number and appointment number, establishing a link between administrative staff and patient data. Overall, the diagram provides a comprehensive view of the interactions and data flow within a hospital system, covering medical, administrative, and infrastructural aspects.

### Design Choices:
This ER diagram is designed to show how different parts of a hospital system are connected. The main entities like Patient, Doctor, Nurse, Receptionist, Room, Bill, and Test Report are chosen because they represent real people or things in a hospital.
We use an Employee entity for all staff members and connect Doctor, Nurse, and Receptionist to it using "ISA" to avoid repeating common details like name, salary, and address.
Relationships such as Consults (between Patient and Doctor), Assigned (Doctor to Patient), and Governs (Room to Patient) are used to show how these people and things interact.
Some assumptions are made, like:
One room can have many patients.
A doctor can consult with multiple patients, but only up to 2 at a time.
This setup helps organize hospital data clearly and logically, just like it would work in real life.

### RESULT:
The ER diagram successfully models the hospital system by clearly representing entities, their attributes, and real-life relationships for efficient data management.
