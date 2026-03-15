Author: [MH]

# Guide from IEEE
Requirements shall be written such that they are: 
- Unambiguous – Open to only one interpretation
- Complete – Nothing missing within project scope
- Verifiable – Ability to test or demonstrate satisfaction
- Consistent – No conflicts between requirements
- Ranked – Clear relative importance and stability

# Writing requirement framework EARS
- While <optional pre-condition>, when <optional trigger>, the <system name> shall <system response>

# System description (IEEE)
## Introduction and Purpose
The purpose of this web-based system is to link DnD sessions to attending members. The organization (DS) currently have no way to systematically determine which users attended which sessions - they currently rely on google sheet which is prone to human error. It is therefore impossible for the users to keep track of sessions they are attending, and hosts of a session cannot verify whether a member's player character is as powerful as members claim. This opens sessions to abuse, and users claim registering for sessions is currently cumbersome. 

## Value Chain 
I use the term "Value Chain" to refer to a business' core model of generate income. DS has the following value chain
- Funding drive + Member recruitment drive -> Funding distribution -> Session hosting -> Membership maintainence

## User Personas or Roles
- Admin: Uses system to request data about users and updates user membership status
- User: Uses system to sign up for sessions and track character progression. Users pay a membership fee. 
- Member: May or may not use the system. A member pays a membership fee to part of DS' activities. 
- Host: Uses the system to create sessions. This person is both a member and a user. 

## User Story or Use Cases
Case 1: Hosting a session 

Case 2: Updating your character 

Case 3: Seeing member statistics

## Feature List
- User registration 
- Statistics dashboard 
- User dashboard 
- Session booking 

## Business Requirements (BR)
1. System shall manage hosted sessions
2. System shall generate session information to users
3. System shall generate membership statistics (Required for DS funding)

## User Requirements (UR)
- System must be able to export data to common formats e.g. pdf, docx or excel
- System must be able to roll dice 

# Functional Requirements (prefix: FR)
2. System must comply with GDPR e.g. by ensuring inactive users are deleted after 6 months of inactivity 

## Funct
## Data representation 

# Nonfunctional Requirements

## Interface Requirements

## Performance Requirements

## Security Requirements

## Design and Implementation Constraints
- System stack must consist of typescript, node and mySQL since system maintainablility is important for DS.
## External system Requirements


## Quality Assurance Requirements

## Documentation Requirements
- System functions, classes or object must be documented with at least the purpose of the code, and the meaning of any parameters or fields. 

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
- Reread system design book again for nice illustrations