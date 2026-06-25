# 🗄 Database Tables

## Block Table

| Block_ID | Block_Name | Block_ContactNo | Block_CctvCode | Block_Location | Block_Gender | Block_Capacity | Shuttle_bus_ID | Campus_ID |
| -------- | ---------- | --------------- | -------------- | -------------- | ------------ | -------------- | -------------- | --------- |
| 1        | Block A    | 3               | 1923           | South Street   | Female       | 50             | WW443          | 1         |
| 2        | Block B    | 3               | 1888           | North Street   | Female       | 50             | VV234          | 1         |
| 3        | Block C    | 3               | 7865           | West Street    | Male         | 50             | WW443          | 1         |
| 4        | Block D    | 3               | 9507           | East Street    | Male         | 50             | VL123          | 1         |
| 5        | Block A    | 3               | 3456           | South Street   | Female       | 50             | VY375          | 2         |
| 6        | Block B    | 3               | 1895           | North Street   | Female       | 50             | QA659          | 2         |
| 7        | Block C    | 3               | 5641           | West Street    | Male         | 50             | VY375          | 2         |
| 8        | Block D    | 3               | 8972           | East Street    | Male         | 50             | WW671          | 2         |

---

## Campus Table

| Campus_ID | Campus_Location | Campus_ContactNo |
| --------- | --------------- | ---------------- |
| 1         | Cyberjaya       | 03-83125803      |
| 2         | Melaka          | 06-2523443       |

---

## Room Table

| Room_ID | Room_Type | Date_Check_In | Room_Status    | Block_ID |
| ------- | --------- | ------------- | -------------- | -------- |
| 1001A   | Single    | 2023-08-19    | Occupied       | 1        |
| 1002A   | Double    | 2023-08-10    | Occupied       | 1        |
| 2005B   | Suite     | 2022-01-05    | 1 bed occupied | 6        |
| 2008B   | Single    | NULL          | Vacant         | 2        |
| 3011D   | Suite     | 2023-02-02    | Occupied       | 4        |
| 4020C   | Double    | 2022-06-05    | Occupied       | 3        |
| 4099C   | Single    | 2023-08-09    | Occupied       | 7        |

---

## Student Table

| Stud_ID    | Stud_Name       | Stud_Gender | Stud_ContactNo | Stud_Email                                                | Room_ID | Block_ID | Campus_ID |
| ---------- | --------------- | ----------- | -------------- | --------------------------------------------------------- | ------- | -------- | --------- |
| 122000898  | Muhammad Fattih | Male        | 017-1132228    | [fattimhaqq@gmail.com](mailto:fattimhaqq@gmail.com)       | 3011D   | 4        | 1         |
| 1220021702 | Kok Wei Boon    | Male        | 016-1184512    | [kokweiboon123@gmail.com](mailto:kokweiboon123@gmail.com) | 4099C   | 7        | 2         |
| 1220045677 | Ana Kariya      | Male        | 012-5975466    | [anakariya87@gmail.com](mailto:anakariya87@gmail.com)     | 3011D   | 4        | 1         |
| 1220051585 | Noora Asya      | Female      | 013-3345211    | [nooraasya00@gmail.com](mailto:nooraasya00@gmail.com)     | 1001A   | 1        | 1         |
| 1220211123 | Nor Diana Alif  | Female      | 016-2080553    | [dianaalif@gmail.com](mailto:dianaalif@gmail.com)         | 1002A   | 1        | 1         |

---

## Employee Table

