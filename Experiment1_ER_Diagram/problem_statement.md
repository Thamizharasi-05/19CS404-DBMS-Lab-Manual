# ER Diagram Workshop – Submission Template

## Objective
To understand and apply ER modeling concepts by creating ER diagrams for real-world applications.

## Purpose
Gain hands-on experience in designing ER diagrams that represent database structure including entities, relationships, attributes, and constraints.

---

# Scenario A: City Fitness Club Management

**Business Context:**  
FlexiFit Gym wants a database to manage its members, trainers, and fitness programs.

**Requirements:**  
- Members register with name, membership type, and start date.  
- Each member can join multiple programs (Yoga, Zumba, Weight Training).  
- Trainers assigned to programs; a program may have multiple trainers.  
- Members may book personal training sessions with trainers.  
- Attendance recorded for each session.  
- Payments tracked for memberships and sessions.

### ER Diagram:

<img width="725" height="522" alt="image" src="https://github.com/user-attachments/assets/fb37fcbf-05a9-46f2-b5f7-9cacd9800f7e" />

### Entities and Attributes

1.Members 
Member ID 
Member Name 
Membership Type 
2.Program 
Program ID 
Program Name 
Duration 
3.Trainer 
Trainer ID 
Trainer Name 
Contact Number 
4.Payment 
Payment ID 
Payment Type 
Payment Amount 
Expire Date 

### Relationships and Constraints

Member – Program → M:N (via Enrolment) 
Program – Trainer → M:N (via Assignment) 
Member – Payment →1:N 

### Assumptions
1.Every user must register as a member before accessing gym services.
2.A member has a unique contact number.
3.Each session or class is led by exactly one trainer.
4.Trainers can conduct multiple sessions but not at overlapping times.
---

# Scenario B: City Library Event & Book Lending System

**Business Context:**  
The Central Library wants to manage book lending and cultural events.

**Requirements:**  
- Members borrow books, with loan and return dates tracked.  
- Each book has title, author, and category.  
- Library organizes events; members can register.  
- Each event has one or more speakers/authors.  
- Rooms are booked for events and study.  
- Overdue fines apply for late returns.

### ER Diagram:

<img width="704" height="437" alt="image" src="https://github.com/user-attachments/assets/edc9f77f-ff7b-4600-800a-1477016719e7" />

### Entities and Attributes

1.Member 
Member ID  
Name 
Contact 
Membership Date 
2.Book 
Book ID  
Title 
Author 
Category 
3.Loan  
Loan ID  
Loan Date 
Return Date 
Fine Amount 
4.Event 
Event ID  
Event Name 
Event Date 
Event Type 
5.Speaker 
Speaker ID  
Name 
Profession 
Contact 
6.Room 
Room ID  
Room Name 
Capacity 
Location 

### Relationships and Constraints

1.Member – Loan – Book → M:N resolved via Loan 
2.Member – Event → M:N resolved via EventRegistration 
3.Event – Speaker → M:N (one event can have many speakers, one speaker can talk at many events) 
4.Event – Room → 1:N (a room can host many events, each event uses one room) 

### Assumptions
1.A member must be registered before borrowing books or registering for events.
2.Member contact number is unique.
3.Each loan refers to a single book and a single member.
4.Loan must have both a loan date and due date.
5.Every book belongs to exactly one category
---

# Scenario C: Restaurant Table Reservation & Ordering

**Business Context:**  
A popular restaurant wants to manage reservations, orders, and billing.

**Requirements:**  
- Customers can reserve tables or walk in.  
- Each reservation includes date, time, and number of guests.  
- Customers place food orders linked to reservations.  
- Each order contains multiple dishes; dishes belong to categories (starter, main, dessert).  
- Bills generated per reservation, including food and service charges.  
- Waiters assigned to serve reservations.

### ER Diagram:
 
<img width="735" height="457" alt="image" src="https://github.com/user-attachments/assets/0ebaca27-8303-485b-9fe7-f348f6593af2" />

### Entities and Attributes

1.Customer  
Customer ID  
Name 
Phone no  
2.Reservation  
Reservation ID  
Reservation date and time 
Customer ID 
3.Table 
Table ID  
Table number  
Capacity  
4.Category 
Category ID 
Category Name  
5.Dish 
Dish ID 
Name  
Price  
Category ID  
6.Order 
Order ID  
Order time 
Reservation ID  
Waiter ID  
7.Bill 
Bill ID  
Total amount  
Order ID  
8.Waiter  
Waiter ID  
Name  
Phone no  
 

### Relationships and Constraints

1Customer ↔️ Reservation  
a.One customer books many reservations. Each reservation belongs to one customer. 1 : N  
2.Reservation ↔️ Table  
a.One reservation is assigned to one table. A table can be assigned to many reservations (over time). 1 : N  
3.Reservation ↔️ Order  
a.One reservation generates one or many orders. Each order belongs to exactly one reservation. 1 : N 
4.Waiter ↔️ Order  
a.One waiter serves many orders. Each order is served by exactly one waiter. 1 : N  
5.Order ↔️ Bill  
a.Each order produces one bill. Each bill is linked to only one order. 1 : 1  
6.Bill ↔️ Dish  
a.A bill contains many dishes. Each dish can appear in many bills. M : N  
7.Dish ↔️ Category  
a.Each dish belongs to one category. A category can contain many dishes. 1 : N 
### Assumptions

1.A customer must register before making a reservation
2.Every reservation requires a valid and unique customerID.
3.A table may serve multiple reservations, but not simultaneously
4.Each order must be served by exactly one waiter
5.A customer can have multiple reservations
6.But no double-booking at the same date and time in the same table.
7.Contact details like phone number are assumed unique.
8.Order time is recorded

---

## Instructions for Students

1. Complete **all three scenarios** (A, B, C).  
2. Identify entities, relationships, and attributes for each.  
3. Draw ER diagrams using **draw.io / diagrams.net** or hand-drawn & scanned.  
4. Fill in all tables and assumptions for each scenario.  
5. Export the completed Markdown (with diagrams) as **a single PDF**
