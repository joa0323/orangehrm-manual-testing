# BUG-001: Multiple clicks on "Reset Password" cause inconsistent behavior

## Precondition
User is on the "Reset Password" page.

## Environment
- Browser: Chrome
- OS: Windows

## Steps to Reproduce
1. Open the Login page.
2. Click "Forgot your password?"
3. Enter a valid username (e.g. Admin).
4. Click "Reset Password" rapidly 2–3 times.

## Expected Result
- The "Reset Password" button should be disabled after the first click or show a loading indicator.
- Only one request should be processed.
- The page should remain responsive.

## Actual Result
- The button remains clickable and allows multiple submissions.
- The page enters a prolonged loading state.
- In one instance, the browser tab crashed (Chrome error: "Aw, Snap!" / STATUS_ACCESS_VIOLATION).
- Behavior is inconsistent (sometimes confirmation message appears, sometimes long loading occurs).

## Severity
High

## Frequency
Intermittent (reproduced multiple times)

## Notes
Issue appears during rapid user interaction.  
May impact system stability and user experience.
