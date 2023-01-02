# moduit API test Documentations

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

## <span style = 'color:green'>2. Check Account Details </span>
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

## <span style = 'color:blue'>3. Update Account </span>
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
