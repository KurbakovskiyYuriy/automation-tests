# Task 3: BDD Test Framework

## Setup & Execution

### Installation
Navigate to `Task_3_BDD_Framework/` and install dependencies:
```sh
pip install -r requirements.txt
```

### Run the tests
```sh
behave
```

### **login.feature** (BDD Test Scenario)
```gherkin
Feature: Login functionality

  Scenario: Successful login
    Given the user is on the login page
    When they enter valid credentials
    Then they should see a welcome message
```

### **login_steps.py** (Step Definitions)
```python
from selenium import webdriver
from selenium.webdriver.common.by import By
import time
from behave import given, when, then

@given("the user is on the login page")
def step_open_login_page(context):
    context.driver = webdriver.Chrome()
    context.driver.get("https://example.com/login")

@when("they enter valid credentials")
def step_enter_credentials(context):
    context.driver.find_element(By.NAME, "username").send_keys("testuser")
    context.driver.find_element(By.NAME, "password").send_keys("password123")
    context.driver.find_element(By.NAME, "login").click()
    time.sleep(2)

@then("they should see a welcome message")
def step_verify_welcome(context):
    welcome_message = context.driver.find_element(By.ID, "welcome")
    assert "Welcome" in welcome_message.text
    context.driver.quit()
