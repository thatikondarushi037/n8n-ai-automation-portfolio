# Day 1 - Webhooks 
## Lead Validation

Added an IF node to validate incoming leads.

Validation rules:
- Name must not be empty
- Email must not be empty
- Budget must be greater than 0
- Employees must be greater than 0

## Failure cases tested

- Missing email
- Missing name
- Zero budget
- Zero employees
- Whitespace-only input
- Invalid budget string
- Negative numbers

## Finding

The current validation only checks whether an email exists.
It does not yet verify that the email format is valid.

Example:

hello

currently passes the "is not empty" validation.

Next improvement:
Add email-format validation and proper error responses.
