# Postman Test Cases Documentation

## Table of Contents
1. [GET User Details](#get-user-details)
2. [POST Create New User](#post-create-new-user)
3. [PUT Update User Information](#put-update-user-information)
4. [DELETE Delete User](#delete-delete-user)
5. [Bug Report Format](#bug-report-format)
6. [Contribution](#contribution)
7. [Contact](#contact)

---

## **1. GET User Details**
```
Test Case ID: TC_POSTMAN_001 Title: Verify GET request to retrieve user details Description: Ensure that the GET request to retrieve user details returns the correct user data. Preconditions: User must exist in the system. Postman Request:

Method: GET
URL: https://api.example.com/users/{userId}
Authorization: Bearer token
Headers:
Content-Type: application/json
Authorization: Bearer {access_token} Steps to Execute:
Open Postman and select the GET method.
Enter the URL with a valid userId in the URL field.
Click on Send.
Check the response for correct user details. Expected Result: The response should return the user details with the correct userId. Status: Pass/Fail
```
---

## **2. POST Create New User**
```
Test Case ID: TC_POSTMAN_002 Title: Verify POST request to create a new user Description: Ensure that the POST request to create a new user functions as expected. Preconditions: User data should be valid and meet the API requirements. Postman Request:

Method: POST
URL: https://api.example.com/users
Authorization: Bearer token
Headers:
Content-Type: application/json
Authorization: Bearer {access_token}
Body:
{
   "username": "new_user",
   "email": "new_user@example.com",
   "password": "password123"
}
Steps to Execute:

Open Postman and select the POST method.
Enter the URL and provide the body with valid user data.
Click on Send.
Verify that the response status code is 201 (Created).
Check that the response contains the created user data. Expected Result: The user should be created successfully, and the response should return the created user’s details. Status: Pass/Fail
```
---

## **3. PUT Update User Information**
```
Test Case ID: TC_POSTMAN_003 Title: Verify PUT request to update user information Description: Ensure that the PUT request to update user details functions as expected. Preconditions: A user must already exist in the system. Postman Request:

Method: PUT
URL: https://api.example.com/users/{userId}
Authorization: Bearer token
Headers:
Content-Type: application/json
Authorization: Bearer {access_token}
Body:
{
   "email": "updated_user@example.com"
}
Steps to Execute:

Open Postman and select the PUT method.
Enter the URL with a valid userId.
Provide the body with the updated user information.
Click on Send.
Verify that the response status code is 200 (OK).
Check the response for the updated user information. Expected Result: The user’s information should be updated successfully. Status: Pass/Fail
```
---

## **4. DELETE Delete User**
```
Test Case ID: TC_POSTMAN_004 Title: Verify DELETE request to remove a user Description: Ensure that the DELETE request successfully removes a user from the system. Preconditions: A user must exist in the system. Postman Request:

Method: DELETE
URL: https://api.example.com/users/{userId}
Authorization: Bearer token
Headers:
Content-Type: application/json
Authorization: Bearer {access_token} Steps to Execute:
Open Postman and select the DELETE method.
Enter the URL with a valid userId.
Click on Send.
Verify that the response status code is 204 (No Content).
Verify that the user is deleted by sending a GET request for the same userId. Expected Result: The user should be deleted, and the GET request should return a 404 (Not Found) for the deleted user. Status: Pass/Fail
```
---

## **Bug Report Format**
```
Bug ID: BUG_POSTMAN_001 Title: POST request to create new user returns 400 Bad Request Severity: High Steps to Reproduce:

Open Postman and select the POST method.
Enter the URL and provide the body with invalid data (e.g., missing required fields).
Click on Send. Expected Result: The server should return a 400 Bad Request error with a message indicating what is wrong. Actual Result: The server returns a 500 Internal Server Error. Attachments: (Screenshots, Postman console logs, API error logs)
```
---

## **Contribution**

If you want to add more test cases, please follow the existing format and create a pull request.

## **Contact**

For any queries, reach out to **Tanzirul Islam** via [LinkedIn](https://LinkedIn.com/in/tanzirulshafin).

---
