# automation-tests
Answers to the test task for Lumen Spei

# Automation Testing Repository

This repository contains three automated testing tasks:

1. **Web Automation Testing** (Selenium & Python)
2. **API Testing** (Postman)
3. **BDD Test Framework** (Behave & Python)

Each task is located in its own directory with specific instructions for setup and execution.

## Repository Structure
```
automation-tests/
├── Task_1_WebAutomation/     # Web automation testing (Selenium)
│   ├── tests/
│   │   ├── test_login.py     # Test script
│   ├── requirements.txt      # Dependencies
│   ├── README.md             # Setup instructions
├── Task_2_API_Testing/       # API testing (Postman)
│   ├── postman_collection.json # Postman collection
│   ├── README.md             # Setup instructions
├── Task_3_BDD_Framework/     # BDD test framework (Behave)
│   ├── features/
│   │   ├── login.feature     # BDD scenario file
│   ├── steps/
│   │   ├── login_steps.py    # Step definitions
│   ├── environment.py        # Behave configuration
│   ├── requirements.txt      # Dependencies
│   ├── README.md             # Setup instructions
├── README.md                 # Main documentation
```

---

## **Automated vs. Manual Testing**

### **Advantages of Automation Testing:**
- Faster execution of repetitive tests.
- More reliable regression testing.
- Can be integrated into CI/CD pipelines.
- Reduces human errors.

### **Disadvantages of Automation Testing:**
- Higher initial setup cost.
- Requires maintenance as applications evolve.
- Not suitable for exploratory or UI-intensive testing.

## **Refactor or adapt an existing test framework**
### **I have created a utility that:**
- Takes HTML code as input.
- Analyzes errors in the structure (unclosed tags, duplicate IDs).
- Corrects the found errors.
- Outputs the corrected code with highlighting of changes
---

This repository provides a structured approach to automated testing, making it easy to run and maintain tests. 🚀
