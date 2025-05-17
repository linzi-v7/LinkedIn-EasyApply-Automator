# LinkedIn Easy Apply Automator 🤖

Automate your LinkedIn job applications via email with the power of AI.

## 📌 Overview

This tool streamlines the LinkedIn **Easy Apply** process using email and automation. Users can apply to multiple jobs by simply sending an email with a PDF resume. The system searches LinkedIn for relevant jobs and automatically handles the application process.

> ⚠️ **Note**: The bot simulates and validates application steps — it does **not** submit final applications. It ensures that the form could be filled correctly, based on your resume and AI's understanding.

---

## ✉️ How to Use

1. Send an email with:

   * **Subject Format**:
     `[LinkedIn Bot] <Job Title> - <Number of Applications>`
   * **Attachment**:
     Your resume in **PDF** format.
   * **Email Body**:
     Include default answers for radio-button type questions (e.g., "Are you authorized to work?") to help the bot auto-fill certain fields. For formatting instructions, use the help command (see [📚 Getting Help](#-getting-help)).

2. The bot:

   * Parses your email.
   * Searches LinkedIn for Easy Apply jobs matching the job title.
   * Begins the application simulation process.

3. You’ll receive a response email with:

   * A **log Excel file** summarizing which applications succeeded or failed.
   * Job-specific details including company name, job title, timestamp, and application link.

## 🧠 Application Handling Details

* **AI-Powered Input Filling**:
  Uses an AI model to extract relevant details from your resume and apply them to form fields.

* **Radio Button Questions**:
  These are filled using a **data table** built from your email body, containing common questions and your default answers.

* **Failure Handling**:

  * If required data is missing (e.g. `DATA_NOT_IN_CV`), the application is **marked as Failed**.
  * If a required UI element is missing, the bot tries to fill what it can — if the form cannot be completed, it is **marked as Failed**.
  * The bot continues applying to the remaining jobs regardless of failures, according to the specified no. of applications.

---

## 📊 Logging and Feedback

Each application is logged into an Excel sheet with the following info:

* Timestamp
* Job Title
* Company
* Application Link
* Application Status: `Success`, `Failed`

This sheet is sent back to the user after all applications are processed.

## 📚 Getting Help

To receive usage instructions and question templates for the email body:

* Send an email with the subject:
  `[LinkedIn Bot] Bot Help`

You will receive a response with formatting guidelines and examples to improve your success rate.

## 🧪 Known Limitations

* Final job applications are **not submitted**; the system ensures only that the form **can** be completed.
* Success rate depends on:

  * Resume quality.
  * AI model performance.
  * Question complexity.
  * Form Complexity (Handled UI Elements, etc..).
* Works only with **Easy Apply** jobs (non-Easy Apply ones are ignored).

## 💡 Example Email

**Subject**:
`[LinkedIn Bot] Backend Developer - 15`

**Attachment**:
`John_Doe_CV.pdf`

**Body**:

```
Yes
NULL
No
etc...
```

---

## 🔒 Privacy Notice

Your resume and job preferences are used only for filling job applications.

## 🚀 Future Plans

* Support for cover letters.
* UI for manual review before submission.
* Multiple resume selection per role type.
* Better handling of complex/obscure form elements.
* Improved error handling and user communication.

---

## 🎓 Academic Info

This project was developed as part of the **Software Requirements Engineering** course in **Ain Shams University**.

## 📄 License

This project is licensed under the **MIT License**, meaning you are free to use, modify, and distribute it with attribution. Read the full terms [here](https://github.com/linzi-v7/LinkedIn-EasyApply-Automator/blob/main/LICENSE).  

## Contact  

Have feedback or want to collaborate? Feel free to connect:  

* **GitHub** – [linzi-v7](https://github.com/linzi-v7)  
* **LinkedIn** – [Faris Osama](https://www.linkedin.com/in/faris-osama-7a3496303/)  

---

### 📌 Project Status: **Completed** 🚀 (Future improvements planned)