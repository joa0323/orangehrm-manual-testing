# BUG-004: Search does not ignore leading space in Employee Name field

## Precondition
User is logged into the system and is on the PIM Employee List page.  
An employee with the name "John" exists in the system.

## Environment
- Application: OrangeHRM Demo
- Module: PIM
- Browser: Chrome
- Testing type: Manual testing

## Steps to Reproduce
1. Navigate to the PIM module.
2. Make sure the Employee List page is open.
3. In the Employee Name field, enter " John" (with a leading space).
4. Click the Search button.

## Expected Result
The system should ignore leading spaces in the search field and return the employee record for "John".

## Actual Result
The system displays the message "No Records Found" and no employee records are returned.

## Severity
Low

## Priority
Low

## Notes
Searching for "John" returns the correct result.  
Searching for "John " (with a trailing space) also returns the correct result.  
Searching for " John" returns "No Records Found".
