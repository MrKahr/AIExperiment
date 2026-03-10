Author: MH

# Requirements
Use the IEEE template

## Functional requirements 
- Application should provide navigational links between pages: landing page, events page, and about us page
- Application should not allow users to duplicate events or accounts 
- Application should authenticate users using an authentication algorithm 
- Application should provide admins with view of user details from database. This view should not be available to users and non-users. 
- Application should provide differing levels of access to non-users, users, admins, and super admins
- Application should only allow 4 members to have the role of superadmin at any time 
- Application should only allow superadmins to promote admins, and superadmins can promote other superadmins only if there are less than 4 current superadmins. 
- Application should allow admins to promote exactly one superadmin iff there are exactly 0 current superadmins
- Application should contain the following information on users: joined date, screen name, age, branch, role, sessions booked, and characters associated with a player. 
- Application should provide details on character associated with a player, including items, exp, name and level of each character
- Application database should support at least 10k records
- Application database schema should have reduced redundancy (BCNF or 3NF forms if possible)
-  Application should store user passwords safely (encrypted), but user data should be available to admins

## Non-functional requirements
- The application should support at least 10k users being logged in simultaneously
- The application should not take longer than 2 seconds to register new users once "register" button is clicked
- 50% of users should rate the intuitiveness of the UI at least a 4 (on a 5-point scale)
- Application should obtain consent for keeping user data when users register
- Application should not keep data longer than 5 months unless consent is given by users for explicit store (GDPR-compliance)