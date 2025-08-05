# Register App Users

You are a junior developer working in a small start-up. Your managers have asked you to develop a new account registration system for a mobile app. The system must validate user
input on the sign-up form before creating an account.

The previous junior developer wrote some helper functions that validate the name, email, and password. Use these functions to register users, store their data, and implement 
some error handling! These have been imported into the workspace for you. They will be a great help to you when registering the user, but first you have to understand what the 
function does! Inspect the docstrings of each of the helper functions: validate_name, validate_email and validate_password.

```python
# Re-run this cell and examine the docstring of each function
from python_functions import validate_name, validate_email, validate_password, top_level_domains

print("validate_name\n")
print(validate_name.__doc__)
print("--------------------\n")

print("validate_email\n")
print(validate_email.__doc__) 
print("--------------------\n")

print("validate_password\n")
print(validate_password.__doc__)

# The top level domains variable is used in validate_email to approve only certain email domains
print(top_level_domains)
```

**Expected Output:**

```
validate_name

 Checks that the name is greater than two characters and is a string data type.

 Args:
    name (str): The inputted name from the user.

 Returns:
    bool: True if the name passes the check, False otherwise.
    
--------------------

validate_email

 Checks that the email address is in a valid format, has a username greater than 1 character, an '@' symbol, and an allowed domain that is in the `top_level_domains` variable.

  Args:
    email (str): The inputted email from the user.

  Returns:
    bool: True if the email passes the checks, False otherwise.
    
--------------------

validate_password

 Checks that the password is strong enough. It should include a capital letter, a number between 0-9 and be greater than 8 characters.

  Args:
    password (str): The inputted password from the user.

  Returns:
    bool: True if the password passes the checks, False otherwise.
    
['.org', '.net', '.edu', '.ac', '.uk', '.com']
```
## The project instructions

Create a validate_user() function, using some helper validation functions to verify user input.

The function should take in the parameters: name, email, and password.
The function should call each of the helper validation functions (validate_name(), validate_email(), and validate_password()).
If any check fails, raise a ValueError with a descriptive error message about the failing validation.
If all checks pass, return True.
Now that you've validated that all the user details are correct, you want to allow users to register to the app. Create a register_user() function to handle the registration logic.

The function should take in the parameters: name, email, and password.
Inside, it should call validate_user() to ensure that the user input is valid.
If validate_user() raises a ValueError, register_user() should catch the exception and return False.
Otherwise, it should create and return a dictionary with the keys: name, email, and password.

## Concepts practiced

Function composition: Calling helper functions (validate_name, validate_email, validate_password) from within a higher-level function (validate_user).

Boolean validation logic: Using helper functions that return True/False to determine if input passes the rules.

Error handling with exceptions: Raising ValueError when validation fails to provide meaningful feedback.

Custom error messages: Writing descriptive messages for each type of failed validation.

Separation of concerns: Keeping validation logic in helper functions, while validate_user coordinates the process.

Basic API design: Designing register_user to handle validation results and return either a user dictionary or False.

Markdown documentation: Using code blocks, expected output sections, and docstrings in the README.