| Emp_ID | Emp_Name          | Emp_Email                                               | Emp_ContactNo | Emp_Department | Campus_ID |
| ------ | ----------------- | ------------------------------------------------------- | ------------- | -------------- | --------- |
| 1134   | Winnie            | [winnie@gmail.com](mailto:winnie@gmail.com)             | 03-9097787    | Security       | 1         |
| 1279   | Jun Wei           | [junwei33@gmail.com](mailto:junwei33@gmail.com)         | 07-3733779    | Finance        | 2         |
| 1823   | Istri Arnina Jana | [arninjana121@gmail.com](mailto:arninjana121@gmail.com) | 02-2135332    | Transportation | 1         |
| 2187   | Nena Bin Ifty     | [nanabinifty@gmail.com](mailto:nanabinifty@gmail.com)   | 02-6666002    | Transportation | 1         |
| 2231   | Roger Lim         | [rogerlim@gmail.com](mailto:rogerlim@gmail.com)         | 05-5555655    | Maintenance    | 1         |

---

## Payment Table

| Payment_ID | Payment_Date | Payment_Amount | Payment_Type         | Payment_Status | Emp_ID | Stud_ID    |
| ---------- | ------------ | -------------- | -------------------- | -------------- | ------ | ---------- |
| 1          | 2023-08-12   | 130.00         | Deposit              | Submitted      | 3298   | 1220051585 |
| 2          | 2023-08-08   | 460.00         | 1st month Hostel fee | Processing     | 1279   | 1220021702 |
| 3          | 2023-08-12   | 230.00         | 1st month Hostel fee | Submitted      | 3298   | 1221221892 |

---

## Room Maintenance Service Table

| RMS_ID | RMS_Type                  | RMS_Date   | RMS_Cost | RMS_Status | Room_ID | Emp_ID |
| ------ | ------------------------- | ---------- | -------- | ---------- | ------- | ------ |
| 1367   | Fan repair service        | 2023-09-23 | 120      | Completed  | 1001A   | 2231   |
| 2546   | Light bulb repair service | 2023-10-01 | 58       | Completed  | 4020C   | 2231   |
| 3643   | Wall painting             | 2023-10-12 | 64       | Processing | 1002A   | 7749   |

---

## Visitor Table

| Pass_ID | Visitor_Name   | Visitor_Gender | Visitor_ContactNo | Visit_Date | EntryTime | ExitTime | Stud_ID    | Room_ID |
| ------- | -------------- | -------------- | ----------------- | ---------- | --------- | -------- | ---------- | ------- |
| QSFA    | Jim Qi         | Female         | 06-9875261        | 2023-09-01 | 12:00     | 12:03    | 1220211123 | 1002A   |
| QSFC    | Syaza Alif     | Female         | 02-7876523        | 2023-09-05 | 15:00     | 19:26    | 1221091976 | 4020C   |
| QSFD    | Muhammad Hijil | Male           | 06-7342222        | 2023-09-13 | 10:46     | 18:00    | 1220051585 | 1001A   |

---

## Security Record Table

| SecurityRec_ID | SecurityRec_Date | SecurityRec_Start_Time | SecurityRec_End_Time | Emp_ID | Block_ID |
| -------------- | ---------------- | ---------------------- | -------------------- | ------ | -------- |
| 11253186       | 2023-09-01       | 07:00                  | 19:00                | 6784   | 5        |
| 12332799       | 2023-09-03       | 00:00                  | 07:00                | 5011   | 1        |
| 12638999       | 2023-09-02       | 19:00                  | 24:00                | 6784   | 6        |

---

## Transportation Table

| Shuttle_bus_ID | Transp_StartingTime | Transp_EndingTime | Travel_Location  | Bus_Capacity |
| -------------- | ------------------- | ----------------- | ---------------- | ------------ |
| QA659          | 17:45               | 20:15             | Hujung Bus Stop  | 30           |
| VL123          | 18:15               | 18:45             | Cyberjaya Utara  | 30           |
| VY375          | 12:15               | 12:45             | MMU Entrance A   | 30           |
| VV234          | 10:15               | 10:45             | Cyberjaya Utara  | 30           |
| WW443          | 07:30               | 08:00             | MMU Entrance B   | 30           |
| WW671          | 15:00               | 15:30             | Sempang Bus Stop | 30           |
