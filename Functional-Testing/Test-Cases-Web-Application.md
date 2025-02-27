## Functional Test Cases

### **1. Login Functionality**
```
Test Case ID: TC_FT_001
Title: Verify login functionality with valid credentials
Description: Ensure that users can log in using valid username and password.
Preconditions: User must have a registered account.
Steps to Execute:
1. Navigate to the login page.
2. Enter valid username and password.
3. Click on the Login button.
Expected Result: User should be successfully logged in and redirected to the dashboard.
Status: Pass/Fail
```

### **2. Login with Invalid Credentials**
```
Test Case ID: TC_FT_002
Title: Verify login functionality with invalid credentials
Description: Ensure that users cannot log in with incorrect username or password.
Preconditions: User must have a registered account.
Steps to Execute:
1. Navigate to the login page.
2. Enter an incorrect username or password.
3. Click on the Login button.
Expected Result: User should see an error message "Invalid username or password."
Status: Pass/Fail
```

### **3. Password Reset Functionality**
```
Test Case ID: TC_FT_003
Title: Verify password reset functionality
Description: Ensure that users can reset their password using a registered email.
Preconditions: User must have access to their registered email.
Steps to Execute:
1. Navigate to the login page.
2. Click on "Forgot Password?" link.
3. Enter the registered email address.
4. Click on the submit button.
5. Check the email inbox for a password reset link.
6. Follow the link and reset the password.
Expected Result: User should receive an email with a password reset link and be able to set a new password.
Status: Pass/Fail
```

## Bug Report Format
```
Bug ID: BUG_001
Title: Login button not working on mobile version
Severity: Critical
Steps to Reproduce:
1. Open the application on a mobile browser.
2. Enter valid credentials and click the login button.
3. Observe that nothing happens.
Expected Result: User should be logged in successfully.
Actual Result: Login button does not respond.
Attachments: (Screenshots, logs, or videos)
```

## Contribution
If you want to add more test cases, please follow the existing format and create a pull request.

## Contact
For any queries, reach out to **Tanzirul Islam** via [LinkedIn](https://LinkedIn.com/in/tanzirulshafin).

