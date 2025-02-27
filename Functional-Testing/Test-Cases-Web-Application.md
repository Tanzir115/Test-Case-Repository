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
### **4. Logout Functionality**
```
Test Case ID: TC_FT_004  
Title: Verify logout functionality  
Description: Ensure that users can log out successfully.  
Preconditions: User must be logged into the application.  
Steps to Execute:  
1. Navigate to the dashboard.  
2. Click on the logout button.  
Expected Result: User should be logged out and redirected to the login page.  
Status: Pass/Fail  
```
### **5. User Registration Functionality**
```
Test Case ID: TC_FT_005  
Title: Verify user registration functionality  
Description: Ensure that new users can create an account with valid details.  
Preconditions: User should not have an existing account.  
Steps to Execute:  
1. Navigate to the registration page.  
2. Enter valid user details (username, email, password, etc.).  
3. Click on the Register button.  
Expected Result: User should receive a confirmation email and be able to log in after verification.  
Status: Pass/Fail  
```
### **6. Registration with Existing Email**
```
Test Case ID: TC_FT_006  
Title: Verify registration with an already registered email  
Description: Ensure that users cannot register with an email that is already in use.  
Preconditions: The email address must be linked to an existing account.  
Steps to Execute:  
1. Navigate to the registration page.  
2. Enter an already registered email and other details.  
3. Click on the Register button.  
Expected Result: User should receive an error message "Email already exists."  
Status: Pass/Fail  
```
### **7. Search Functionality**
```
Test Case ID: TC_FT_007  
Title: Verify search functionality  
Description: Ensure that users can search for items using keywords.  
Preconditions: The system must have items available for search.  
Steps to Execute:  
1. Navigate to the search bar.  
2. Enter a valid keyword.  
3. Click the Search button.  
Expected Result: Relevant search results should be displayed.  
Status: Pass/Fail  
```
### **8. Add to Cart Functionality**
```
Test Case ID: TC_FT_008  
Title: Verify add to cart functionality  
Description: Ensure that users can add items to the shopping cart.  
Preconditions: User must be logged in, and items must be available.  
Steps to Execute:  
1. Navigate to the product page.  
2. Click on the "Add to Cart" button.  
3. Open the cart to check the added item.  
Expected Result: Item should be added to the cart successfully.  
Status: Pass/Fail  
```
### **9. Checkout Process**
```
Test Case ID: TC_FT_009  
Title: Verify checkout process  
Description: Ensure that users can complete a purchase successfully.  
Preconditions: User must have items in the cart and be logged in.  
Steps to Execute:  
1. Navigate to the cart page.  
2. Click on the checkout button.  
3. Enter valid payment details and complete the purchase.  
Expected Result: User should receive an order confirmation message.  
Status: Pass/Fail  
```
### **10. Profile Update Functionality**
```
Test Case ID: TC_FT_010  
Title: Verify profile update functionality  
Description: Ensure that users can update their profile information.  
Preconditions: User must be logged into their account.  
Steps to Execute:  
1. Navigate to the profile settings page.  
2. Update the required fields (name, email, password, etc.).  
3. Click on the Save button.  
Expected Result: Profile details should be updated successfully.  
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

