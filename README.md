# IT23208476 - Pixelssuite Functional & Usability Testing

## 📌 Assignment Details

* **Module:** IT3040 – IT Project Management (ITPM)
* **Assignment:** Assignment 1 – Option 2
* **Student ID:** IT23208476
* **Objective:**
  This project evaluates the **functional correctness and usability** of the Pixelssuite website by testing its key features under both valid and invalid conditions.

---

## 🌐 Website Under Test

🔗 https://www.pixelssuite.com/

---

## 🎯 Features Tested

The following features of the application were tested:

1. Document Conversion
2. PDF Editing
3. Image Resizing
4. Cropping
5. Compression
6. Image Format Conversion
7. Meme Generation
8. Color Picker
9. Image Rotation
10. Image Flipping

---

## 🧪 Test Case Design

* A total of **36 test cases** were created
* Each feature includes:

  * ✅ 1 Positive test case
  * ❌ 2 Negative test cases

### ✔ Test Coverage Includes:

* Valid inputs
* Invalid file types
* Missing inputs
* Edge cases
* User interaction behavior

---

## 🤖 Test Automation

### 🔹 Automated Scenario

One test case was automated using **Playwright** to verify:

✔ Image upload
✔ Preview functionality
✔ System response validation

---

## ⚙️ Technologies Used

* **Python 3**
* **Playwright**
* **OpenPyXL**
* **CSV for result recording**

---

## 📁 Project Structure

```
test_automation_ui/
│
├── image_preview_test.py        # Automation script
├── execution_results.csv        # Test execution results
├── sample.png                   # Sample input image
├── results/
│   └── preview_pass.png         # Screenshot of successful test
```

---

## 🚀 How to Run the Automation

### 🔹 Step 1: Install Requirements

```bash
python -m pip install playwright openpyxl
python -m playwright install
```

---

### 🔹 Step 2: Navigate to Project Folder

```bash
cd /d D:\test_automation_ui
```

---

### 🔹 Step 3: Run the Test

```bash
python image_preview_test.py --url "https://www.pixelssuite.com/convert-to-png" --slow-mo-ms 2000
```

---

## 📊 Execution Results

* **Preview Detected:** TRUE
* **Status:** PASS
* **Output File:** execution_results.csv
* **Screenshot:** results/preview_pass.png

---

## 📷 Evidence

The automation script captures a screenshot when the preview is successfully displayed.

✔ Screenshot file:
`results/preview_pass.png`

---

## 📌 Assumptions

* The system should display a preview after uploading a valid PNG image
* Supported formats include PNG, JPG, and WEBP
* The preview section must accurately reflect the uploaded image

---

## ⚠️ Limitations

* Backend API testing is not included
* Performance and security testing are out of scope
* Automation focuses only on preview functionality

---

## ✅ Conclusion

The testing process confirmed that:

* Core features of the Pixelssuite application function correctly
* The preview functionality operates as expected
* Minor usability improvements can be considered for better user feedback

---

## 🔗 Repository Link

(Add your GitHub repository link here)

---

## 📦 Submission Includes

* ✔ Manual Test Cases (Excel File)
* ✔ Automation Script (Playwright Project)
* ✔ execution_results.csv
* ✔ GitHub Repository

---

## 👨‍💻 Author

**IT23208476**
