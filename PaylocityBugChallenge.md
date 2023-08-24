
# Paylocity STE Assessment- Bug Challenge :bug: 🔍 


<details>

<summary>Bug 01- Error Occured processing request</summary>

## Description
Upon attempting to process a user's request, an error occurs with the following details:

Error Message: An error occurred while processing your request.
Request ID: 0HMT379708TF5

The error message suggests that there was a problem during the request processing. It includes a unique Request ID for tracking purposes.

Additionally, the message provides an option to enable "Development Mode" for more detailed error information. However, a caution is given against using this mode in deployed applications due to potential exposure of sensitive information to end users.

## Steps To Reproduce

1.Go to the URL: https://wmxrwq14uc.execute-api.us-east-1.amazonaws.com/Prod/Account/Login

2.Enter invalid characters in the `Username` and `Password` fields

3.Click on the `Login` button


## Actual behavior
Error Message: An error occurred while processing your request is shown to the user. Alogn with Request ID: 0HMT379708TF5 is also displayed, all errors after the user clicks on the Login button

## Expected behavior
A clear and concise description of what you expected to happen.

## Priority
High

## Screenshots/Video
<img width="1339" alt="Screen Shot 2023-08-22 at 9 39 15" src="https://github.com/erodm09/PaylocityTask/assets/102558006/b6b637e7-87b0-468b-b39b-21cc17753140">


## Device Details:
Device: MacBook Pro (13-inch, M2, 2022) Chip M2
OS: MacOs
Version: Mac OS Monterrey Version 12.4
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

Additional context
Add any other context about the problem here

</details> 

<details>

<summary>Bug 02- Error Handling not clearing after User goes back</summary>


## Description
After a user inputs an incorrect or missing password during the login process and then inputs incorrect password or username, and proceeds after the error displayed, to rectify it by refreshing the page, the initial error message persists about the missing Username or Password. The error message indicates that an incorrect password was provided.

## Steps To Reproduce

1.Navigate to the login page.

2.Input an incorrect `password` or leave the `password` field blank.

3.Click the `login` button.

4.Observe the displayed error message described in `Bug-01`.

5.Click on the Back button on the Brwoser

6.Refresh the page using the browser's refresh button or shortcut (e.g., F5 or Ctrl + R).

7.Observe that the initial error message remains unchanged.


## Actual behavior
Error Message: An error occurred while processing your request is shown to the user. Alogn with Request ID: 0HMT379708TF5 is also displayed, all errors after the user clicks on the Login button

## Expected behavior
Even after refreshing the page, the initial error message indicating an incorrect or missing password continues to be displayed, which could cause user confusion and potentially impact the user experience.

## Priority
Medium

## Screenshots/Video


https://github.com/erodm09/PaylocityTask/assets/102558006/71ab68e4-26da-44d3-945b-a135be60b309



## Device Details:

OS: MacOs
Version: Mac OS Monterrey Version 12.4
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<details>

<summary>Bug 03- Paylocity Benefits Dashboard link available and shown to user after clicking</summary>


## Description
After a user inputs an incorrect or missing password during the login process and then inputs incorrect password or username, and proceeds after the error displayed, to rectify it by refreshing the page, the initial error message persists about the missing Username or Password. The error message indicates that an incorrect password was provided.

## Steps To Reproduce

1. Go to the following Login website link
2.On the upper left corner click on the Paylocity Benefits Dashboard message link.
3. Note that no login credentials are required to access the dashboard.
Observe that the form to add dependents is accessible and can be interacted with.

## Actual behavior
1. The Paylocity Benefits Dashboard is accessible without requiring login credentials.
2.Users can interact with the form to try and add dependents without proper authentication or employee data.

## Expected behavior
1.The Paylocity Benefits Dashboard should require proper login credentials before allowing access.
2.Users should only be able to interact with the form and access data if they are authenticated and authorized users.
3.Unauthorized users should not have access to any functionality of the dashboard.

## Priority
Low

## Screenshots/Video



https://github.com/erodm09/PaylocityTask/assets/102558006/76590c0a-6083-4095-8dbc-10ae96b9acab




## Device Details:

OS: MacOs
Version: Mac OS Monterrey Version 12.4
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<details>

