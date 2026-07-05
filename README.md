# Scholarship-eligibility-workflow
# 🎓 Scholarship Eligibility Workflow

An automated scholarship eligibility workflow built using **n8n**. This workflow receives student application data through a form, checks the eligibility based on the student's percentage, and automatically sends the appropriate email using Gmail.

---

## 📌 Overview

This workflow automates the scholarship screening process.

When a student submits an application form, the workflow extracts the required information, evaluates the student's percentage, and sends either a **Congratulations** email or a **Regret** email based on the eligibility criteria.

This project demonstrates how conditional logic and email automation can simplify repetitive administrative tasks.

---

# 📖 Workflow Architecture
![image alt](https://github.com/n8n-workflows-projects/Scholarship-eligibility-workflow/blob/4e147d82322bf2199f97074115990edb507ff57a/Screenshot%202026-07-05%20151510.png)

---

## 🔄 Workflow Flow

```text
Student Form Submission
          │
          ▼
  On Form Submission
          │
          ▼
     Edit Fields
          │
          ▼
        IF Node
      /          \
 Eligible      Not Eligible
     │              │
     ▼              ▼
Congratulations   Regret
 Email            Email
```

---

# ⚙️ Workflow Components

| Node | Purpose |
|------|----------|
| **On Form Submission** | Starts the workflow whenever a student submits the application form. |
| **Edit Fields** | Extracts and formats only the required fields from the submitted form. |
| **IF Node** | Checks whether the student's percentage is greater than or equal to the eligibility criteria. |
| **Gmail (Eligible)** | Sends a congratulatory email to eligible students. |
| **Gmail (Not Eligible)** | Sends a regret email to students who do not meet the eligibility criteria. |

---

# 🧠 How It Works

## Step 1

The student fills out the scholarship application form.

Example Input

```
Name: John Doe

Email: john@example.com

Phone Number: +91XXXXXXXXXX

Percentage: 92%
```

---

## Step 2

The **On Form Submission** trigger activates automatically after the form is submitted.

---

## Step 3

The **Edit Fields** node extracts only the required information.

Example

- Full Name
- Email Address
- Phone Number
- Percentage

---

## Step 4

The **IF Node** evaluates the student's percentage.

Condition

```
Percentage >= 90
```

### If TRUE

Student is eligible for the scholarship.

↓

A Congratulations email is sent.

---

### If FALSE

Student is not eligible.

↓

A Regret email is sent.

---

## Step 5

The student immediately receives an automated email based on the evaluation.

---

# 🖼 Workflow Screenshot

![image alt](https://github.com/n8n-workflows-projects/Scholarship-eligibility-workflow/blob/1794d9339476f5dcdc28a37b7d5d7632e4b0bf87/Screenshot%202026-07-05%20150434.png)

![image alt](https://github.com/n8n-workflows-projects/Scholarship-eligibility-workflow/blob/64b03a97086dd644782dd32e5ec0d7bf69f3651f/Screenshot%202026-07-05%20151713.png)

---

# 📧 Sample Emails

## ✅ Eligible Student

**Subject**

```
🎉 Congratulations! Scholarship Application Approved
```

**Email**

```
Hello {{Name}},

Congratulations!

We are pleased to inform you that you have successfully met the scholarship eligibility criteria.

Our team will contact you soon with the next steps.

Best Wishes,
Scholarship Committee
```

---

## ❌ Not Eligible Student

**Subject**

```
Scholarship Application Update
```

**Email**

```
Hello {{Name}},

Thank you for applying for our scholarship program.

After reviewing your application, we regret to inform you that you do not meet the minimum eligibility criteria.

We encourage you to apply again in the future.

We wish you all the best.

Regards,
Scholarship Committee
```

---

# 📋 Eligibility Criteria

| Requirement | Value |
|-------------|-------|
| Minimum Percentage | **90%** |
| Eligible Condition | Percentage ≥ 90 |
| Not Eligible | Percentage < 90 |

---

# 🚀 Features

- Automated scholarship screening
- Form submission trigger
- Conditional logic using IF node
- Automatic Gmail integration
- Instant email notifications
- Beginner-friendly workflow
- Easy to customize eligibility criteria

---

# 📂 Workflow Structure

```text
On Form Submission
        │
        ▼
   Edit Fields
        │
        ▼
      IF Node
     /       \
 TRUE       FALSE
  │            │
  ▼            ▼
Gmail      Gmail
Eligible   Not Eligible
```

---

# 🛠 Technologies Used

- n8n
- Gmail Node
- Forms Trigger
- IF Node
- Set (Edit Fields) Node

---

# 💡 Use Cases

- Scholarship Management
- College Admissions
- Internship Screening
- Training Program Eligibility
- Contest Registration
- Employee Eligibility Verification

---

# 🔮 Future Enhancements

This workflow can be enhanced by adding:

- 🗄 Google Sheets database
- 📊 Airtable integration
- 📄 PDF certificate generation
- 🤖 AI-powered application review
- 📱 WhatsApp notifications
- 📧 Admin notification emails
- 📈 Dashboard for application tracking
- ☁️ Cloud database integration

Future Workflow

```text
Student Form
      │
      ▼
Form Trigger
      │
      ▼
AI Validation
      │
      ▼
Database
      │
      ▼
Eligibility Check
      │
      ▼
Email + WhatsApp + Dashboard
```

---

# 📚 Learning Objectives

After completing this workflow, you will understand:

- How Form Triggers work in n8n
- Using the Edit Fields (Set) node
- Building conditional logic with IF nodes
- Sending automated emails with Gmail
- Designing decision-based workflows
- Creating beginner automation projects

---

# 📁 Repository Structure

```text
Scholarship-Eligibility-Workflow/
│
├── README.md
├── Scholarship Eligibility Workflow.json
│
└── images/
    ├── workflow.png
    ├── architecture.png
    └── email-preview.png
```

---

# 📄 License

This project is created for educational and learning purposes.

Feel free to modify and extend it for your own automation projects.

---

# ⭐ Support

If this workflow helped you learn n8n automation:

⭐ Star this repository

🍴 Fork the project

📢 Share it with others learning workflow automation

Happy Automating! 🚀
