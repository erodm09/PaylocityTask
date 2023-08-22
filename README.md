# Paylocity STE Assessment- Bug Challenge

<details>

<summary>Bug 01- Error Occured processing request/summary>
## Description
Upon attempting to process a user's request, an error occurs with the following details:

Error Message: An error occurred while processing your request.
Request ID: 0HMT379708TF5

The error message suggests that there was a problem during the request processing. It includes a unique Request ID for tracking purposes.

Additionally, the message provides an option to enable "Development Mode" for more detailed error information. However, a caution is given against using this mode in deployed applications due to potential exposure of sensitive information to end users.

## Steps To Reproduce

1.Go to the URL: `https://wmxrwq14uc.execute-api.us-east-1.amazonaws.com/Prod/Account/Login`

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

<summary>Bug 02- Error Handling not clearing after User goest back</summary>


## Description
After a user inputs an incorrect or missing password during the login process and then attempts to rectify the error by refreshing the page, the initial error message persists. The error message indicates that an incorrect password was provided and provides a Request ID for tracking.

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
A clear and concise description of what you expected to happen.

## Priority
High

## Screenshots/Video


## Device Details:

OS: MacOs
Version: Mac OS Monterrey Version 12.4
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]


