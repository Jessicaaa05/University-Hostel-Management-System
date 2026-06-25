# Business Rules

This document describes the business rules governing the University Hostel Management System database.

## Campus Management

1. Each campus is identified by a unique `Campus_ID`.
2. A campus can contain multiple hostel blocks.
3. Each hostel block must belong to exactly one campus.

---

## Block Management

1. Each hostel block is identified by a unique `Block_ID`.
2. A block is designated for either male or female students.
3. A block can contain multiple rooms.
4. A block may be assigned to a shuttle bus service.
5. A block can have multiple security records.

---

## Room Management

1. Each room is identified by a unique `Room_ID`.
2. A room belongs to exactly one hostel block.
3. A room has a predefined capacity.
4. A room can accommodate multiple students, provided the capacity limit is not exceeded.
5. A room can have multiple maintenance service records.

---

## Student Management

1. Each student is identified by a unique `Student_ID`.
2. A student can only be assigned to one room at a time.
3. A student may make multiple hostel-related payments.
4. A student may receive multiple visitors.

---

## Visitor Management

1. Each visitor is identified by a unique `Visitor_ID`.
2. A visitor must be associated with a registered student.
3. Visitor information and visit records must be maintained for security purposes.
4. Multiple visitors may visit the same student on different occasions.

---

## Payment Management

1. Each payment is identified by a unique `Payment_ID`.
2. Each payment record must belong to one student.
3. Payment transactions are processed by an employee.
4. A student may have multiple payment records.

---

## Employee Management

1. Each employee is identified by a unique `Employee_ID`.
2. Each employee belongs to one campus.
3. An employee may process multiple payment records.
4. An employee may handle multiple room maintenance services.
5. An employee may be assigned to multiple security duties.

---

## Room Maintenance Services

1. Each maintenance service request is identified by a unique `Maintenance_ID`.
2. A maintenance service request must be associated with one room.
3. Maintenance services are handled by assigned employees.
4. A room may have multiple maintenance records over time.

---

## Security Records

1. Each security record is identified by a unique `SecurityRecord_ID`.
2. Security duties are assigned to employees.
3. Security records are associated with specific hostel blocks.
4. A block may have multiple security records.

---

## Transportation Services

1. Each shuttle bus is identified by a unique `Shuttle_bus_ID`.
2. A shuttle bus may serve multiple hostel blocks.
3. Transportation information is maintained to support student mobility between hostel blocks and campus facilities.

---

## Database Integrity Rules

1. Every table must have a primary key.
2. Foreign keys must reference valid records in related tables.
3. Duplicate primary key values are not allowed.
4. Referential integrity must be maintained between related tables.
5. Deleting parent records should not create orphan records in related tables.

---

## Relationship Summary

| Parent Entity  | Child Entity             | Relationship |
| -------------- | ------------------------ | ------------ |
| Campus         | Block                    | One-to-Many  |
| Campus         | Employee                 | One-to-Many  |
| Block          | Room                     | One-to-Many  |
| Block          | Security Record          | One-to-Many  |
| Room           | Student                  | One-to-Many  |
| Room           | Room Maintenance Service | One-to-Many  |
| Student        | Visitor                  | One-to-Many  |
| Student        | Payment                  | One-to-Many  |
| Employee       | Payment                  | One-to-Many  |
| Employee       | Room Maintenance Service | One-to-Many  |
| Employee       | Security Record          | One-to-Many  |
| Transportation | Block                    | One-to-Many  |