<summary>Bug 04- No Error Message when inputing larger than required characters on First Name</summary>


## Description
When attempting to input larger than required characters in the "First Name" field during the process of adding or editing an employee on the Benefits Dashboard application, no error message is displayed, and the application allows the user to proceed without any indication of the input exceeding the limit.

## Steps To Reproduce

1.Open the Benefits Dashboard application.

2.Navigate to the section where you can add or edit an employee.

3.In the "First Name" field, input a string of characters that is longer than the specified limit (e.g., more than 50 characters).

4.Attempt to proceed by clicking the "Save" or "Submit" button

## Actual behavior
No error message is shown, and the application doesnt let the user know that is inputing a wrong field

## Expected behavior
An error message should be displayed on the UI, indicating that the input for the "First Name" field exceeds the allowed character limit.

## Priority
Low

## Screenshots/Video




https://github.com/erodm09/PaylocityTask/assets/102558006/2bd71e5c-6b43-4fb3-9e81-7fe72576a863




## Device Details:

OS: MacOs
Version: Mac OS Monterrey Version 12.4
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<details>

<summary>Bug 05-Duplicate Employee Addition with Same Details is allowed</summary>


## Description

The current version of the application permits the addition of an employee with the exact same First Name, Last Name, and Dependents as an existing entry. This oversight leads to the creation of duplicate employee records within the system, causing potential data inconsistency and confusion.


## Pre-condition

Have an existing user with valid First Name, Last Name and Dependent.


## Steps To Reproduce

1.Go to link for the application to

2.Enter valid details for Username and password and click on the Login button

2.Click on the `Add Employee` button

3.Input the same First Name, Last Name, and Dependents as an already existing employee.

4.Proceed with adding the employee by clicking on the Save button

## Actual behavior
No error message is shown, and the application doesnt let the user know that he/she is adding a Duplicat or existing user

## Expected behavior
An error message should be displayed on the UI, indicating that the entered user already exists to Try agian.

## Priority
High

## Screenshots/Video


https://github.com/erodm09/PaylocityTask/assets/102558006/394f08af-6fc7-42e9-a5d7-65c27b79dc05



## Device Details:

OS: MacOs
Version: Mac OS Monterrey Version 12.4
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<details>

<summary>Bug 06-API - Error Sending POST Request with Invalid String on dependent field</summary>


## Description

While using Postman to send a POST request to add a New employee, an error is encountered when an invalid string value is provided as the dependent's field. The application should handle and validate input data to prevent the addition of invalid or incorrect values.


## Pre-condition

Have the valid Postman collection imported in Postman


## Steps To Reproduce

1. Launch Postman and access the QA Challenge- Master collection
2. Go to the POST request `Add Employee` for adding a new Employee.
3. On the Depndent field enter an invalid string (e.g., "X") as the dependent's number information.
4. Click on the Send button to send the POST request.

## Actual behavior
Upon sending the POST request, it allows the input of an invalid string as the dependent's field information. After sending an error occurs, but the error message is not descriptive enough to identify the issue.

## Expected behavior
If an invalid string value is provided, the application should display an error message indicating that the input is invalid. 

## Priority
Medium

## Screenshots/Video


<img width="1366" alt="Screen Shot 2023-08-24 at 0 19 36" src="https://github.com/erodm09/PaylocityTask/assets/102558006/7b925d27-3746-4a43-a7de-bcfde3726a42">



## Device Details:
Postman Version: 10.17.3-230823-0523
OS: MacOs 10.15.7
Version: Mac OS Monterrey Version 12.4
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<details>

<summary>Bug 07-API -  Error with Invalid ID in PUT Request Body for Employee Updated</summary>


## Description

When attempting to update an employee's information using a PUT request, an error is encountered due to an invalid ID being provided in the request body. The application should handle and validate input data to ensure that only valid IDs are accepted for updates


## Pre-condition

Have the valid Postman collection imported in Postman


## Steps To Reproduce

1. Launch Postman and access the QA Challenge- Master collection
2. Go to the PUT request `Update Employee` for editing an Employee.
3. On the Request body include an invalid ID value of a user.
4. Click on the Send button to send the PUT request.


