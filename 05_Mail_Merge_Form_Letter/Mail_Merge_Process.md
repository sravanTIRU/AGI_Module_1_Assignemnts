# Mail Merge Practical — Student Software Career Domain Preference

## 1. What is the dataset about?

The dataset contains information about **20 students and their preferred software career domains**.

The purpose is to use this data to create personalized letters from each student to a faculty member using **Microsoft Word Mail Merge**.

Each student has:
- A primary software career domain
- A secondary domain of interest
- Current skill level
- Preferred technology

### Career domains included

- Frontend Development
- Backend Development
- Full Stack Development
- DevOps
- Cloud Computing
- Data Science
- Data Engineering
- Cybersecurity
- Mobile Development
- Software Testing
- Artificial Intelligence
- Database Development

---

## 2. About the letter

The letter is written **from the student to the faculty member**.

The student formally communicates their preferred software career domain and requests guidance about the appropriate learning and career path.

The letter contains:
1. Student identity
2. Course and year/semester
3. Primary career-domain preference
4. Secondary career-domain preference
5. Current skill level
6. Preferred technology
7. Request for faculty guidance

Instead of preparing 20 letters manually, Mail Merge automatically inserts the correct information for every student.

---

## 3. Dataset fields

| Field | Purpose |
|---|---|
| `Student_ID` | Unique student ID |
| `Student_Name` | Student name |
| `Course` | Student course |
| `Year_Semester` | Current year/semester |
| `Student_Email` | Student email |
| `Faculty_Name` | Faculty name |
| `Designation` | Faculty designation |
| `Department` | Department |
| `Institution_Name` | Institution |
| `Domain` | Primary software career preference |
| `Secondary_Domain` | Secondary career preference |
| `Skill_Level` | Current skill level |
| `Preferred_Technology` | Preferred technology |
| `Date` | Date of letter |

---

# 4. What is Mail Merge?

**Mail Merge** is a Microsoft Word feature that combines:

1. A **main document** — the letter template
2. A **data source** — the Excel dataset

Word takes information from each row of the Excel file and inserts it into the appropriate fields in the letter.

### Basic process

```text
Excel Dataset
      ↓
Word Letter Template
      ↓
Insert Mail Merge Fields
      ↓
Preview Results
      ↓
Generate Personalized Letters
```

For this practical:

```text
20 Student Records
        +
1 Letter Template
        ↓
20 Personalized Letters
```

---

# 5. Prepare the Excel dataset

Open:

`Student_Career_Domain_Mail_Merge_Dataset.xlsx`

Make sure:

- The first row contains column names.
- Each student occupies one row.
- There are no completely blank rows inside the dataset.
- The file is saved before starting Mail Merge.
- Column names are unique and clear.

Example:

| Student_ID | Student_Name | Domain | Secondary_Domain | Skill_Level |
|---|---|---|---|---|
| ST001 | Rahul Kumar | Backend Development | DevOps | Beginner |
| ST002 | Priya Sharma | Frontend Development | Full Stack Development | Intermediate |
| ST003 | Arjun Reddy | DevOps | Cloud Computing | Beginner |

Save and close Excel after checking the data.

---

# 6. Create the letter in Microsoft Word

Open **Microsoft Word** and create a blank document.

Use this letter structure:

```text
From:
«Student_Name»
«Student_ID»
«Course»
«Year_Semester»
«Student_Email»

To:
«Faculty_Name»
«Designation»
«Department»
«Institution_Name»

Date: «Date»

Subject: Submission of Preferred Software Career Domain

Respected Sir/Madam,

I am «Student_Name», a student of «Course», currently studying in
«Year_Semester». As part of the career guidance and domain selection
activity, I am writing to formally submit my preferred area of interest
for pursuing a career in the software industry.

After considering my interests and current skills, I would like to
select the following domain as my primary career preference:

Preferred Domain: «Domain»

My secondary area of interest is:

Secondary Domain: «Secondary_Domain»

My current skill level in the selected area is «Skill_Level», and the
technology that I am particularly interested in learning or working
with is «Preferred_Technology».

I would like to develop my knowledge and practical skills in my
selected domain through appropriate coursework, hands-on projects,
technical training, and industry-oriented activities.

I kindly request your guidance and support in planning a suitable
learning path for my selected career domain.

I hereby submit my preference for your consideration and further guidance.

Thank you.

Yours faithfully,

«Student_Name»
Student ID: «Student_ID»
Course: «Course»
Year/Semester: «Year_Semester»
```

---

# 7. Start Mail Merge

In Microsoft Word:

