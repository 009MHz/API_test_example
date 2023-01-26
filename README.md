# Test Documentations

## <span style ="color:orange">1. Create Account</span>
### Response Validation
This script contains tests to validate the response from a request.
- *Test 1: Request is succeed* <br>
This test checks that the request was successful by verifying that the response status code is 200. 

- *Test 2: Response delay is accepted* <br>
This test checks that the response time is within an acceptable range by verifying that the response time is below 1000 milliseconds.

### Contents Response Validation
This script contains tests to validate the contents of the response body.
- *Test 1: User "***id***" is generated* <br>
This test checks that the 'id' field in the response body is not empty.

- *Test 2: ***token*** is generated* <br>
This test checks that the 'token' field in the response body is not empty.

### Parsing the inserted value into environment variables
This script contains code to parse the request body and store the values in environment variables.

The script first parses the request body as a JSON object and stores it in the ***"requestBody"*** variable. It then uses the `pm.environment.set()` function to set the values of the `"name", "email", "first_name", and "last_name"` environment variables.

### Parsing the output into environment variable
This script contains code to parse the response body and store the values in environment variables.

The script first parses the response body as a JSON object and stores it in the `data` variable. It then uses the `postman.setEnvironmentVariable()` function to set the values of the `id` and `token` environment variables.

## 2. Check Account Details
### Response Validation
This script contains tests to validate the response from a request.
- *Test 1: Request is succeed* <br>
This test checks that the request was successful by verifying that the response status code is 200.

- *Test 2: Response delay is accepted* <br>
This test checks that the response time is within an acceptable range by verifying that the response time is below 1000 milliseconds.

### Contents Response Validation
This script contains tests to validate the contents of the response body.
- *Test 1: User ***"id"*** is correct* <br>
This test checks that the `id` field in the response body is correct by comparing it to the value of the `id` that stored in the environment variable.

- *Test 2: User ***email*** is correct* <br>
This test checks that the `email` field in the response body is correct by comparing it to the value of the *"email"* environment variable.

- *Test 3: User ***"first name"*** is correct* <br>
This test checks that the `first_name` field in the response body is correct by comparing it to the value of the `first_name` environment variable.

- *Test 4: User "***last name***" is correct* <br>
This test checks that the `last_name` field in the response body is correct by comparing it to the value of the `last_name` environment variable.

## 3. Update Account
### Response Validation
This script contains tests to validate the response from a request.

- *Test 1: Request is succeed* <br>
This test checks that the request was successful by verifying that the response status code is 200.

- *Test 2: Response delay is accepted* <br>
This test checks that the response time is within an acceptable range by verifying that the response time is below 700 milliseconds.

### Contents Response Validation
This script contains tests to validate the contents of the response body.

- *Test 1: Response body contains ***'updated'**** <br>
This test checks that the response body contains the string `updated`.

- *Test 2: Updated response value is ***not empty**** <br>
This test checks that the 'updatedAt' field in the response body is not empty.

### Parsing the updated value into environment variables
This script contains code to parse the request body and store the values in environment variables.

The script first parses the request body as a JSON object and stores it in the `requestBody` variable. It then uses the `pm.environment.set()` function to set the values of the `gender` and `job` environment variables.

## 3b. Validating updated Account
### Response Validation
This script contains tests to validate the response from a request.

- *Test 1: Successful POST request* <br>
This test checks that the POST request was successful by verifying that the response status code is one of [201, 200, 202].

- *Test 2: Response delay is accepted* <br>
This test checks that the response time is within an acceptable range by verifying that the response time is below 1000 milliseconds.

### Validate the existing response content
This script contains tests to validate the contents of the response body for existing user information.

- *Test 1: User ***'ID'*** is correct* <br>
This test checks that the 'ID' field in the response body is correct by comparing it to the value of the "id" environment variable.

- *Test 2: User ***'email'*** is correct* <br>
This test checks that the `email` field in the response body is correct by comparing it to the value of the `"email"` environment variable.

- *Test 3: User ***first name*** is correct* <br>
This test checks that the `'first_name'` field in the response body is correct by comparing it to the value of the `"first_name"` environment variable.

- *Test 4: User ***last name*** is correct*
This test checks that the `'last_name'` field in the response body is correct by comparing it to the value of the `"last_name"` environment variable.

### Validate the updated content
This script contains tests to validate the updated user information stored in the environment variables.

- *Test 1: Job is updated* <br>
This test checks that the `'job'` field in the environment variables is not empty.

- *Test 2: Gender is updated*
This test checks that the `'gender'` field in the environment variables is not empty.

## 4. Deleting the account
### Validating the Response contents
This script contains tests to validate the response from a request.

- *Test 1: User ***ID*** has been cleared* <br>
This test checks that the user ID has been successfully cleared by verifying that the response status code is 204.

- *Test 2: Response delay is accepted* <br>
This test checks that the response time is within an acceptable range by verifying that the response time is below 700 milliseconds.

### Removing environment variables
This script contains code to remove the specified environment variables. The script first defines an array of variable names and then uses the `pm.environment.unset()` function to remove each variable.

### Validating the deleted environment
This script contains tests to validate that the specified environment variables have been successfully removed.

The script first defines an array of variable names and then uses a loop to iterate through each variable. For each variable, the script uses the pm.expect() function to verify that the value of the variable is undefined.
