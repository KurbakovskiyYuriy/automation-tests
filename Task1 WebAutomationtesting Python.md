# Task 1: Web Automation Testing

## Setup & Execution

### Installation
Navigate to `Task_1_WebAutomation/` and install dependencies:
```sh
pip install -r requirements.txt
```

### Run the test
```sh
python tests/test_login.py
```

### **test_login.py** (Selenium Web Automation Test)
```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
import time

# WebDriver setup
driver = webdriver.Chrome()

driver.get("https://example.com/login")

# Enter login details
username = driver.find_element(By.NAME, "username")
password = driver.find_element(By.NAME, "password")
login_button = driver.find_element(By.NAME, "login")

username.send_keys("testuser")
password.send_keys("password123")
login_button.click()

time.sleep(2)

# Verify login success
welcome_message = driver.find_element(By.ID, "welcome")
assert "Welcome" in welcome_message.text

driver.quit()
