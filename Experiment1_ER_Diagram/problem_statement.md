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

# ER Diagram Submission - Student Name:
### NAME: MOHANRAJ.S
### REGISTER NO: 212224100036

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

Relationships:
1. Consults (Patient ↔ Doctor)
A patient consults one or more doctors
A doctor can consult up to 2 patients at a time

3. Assigned (Patient → Doctor)
Patients are assigned to specific doctors for treatment

3. Governs (Room → Patients)
One room can accommodate multiple patients
A patient is assigned to one room

4. Hosts (Room → Bill)
A room is associated with one or more bills

5. Maintains (Receptionist → Record)
Receptionists maintain records containing appointment and patient info

6. Has (Patient → Test Report)
A patient can have multiple test reports

7. ISA Relationship (Employee → Doctor/Nurse/Receptionist)
Specialization of employees into specific roles

Constraints:
Cardinality Constraints:
A doctor can consult up to 2 patients at a time
A room can be assigned to many patients
Each patient is assigned to one room
Each patient can have many bills and test reports
Participation Constraints:
Patients must be linked to at least one doctor and room
Receptionists must be linked to at least one record

### Extension (Prerequisite / Billing):
### Extension (Prerequisite / Billing) – Simple Explanation:
To extend the ER diagram with a Billing prerequisite, we can add more detail to the billing process, which is an important part of hospital management.
New/Extended Entities and Attributes:

1. Billing (extended)
Existing: Bill_ID, Amount
Add: Date, Payment_Mode (Cash/Card/Online), Status (Paid/Unpaid)

2. Prerequisite:
A Patient must have a Test Report or Doctor Consultation before a bill is generated.

A Bill is only created after services like room assignment, consultation, or testing.

Updated Relationships:
Patient → Billing: A patient can have multiple bills.
Billing ← Test Report / Consultation / Room: A bill depends on these services.
Constraint: A bill cannot exist without at least one of these services being completed.

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