## Actual behavior
The application accepts the PUT request with an invalid ID value in the request body.The server responds with an error message that is not specific enough to identify the issue.

## Expected behavior
The application should validate the provided ID to ensure that it is a valid and existing employee ID.If an invalid ID is detected in the request body, the application should return a clear error response indicating that the ID is not valid

## Priority
High

## Screenshots/Video

<img width="1315" alt="Screen Shot 2023-08-24 at 12 46 23" src="https://github.com/erodm09/PaylocityTask/assets/102558006/a4c4275a-0e19-4243-9836-c01d0ae17fd5">



## Device Details:
Postman Version: 10.17.3-230823-0523
OS: MacOs 10.15.7
Version: Mac OS Monterrey Version 12.4
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<details>

<summary>Bug 08-API -  Incorrect Response for DELETE Request with Non-Existing Employee ID</summary>


## Description

When sending a DELETE request to remove an employee from the system, if an employee ID that has already been deleted or does not exist is provided in the request URL, the application responds with a "200 OK" status. This behavior is misleading as it suggests successful deletion, even though the employee does not exist in the first place.

## Pre-condition

Have the valid Postman collection imported in Postman


## Steps To Reproduce

1. Launch Postman and access the QA Challenge- Master collection
2. Go to the DELETE request `Delete Employee` to remove an Employee.
3. On the Request URL include an invalid ID or already deleted employee ID value of a user.
4. Click on the Send button to send the DELTE request.


## Actual behavior
The application accepts the DELETE request with a non-existing or already deleted employee ID. The server responds with a "200 OK" status, which incorrectly suggests successful deletion.

## Expected behavior
The application should validate the provided employee ID to ensure that it exists in the system. If a non-existing or already deleted ID is detected, the application should return a "404 Not Found" status or an appropriate error response indicating that the employee does not exist.

## Priority
High

## Impact:
This issue has the following negative impacts:

Misleading Response: The "200 OK" status implies successful deletion when the employee does not exist, leading to confusion and incorrect assumptions.
Data Integrity: Users might believe they have successfully deleted a nonexistent employee, affecting data integrity and accuracy.
Ineffective Error Handling: The application fails to provide accurate error responses for such cases, making troubleshooting difficult.

## Screenshots/Video
<img width="1273" alt="Screen Shot 2023-08-24 at 13 08 43" src="https://github.com/erodm09/PaylocityTask/assets/102558006/65eae627-a7e2-41f3-b249-ac055f4051bb">

<img width="1342" alt="Screen Shot 2023-08-24 at 13 09 02" src="https://github.com/erodm09/PaylocityTask/assets/102558006/e499b90c-9e7c-47d6-888f-681419484a11">

<img width="1384" alt="Screen Shot 2023-08-24 at 13 10 09" src="https://github.com/erodm09/PaylocityTask/assets/102558006/89c912ef-f652-41fc-bd83-6aad6d2dd517">



## Device Details:
Postman Version: 10.17.3-230823-0523
OS: MacOs 10.15.7
Version: Mac OS Monterrey Version 12.4
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>



<details>

<summary>Bug 09-API -  Incorrect Response for GET Request with Non-Existing Employee ID</summary>


## Description

When sending a GET request to remove an employee from the system, if an employee ID that has already been deleted or does not exist is provided in the request URL, the application responds with a "200 OK" status. This behavior is misleading as it suggests successful, even though the employee does not exist in the first place.

## Pre-condition

Have the valid Postman collection imported in Postman


## Steps To Reproduce

1. Launch Postman and access the QA Challenge- Master collection
2. Go to the GET request `Get Employee` to retreive information of an Employee.
3. On the Request URL input an already non existing or recently deleted employee ID value of a user.
4. Click on the Send button to send the GET request.


## Actual behavior
The application accepts the GET request with a non-existing or already deleted employee ID. The server responds with a "200 OK" status, which incorrectly suggests successful retreivement of Employee details.

## Expected behavior
The application should validate the provided employee ID to ensure that it exists in the system. If a non-existing or already deleted ID is detected, the application should return a "404 Not Found" status or an appropriate error response indicating that the employee does not exist.

## Priority
High

## Impact:
This issue has the following negative impacts:

Misleading Response: The "200 OK" status implies successful deletion when the employee does not exist, leading to confusion and incorrect assumptions.
Data Integrity: Users might believe they have successfully deleted a nonexistent employee, affecting data integrity and accuracy.
Ineffective Error Handling: The application fails to provide accurate error responses for such cases, making troubleshooting difficult.

## Screenshots/Video

<img width="1384" alt="Screen Shot 2023-08-24 at 13 10 09" src="https://github.com/erodm09/PaylocityTask/assets/102558006/3e3101a7-bcc0-4dbe-86a4-210941aeccc2">


## Device Details:
Postman Version: 10.17.3-230823-0523
OS: MacOs 10.15.7
Version: Mac OS Monterrey Version 12.4
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>


<details>

<summary>Bug 10-API -  Error with Invalid ID in GET Request Body for Employee Updated</summary>


## Description

When attempting to retreive an employee's information using a GET request, an error is encountered due to an invalid ID being provided in the request URL. The application should handle and validate input data to ensure that only valid IDs are accepted for updates

## Pre-condition

Have the valid Postman collection imported in Postman


## Steps To Reproduce

1. Launch Postman and access the QA Challenge- Master collection
2. Go to the GET request `GET Employee` to retrieve an Employee's information.
3. On the Request body include an invalid ID value of an Employee.
4. Click on the Send button to send the GET request.


## Actual behavior
The application accepts the GET request with an invalid ID value in the request URL.The server responds with an error message that is not specific enough to identify the issue.

## Expected behavior
The application should validate the provided ID in the URL to ensure that it is a valid and or non existing employee ID.If an invalid ID is detected in the request body, the application should return a clear error response indicating that the ID is not valid

## Priority
High

## Screenshots/Video

<img width="1370" alt="Screen Shot 2023-08-24 at 14 08 42" src="https://github.com/erodm09/PaylocityTask/assets/102558006/1b8cd3d1-b80d-4afd-8a13-787892923397">

<img width="1022" alt="Screen Shot 2023-08-24 at 14 09 49" src="https://github.com/erodm09/PaylocityTask/assets/102558006/beaa4b9c-7b1a-470a-b546-06f068ac8fdc">

## Device Details:
Postman Version: 10.17.3-230823-0523
OS: MacOs 10.15.7
Version: Mac OS Monterrey Version 12.4
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<details>

<summary>Bug 11-API -  Inconsistent Response for PUT Request with Unchanged User Detailsd</summary>


## Description

When sending a PUT request to edit a user's information, if the request body contains the same details as the existing user, the application responds with a "200 OK" status. This behavior is inconsistent with the expectation that only changes in user details should trigger a successful update response.

## Pre-condition

Have the valid Postman collection imported in Postman


## Steps To Reproduce

1. Launch Postman and access the QA Challenge- Master collection
2. Go to the PUT request `Update Employee` to retrieve an Employee's information.
3. Provide the exact same details as the existing user in the request body.
4. Click on the Send button to send the PUT request.


## Actual behavior
The application accepts the PUT request with unchanged user details in the request body.The server responds with a "200 OK" status, suggesting a successful update even though no changes were made.

## Expected behavior
The application should validate the provided user details against the existing user's information.If the user details in the request body are identical to the existing user, the application should return a "304 Not Modified" status or an appropriate response indicating that no changes were made.

## Priority
Medium

## Screenshots/Video

<img width="718" alt="Screen Shot 2023-08-24 at 14 44 31" src="https://github.com/erodm09/PaylocityTask/assets/102558006/f3dd5599-6c6d-4c37-9e33-4dcd64b9b71c">

<img width="798" alt="Screen Shot 2023-08-24 at 14 44 45" src="https://github.com/erodm09/PaylocityTask/assets/102558006/436b6489-8865-4424-9535-5214f578a167">

<img width="1201" alt="Screen Shot 2023-08-24 at 14 46 50" src="https://github.com/erodm09/PaylocityTask/assets/102558006/0610394b-24ea-4308-87f5-1585c8ae464e">



## Device Details:
Postman Version: 10.17.3-230823-0523
OS: MacOs 10.15.7
Version: Mac OS Monterrey Version 12.4
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

