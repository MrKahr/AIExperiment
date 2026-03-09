Author: MH

# Requirements
## Functional requirements 
- Application should provide differing levels of access to non-users, users and admins
- Database should support at least 10k records
- Database schema should have reduced redundancy (BCNF or 3NF forms if possible)

## Non-functional requirements
- The application should support at least 10k users being logged in simultaneously
- The application should not take longer than 2 seconds to register new users once "register" button is clicked
- 50% of users should rate the intuitiveness of the UI at least a 4 (on a 5-point scale)
- User passwords should be stored safely (encrypted), but user data should be available to admins