# 🚇 Metro Self-Service Machine – UiPath RPA Project

A UiPath-based RPA workflow that simulates a Delhi Metro Self-Service Recharge Machine.


This project simulates a **Delhi Metro Self-Service Token Booking Machine** built using UiPath. The bot allows users to select balance, choose source and destination stations, and book metro tickets based on fare — just like a real-life metro kiosk!

---

## 📌 Project Highlights

- ✅ Built in UiPath Studio (Windows - Legacy)
- 🗓️ Assignment Date: 21 July 2025  
- ✅ Completed: 23 July 2025  
- 💼 Internship Project at: **Chiacon Consulting Pvt. Ltd.**

---

## 🎯 Objective

To automate a Metro Ticket Self-Service System where:
- User selects initial card balance
- Selects Source and Destination Stations
- Bot checks fare and deducts balance
- Offers re-booking or top-up if needed

---

## 🧠 Key Features & Workflow

### 🔷 Step-by-Step Bot Flow:

1. **User Input (Input Dialog Box)**  
   - Name & Initial Balance (₹50/₹100/₹200/₹500)

2. **Excel File Reading (Excel Process Scope + Read Range)**  
   - Read data from `Metro Fare Data.xlsx`
   - Data stored in a DataTable variable

3. **Get Unique Source & Destination Stations**  
   - Used **Filter DataTable** to extract only `Source` column  
   - Then applied **Remove Duplicate Rows** to get unique values  
   - Converted values into array (String Manipulation)  
   - Displayed unique options to user using **Multiple Choice Dialog**

4. **Fare Calculation (For Each Row Activity)**  
   - Used logic to compare user-selected source and destination  
   - Retrieved fare from DataTable based on match

5. **Fare Deduction & Loop**  
   - Compared balance and fare  
   - If sufficient balance: show success message and deduct fare  
   - If insufficient: show top-up option (₹50, ₹100, etc.), update balance

6. **Loop Ticket Booking**  
   - After each booking, ask user:  
     “Do you want to book another ticket?”  
   - If yes, loop restarts  
   - If no, final message with summary (booked tickets & remaining balance)

7. **Exception Handling**  
   - Used **IF condition** to check empty source or destination  
   - Displayed warning messages accordingly  
   - Validated negative or zero balance conditions  
   - Ensured user experience remains smooth even during invalid inputs

---

## 🧰 Activities & Concepts Used

- `Input Dialog`
- `Multiple Choice Dialog`
- `Excel Process Scope`
- `Read Range`
- `Filter DataTable`
- `Remove Duplicate Rows`
- `For Each Row`
- `If Condition`
- `String Manipulation (Replace, Split)`
- `Message Box`
- `Exception Handling (Try-Catch)`

---

## 📁 Files Included

- `Main.xaml` – Main workflow file  
- `Metro Fare Data.xlsx` – Excel sheet with sample station data  
- `project.json` – UiPath project config  
- `Screenshots / Video`

---

## 🔗 Author

👨‍💻 Gagan Grover  
📧 gagangrover986@gmail.com  
🔗 [LinkedIn Profile](www.linkedin.com/in/gagan-grover-18b794373)

---

## 💡 Future Enhancements

- Add user authentication
- Export booked tickets to Excel or PDF
- UI enhancements with custom forms
- Auto-balance suggestion and route planner

---

## 🏷️ Tags

`UiPath` `RPA Project` `Excel Automation` `DataTable Manipulation` `Dialog Box` `For Each Row` `Internship Assignment` `Metro Booking System`
