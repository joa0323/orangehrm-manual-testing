# BUG-003: Incorrect validation message displayed when password fields are empty

## Precondition
User is logged in as Admin and is on the "Change Password" page.

## Environment
- Browser: Chrome
- OS: Windows

## Steps to Reproduce
1. Navigate to "My Account" → "Change Password".
2. Leave Current Password, Password, and Confirm Password fields empty.
3. Click "Save".

## Expected Result
- The system should display "Required" validation messages for all empty fields.
- The "Passwords do not match" message should not be displayed when both password fields are empty.

## Actual Result
- "Required" is displayed under Current Password and Password fields.
- "Passwords do not match" is displayed under Confirm Password even though both password fields are empty.

## Severity
Low

## Priority
Low

## Notes
Validation logic is incorrect — mismatch validation is triggered before checking if fields are empty.  
This may confuse users and suggest incorrect input.