**Step 1:** Open the **Mailings** tab.

**Step 2:** Select:

**Start Mail Merge → Letters**

This tells Word that the output will be individual letters.

---

# 8. Connect the Excel dataset

Go to:

**Mailings → Select Recipients → Use an Existing List**

Select:

`Student_Career_Domain_Mail_Merge_Dataset.xlsx`

When Word asks you to select a worksheet, choose:

**Student Data**

Make sure the option indicating that the **first row contains column headers** is enabled.

Click **OK**.

Word is now connected to the Excel dataset.

---

# 9. Insert Mail Merge fields

Place the cursor where the student's name should appear.

Select:

**Mailings → Insert Merge Field**

Select:

`Student_Name`

Word will insert:

`«Student_Name»`

Repeat this for the other fields.

### Field mapping

| Letter Information | Mail Merge Field |
|---|---|
| Student Name | `«Student_Name»` |
| Student ID | `«Student_ID»` |
| Course | `«Course»` |
| Year/Semester | `«Year_Semester»` |
| Student Email | `«Student_Email»` |
| Faculty Name | `«Faculty_Name»` |
| Designation | `«Designation»` |
| Department | `«Department»` |
| Institution | `«Institution_Name»` |
| Date | `«Date»` |
| Primary Domain | `«Domain»` |
| Secondary Domain | `«Secondary_Domain»` |
| Skill Level | `«Skill_Level»` |
| Preferred Technology | `«Preferred_Technology»` |

**Important:** Do not manually type the `« »` merge fields. Insert them using **Insert Merge Field**.

---

# 10. Preview the letters

Go to:

**Mailings → Preview Results**

Use:

**Previous Record ←** and **Next Record →**

to move through the students.

Check that:
- Names are correct.
- Student IDs are correct.
- Domains are correct.
- Faculty information is correct.
- Course and semester information are correct.
- No fields are missing.
- Formatting is correct.

---

# 11. Complete the Mail Merge

Once everything is checked:

**Mailings → Finish & Merge**

You will see options such as:

### Edit Individual Documents
Creates a new Word document containing the merged letters.

**Recommended for this practical.**

### Print Documents
Sends the merged letters to the printer.

### Send Email Messages
Can be used to send the letters electronically when valid email addresses are available.

For this exercise select:

**Finish & Merge → Edit Individual Documents → All**

Word will create a new document containing the personalized letters.

---

# 12. Expected output

The dataset contains:

**20 students**

Therefore:

```text
1 Excel Dataset
       +
1 Word Letter Template
       ↓
20 Personalized Letters
```

For example:

### Student 1

**Name:** Rahul Kumar  
**Domain:** Backend Development  
**Technology:** Python

### Student 2

**Name:** Priya Sharma  
**Domain:** Frontend Development  
**Technology:** JavaScript

### Student 3

**Name:** Arjun Reddy  
**Domain:** DevOps  
**Technology:** Linux

The letter structure remains the same, while student-specific information changes automatically.

---

# 13. Recommended file structure

Keep the files together:

```text
Student_Career_Mail_Merge/
│
├── Student_Career_Domain_Mail_Merge_Dataset.xlsx
├── Student_Career_Domain_Mail_Merge_Letter.docx
└── Merged_Student_Letters.docx
```

Where:

- `.xlsx` = Mail Merge data source
- `Letter.docx` = Main Mail Merge template
- `Merged_Student_Letters.docx` = Final generated letters

---

# 14. Complete Mail Merge workflow

```text
Create Excel Dataset
        ↓
Enter 20 Student Records
        ↓
Save Excel File
        ↓
Create Letter in Word
        ↓
Mailings
        ↓
Start Mail Merge
        ↓
Letters
        ↓
Select Recipients
        ↓
Use Existing List
        ↓
Select Excel File
        ↓
Insert Merge Fields
        ↓
Preview Results
        ↓
Check All Records
        ↓
Finish & Merge
        ↓
Edit Individual Documents
        ↓
20 Personalized Student Letters
```

---

# 15. Practical objective

### Objective

To create personalized student letters using **Microsoft Word Mail Merge** by combining a common letter template with a student career-domain preference dataset maintained in Microsoft Excel.

### Skills demonstrated

- Creating structured data in Excel
- Creating a form letter in Word
- Connecting Excel with Word
- Inserting Mail Merge fields
- Previewing merged records
- Generating multiple personalized documents
- Managing a Mail Merge dataset

### Final result

A single Word letter template is used to automatically generate **20 individualized letters**, with each letter containing the correct student's personal information, software career preference, skill level, and preferred technology.
