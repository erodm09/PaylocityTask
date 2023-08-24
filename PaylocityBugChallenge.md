
# Paylocity STE Assessment- Bug Challenge

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


