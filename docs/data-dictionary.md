# 📚 Data Dictionary

## CAMPUS

| Attribute Name | Content | Type | Format | Required | PK/FK | Reference Table |
|---------------|----------|------|--------|----------|--------|----------------|
| Campus_ID | Campus Identification (auto increment) | Int(5) | Xxxxxx | Y | PK | |
| Campus_Location | Campus location | VChar(255) | Xxxxxx | Y | | |
| Campus_ContactNo | Campus contact number | VChar(255) | 99-9999 | Y | | |

---

## BLOCK

| Attribute Name | Content | Type | Format | Required | PK/FK | Reference Table |
|---------------|----------|------|--------|----------|--------|----------------|
| Block_ID | Block identification | Int(5) | 99999 | Y | PK | |
| Block_Name | Block name | VChar(255) | Xxxxxx | Y | | |
| Block_ContactNo | Block contact number | Int(20) | 99-9999 | Y | | |
| Block_CctvCode | Block cctv code | Int(20) | 99999 | | | |
| Block_Location | Block location | VChar(255) | Xxxxxx | | | |
| Block_Gender | Block gender | VChar(255) | Xxxxxx | | | |
| Block_Capacity | Block capacity | Int(5) | 99999 | | | |
| ShuttleBus_ID | Shuttle bus identification | VChar(5) | Xx999 | Y | FK | TRANSPORTATION |
| Campus_ID | Campus identification | Int(20) | 99999 | Y | FK | CAMPUS |

---

## ROOM

| Attribute Name | Content | Type | Format | Required | PK/FK | Reference Table |
|---------------|----------|------|--------|----------|--------|----------------|
| Room_ID | Room identification | VChar(5) | 9999X | Y | PK | |
| Room_Type | Room type | VChar(255) | Xxxxxx | | | |
| Date_check_in | Check in date | Date | 99/99/99 | | | |
| Room_Status | Room status | VChar(255) | Xxxxxx | Y | | |
| Block_ID | Block identification | Int(5) | 99999 | Y | FK | BLOCK |

---

## STUDENT

| Attribute Name | Content | Type | Format | Required | PK/FK | Reference Table |
|---------------|----------|------|--------|----------|--------|----------------|
| Stud_ID | Student identification | Int(10) | 99999 | Y | PK | |
| Stud_Name | Student name | VChar(255) | Xxxxxx | Y | | |
| Stud_Gender | Student gender | VChar(255) | Xxxxxx | Y | | |
| Stud_ContactNo | Student contact number | VChar(255) | 99-9999 | | | |
| Stud_email | Student email | VChar(255) | Xxxxxx | | | |
| Room_ID | Room identification | VChar(5) | 9999X | | FK | ROOM |
| Block_ID | Block identification | Int(5) | 99999 | | FK | BLOCK |
| Campus_ID | Campus identification | Int(5) | 99999 | Y | FK | CAMPUS |

---

## VISITOR

| Attribute Name | Content | Type | Format | Required | PK/FK | Reference Table |
|---------------|----------|------|--------|----------|--------|----------------|
| Pass_ID | Visitor identification | CHAR(5) | Xxxxx | Y | PK | |
| Visitor_Name | Visitor name | VChar(255) | Xxxxxx | Y | | |
| Visitor_Gender | Visitor gender | VChar(255) | Xxxxxx | Y | | |
| Visitor_ContactNo | Visitor contact number | VChar(255) | 99-9999 | Y | | |
| Visit_Date | Visit date | Date | 99/99/99 | Y | | |
| Entry_Time | Entry time | Time | 99:99 | | | |
| Exit_Time | Exit time | Time | 99:99 | | | |
| Stud_ID | Student identification | Int(5) | Xxxxx | Y | FK | STUDENT |
| Room_ID | Room identification | VChar(5) | 99999 | Y | FK | ROOM |

---

## ROOM MAINTENANCE SERVICE

| Attribute Name | Content | Type | Format | Required | PK/FK | Reference Table |
|---------------|----------|------|--------|----------|--------|----------------|
| RMS_ID | Maintenance identification | Int(10) | Xxxxxx | Y | PK | |
| RMS_type | Service type | VChar(255) | Xxxxxx | Y | | |
| RMS_Date | Maintenance date | Date | 99/99/99 | Y | | |
| RMS_cost | Maintenance cost | Int(10) | Xxxxxx | Y | | |
| RMS_Status | Maintenance status | VChar(255) | Xxxxxx | Y | | |
| Room_ID | Room identification | VChar(5) | 9999X | Y | FK | ROOM |
| Emp_ID | Employee identification | Int(5) | 99999 | | FK | EMPLOYEE |

---

## EMPLOYEE

| Attribute Name | Content | Type | Format | Required | PK/FK | Reference Table |
|---------------|----------|------|--------|----------|--------|----------------|
| Emp_ID | Employee identification | Int(5) | Xxxxxx | Y | PK | |
| Emp_Name | Employee name | VChar(255) | Xxxxxx | Y | | |
| Emp_Email | Employee email | VChar(255) | Xxxxxx | | | |
| Emp_ContactNo | Employee contact number | VChar(255) | 99-9999 | Y | | |
| Emp_Department | Employee department | VChar(255) | Xxxxxx | | | |
| Emp_Address | Employee address | VChar(255) | Xxxxxx | Y | | |
| Campus_ID | Campus identification | Int(5) | Xxxxxx | | FK | CAMPUS |

---

## SECURITY RECORD

| Attribute Name | Content | Type | Format | Required | PK/FK | Reference Table |
|---------------|----------|------|--------|----------|--------|----------------|
| SecurityRec_ID | Security record (auto increment) | Int(20) | Xxxxxx | Y | PK | |
| SecurityRec_Date | Security record date | Date | 99/99/99 | Y | | |
| SecurityRec_Start_time | Security record start time | Time | Xxxxxx | Y | | |
| SecurityRec_End_time | Security record end time | Time | Xxxxxx | Y | | |
| Emp_ID | Employee identification | Int(5) | 99999 | | FK | EMPLOYEE |
| Block_ID | Block identification | Int(5) | 99999 | | FK | BLOCK |

---

## PAYMENT

| Attribute Name | Content | Type | Format | Required | PK/FK | Reference Table |
|---------------|----------|------|--------|----------|--------|----------------|
| Payment_ID | Payment identification (auto increment) | Int(255) | 99999 | Y | PK | |
| Payment_Date | Payment date | Date | 99/99/99 | Y | | |
| Payment_Amount | Payment amount | Decimal(10,2) | RM99.99 | Y | | |
| Payment_type | Payment type | VChar(255) | Xxxxxx | | | |
| Payment_status | Payment status | VChar(255) | Xxxxxx | | | |
| Emp_ID | Employee identification | Int(5) | 99999 | | FK | EMPLOYEE |
| Stud_ID | Student identification | Int(10) | 99999 | | FK | STUDENT |

---

## TRANSPORTATION

| Attribute Name | Content | Type | Format | Required | PK/FK | Reference Table |
|---------------|----------|------|--------|----------|--------|----------------|
| ShuttleBus_ID | Shuttle bus identification | VChar(5) | Xx999 | Y | PK | |
| Transp_StartingTime | Transportation starting time | Time | 99:99 | Y | | |
| Transp_EndingTime | Transportation ending time | Time | 99:99 | Y | | |
| Travel_Location | Travel location | VChar(255) | Xxxxxx | | | |
| Bus_Capacity | Bus capacity | Int(5) | 99999 | | | |