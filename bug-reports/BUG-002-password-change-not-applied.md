# BUG-002: Password change shows success message but new password does not work

## Precondition
User is logged in as Admin.

## Environment
- Browser: Chrome
- OS: Windows

## Steps to Reproduce
1. Navigate to "My Account" → "Change Password".
2. Enter current password: admin123.
3. Enter new password: other123.
4. Click "Save".
5. Log out.
6. Attempt to log in using username Admin and password other123.

## Expected Result
User should be able to log in using the new password.

## Actual Result
- Login fails with "Invalid credentials" message.
- Old password (admin123) still allows login.
- UI displays a success message despite the password not being updated.

## Severity
High

## Priority
High

## Notes
System shows a success message, but the password is not updated.  
This may lead to user confusion and potential security concerns.
