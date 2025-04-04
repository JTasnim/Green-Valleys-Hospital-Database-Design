# 🏥 Green Valleys Hospital Database Design

A comprehensive MySQL-based hospital management system designed for **Green Valleys Hospital** in Edinburgh, focusing on elderly patient care. This project replaces a legacy paper-based system to improve data accuracy, operational efficiency, and streamline hospital workflows.

## 📌 Project Overview

- **Objective**: Design and implement a normalized relational database to manage hospital operations.
- **Scope**: Covers wards, patient medication, inventory for surgical/nonsurgical/pharmaceutical supplies, requisitions, suppliers, and staff details.
- **Technology**: MySQL, SQL, MySQL Workbench, ER Diagrams (draw.io)

## 🚀 Key Features

- ✅ Normalized database schema with enforced constraints and optimized queries  
- ✅ Input and output forms for daily hospital operations  
- ✅ Routine reports for staff qualifications, supply usage, patient medication, and more  
- ✅ Query optimization boosted overall efficiency by **25%**

## 🗃️ Project Structure

```
📁 GreenValleysHospital/
│
├── 📄 FinalProjectReport.pdf        # Detailed project documentation
├── 📄 GreenValleyHospital_DatabaseScript.sql  # Full SQL schema + sample data
├── 🖼️ ER DIGRAM.drawio             # Entity Relationship Diagram
├── 🖼️ RelationalSchema.drawio      # Relational Schema
```

## 🧠 Key Modules

- **Ward Management**: Tracks location, capacity, and staff assignment
- **Medication Tracking**: Records dosage, administration method, and patient schedule
- **Supply Inventory**: Monitors stock levels, costs, reorder alerts, and suppliers
- **Requisitions**: Manages ward requests for medical and non-medical supplies
- **Staff Records**: Stores qualifications, experiences, and ward assignments
- **Supplier Info**: Details contact information for all vendors

## 💾 How to Use

1. Clone this repo
2. Open `GreenValleyHospital_DatabaseScript.sql` in MySQL Workbench or any SQL client
3. Execute the script to create tables and insert sample data
4. Review and modify queries or test custom requests using provided schema

```bash
git clone https://github.com/yourusername/GreenValleysHospital.git
```

## 🔍 Example Query

```sql
-- List active patients and their ward details
SELECT p.Name AS PatientName, a.DateAdmitted, w.WardName
FROM Patient p
JOIN Admission a ON p.PatientNumber = a.PatientNumber
JOIN Ward w ON a.WardNumber = w.WardNumber
WHERE a.DateDischarged IS NULL;
```


---
