Author: [MH]

## Helpful guide from IEEE
- Unambiguous – Open to only one interpretation
- Complete – Nothing missing within project scope
- Verifiable – Ability to test or demonstrate satisfaction
- Consistent – No conflicts between requirements
- Ranked – Clear relative importance and stability

# System description (IEEE)
## Introduction and Purpose
The purpose of this web-based system is to link DnD sessions to attending members. The organization (DS) currently have no way to systematically determine which users attended which sessions - they currently rely on google sheet which is prone to human error. It is therefore impossible for the admins and hosts of a session to verify whether a member's player character is as powerful as they claim. This opens sessions to abuse, and users claim registering for sessions is currently cumbersome. 

## Business Requirements


## Value Chain 
I use the term "Value Chain" to refer to a business' core model of generate income. DS has the following value chain
- Funding drive + Member recruitment drive -> Funding distribution -> Session hosting -> Membership maintainence

## User Personas or Roles
- Admin: 
- User:
- Member: A person paying to be part of DS' activities who may or may not be a user of the booking system
- Host: A person in charge of single sessions. This person is both a member and a user. 

## Feature List
-  

## User Story or Use Cases
## User Requirements
## Functional Requirements
## Nonfunctional Requirements
## Interface Requirements
## Performance Requirements
## Security Requirements

## Design and Implementation Constraints
- System stack must consist of javascript, node and mySQL since resources are very limited at DS
- 
## External System Requirements
## Quality Assurance Requirements
## Documentation Requirements

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

### TODO: 
- Create nice value chain picture [Value Chain section](#value-chain)