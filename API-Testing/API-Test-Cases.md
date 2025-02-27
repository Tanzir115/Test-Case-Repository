# API Test Cases Documentation

## Table of Contents
1. [Test Case 1: Verify API Endpoint Availability](#test-case-1-verify-api-endpoint-availability)
2. [Test Case 2: Verify Valid Response Format](#test-case-2-verify-valid-response-format)
3. [Test Case 3: Verify API Response Time](#test-case-3-verify-api-response-time)
4. [Test Case 4: Verify API Response for Valid Data](#test-case-4-verify-api-response-for-valid-data)
5. [Test Case 5: Verify API Response for Invalid Data](#test-case-5-verify-api-response-for-invalid-data)
6. [Test Case 6: Verify API Response for Missing Mandatory Parameters](#test-case-6-verify-api-response-for-missing-mandatory-parameters)
7. [Test Case 7: Verify API Authentication](#test-case-7-verify-api-authentication)
8. [Test Case 8: Verify API Rate Limiting](#test-case-8-verify-api-rate-limiting)
9. [Test Case 9: Verify API Data Update (PUT/PATCH)](#test-case-9-verify-api-data-update-putpatch)
10. [Test Case 10: Verify API Data Deletion (DELETE)](#test-case-10-verify-api-data-deletion-delete)

---

## Test Case 1: Verify API Endpoint Availability

- **Test Case ID**: TC_API_001
- **Objective**: Ensure the API endpoint is accessible.
- **Pre-condition**: The API server is running.
- **Test Steps**:
  1. Send a GET request to the API endpoint (e.g., `https://api.example.com/users`).
- **Expected Result**: The API responds with HTTP status code 200 OK.
- **Pass/Fail Criteria**: The response status should be 200.

---

## Test Case 2: Verify Valid Response Format

- **Test Case ID**: TC_API_002
- **Objective**: Ensure the API returns the correct data format (e.g., JSON, XML).
- **Pre-condition**: The API endpoint is available.
- **Test Steps**:
  1. Send a GET request to the API endpoint.
  2. Check the Content-Type header in the response.
- **Expected Result**: The Content-Type header should be `application/json`.
- **Pass/Fail Criteria**: The response format should be JSON.

---

## Test Case 3: Verify API Response Time

- **Test Case ID**: TC_API_003
- **Objective**: Ensure the API response time is within acceptable limits.
- **Pre-condition**: The API endpoint is available.
- **Test Steps**:
  1. Send a GET request to the API endpoint.
  2. Measure the response time.
- **Expected Result**: The response time should be less than 2 seconds.
- **Pass/Fail Criteria**: The response time should be under 2 seconds.

---

## Test Case 4: Verify API Response for Valid Data

- **Test Case ID**: TC_API_004
- **Objective**: Ensure the API responds with valid data for correct input.
- **Pre-condition**: The API endpoint is available.
- **Test Steps**:
  1. Send a GET request with valid query parameters (e.g., `https://api.example.com/users?id=1`).
- **Expected Result**: The API responds with valid data for the requested user (e.g., user ID 1).
- **Pass/Fail Criteria**: The response data should match the expected user details.

---

## Test Case 5: Verify API Response for Invalid Data

- **Test Case ID**: TC_API_005
- **Objective**: Ensure the API handles invalid input gracefully.
- **Pre-condition**: The API endpoint is available.
- **Test Steps**:
  1. Send a GET request with invalid query parameters (e.g., `https://api.example.com/users?id=invalid`).
- **Expected Result**: The API responds with an error (e.g., 400 Bad Request).
- **Pass/Fail Criteria**: The response status code should be 400 or appropriate error code.

---

## Test Case 6: Verify API Response for Missing Mandatory Parameters

- **Test Case ID**: TC_API_006
- **Objective**: Ensure the API returns an error when required parameters are missing.
- **Pre-condition**: The API endpoint is available.
- **Test Steps**:
  1. Send a GET request without a mandatory parameter (e.g., `https://api.example.com/users` without `id`).
- **Expected Result**: The API responds with a 400 error, indicating a missing parameter.
- **Pass/Fail Criteria**: The response status code should be 400.

---

## Test Case 7: Verify API Authentication

- **Test Case ID**: TC_API_007
- **Objective**: Ensure the API requires and handles authentication correctly.
- **Pre-condition**: The API supports authentication (e.g., via API key, OAuth).
- **Test Steps**:
  1. Send a GET request to the API endpoint without authentication.
  2. Send a GET request with valid authentication (e.g., API key).
- **Expected Result**: The API should reject the unauthenticated request (e.g., 401 Unauthorized).
- **Pass/Fail Criteria**: Unauthorized request should return a 401 status, and authenticated request should return valid data.

---

## Test Case 8: Verify API Rate Limiting

- **Test Case ID**: TC_API_008
- **Objective**: Ensure the API has proper rate limiting.
- **Pre-condition**: The API has rate-limiting rules.
- **Test Steps**:
  1. Send multiple requests (e.g., 100 requests) in a short period of time.
- **Expected Result**: The API should return a 429 Too Many Requests error after the rate limit is exceeded.
- **Pass/Fail Criteria**: After exceeding the rate limit, the response should return a 429 status.

---

## Test Case 9: Verify API Data Update (PUT/PATCH)

- **Test Case ID**: TC_API_009
- **Objective**: Ensure the API correctly updates data when using PUT or PATCH.
- **Pre-condition**: The API allows data update.
- **Test Steps**:
  1. Send a PUT or PATCH request with valid data to update a resource (e.g., `https://api.example.com/users/1`).
  2. Check the updated resource by sending a GET request.
- **Expected Result**: The data should be updated correctly in the response.
- **Pass/Fail Criteria**: The updated resource data should reflect the changes.

---

## Test Case 10: Verify API Data Deletion (DELETE)

- **Test Case ID**: TC_API_010
- **Objective**: Ensure the API correctly deletes data when using DELETE.
- **Pre-condition**: The API supports data deletion.
- **Test Steps**:
  1. Send a DELETE request to remove a resource (e.g., `https://api.example.com/users/1`).
  2. Send a GET request to confirm the resource is deleted.
- **Expected Result**: The resource should no longer exist (404 Not Found).
- **Pass/Fail Criteria**: The resource should be deleted successfully.

---

## Notes

- Add any additional notes or remarks about testing here (e.g., environments used, limitations, etc.).
