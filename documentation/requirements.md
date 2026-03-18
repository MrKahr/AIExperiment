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
### Case 1: Host 
As a host, I want to create, plan and host interesting DnD sessions for fellow members. 

### Case 2: User + info 
- As a user, I want see attend sessions that I find interesting, and see and update my character information to fell a sense of character progression. I also want to perform actions actions in DnD (roll dice). 

### Case 3: Admin 
- As an admin, I want to keep track of members' statuses which I use for applying for funding, and to remove members from the union if they don't live up to our code of conduct. 

## Feature List
1. Session booking - Users create, and register for DnD sessions
2. User registration - Users sign up to system with their details
3. Statistics dashboard - Admins can see and administrate membership status of each user
4. User dashboard - User have an overview of which sessions they are registered for and which characters they have used in sessions
5. Dice rolling - Users provided with dice rolling tool that shows rolling animation

## Business Requirements (BR)
1. DS should be able to view, cancel and edit session details
2. DS should make session information to available to users to register
3. DS should have access to membership statistics (Required for DS funding)

## User Requirements (UR)
1. Users should be able to register for system
2. Users should be able to create DnD session in system
3. Users should be able to register for DnD session
4. Users should be able to see their registrations
5. When two users are registerd for the same session, they should be to see other users' mail and screen names
6. Admin users should be able to see list of all members in database
7. Users should be able to see their character information e.g. name, level, items, class, spells and abilities
8. User should be able to export their data to formats pdf, docx or excel
9. Users should be able to roll virtual dice

# Functional Requirements (FR)
## Interface requirements (IR)
    1. While a user is not logged in, system page "my profile" shall provide user with window with fields 
        - username (required)
        - email (required)
        - phone + country code 
        - password
   
    2. When a 
    - When an authenticated user selects "my dashboard", system shall provide navigation options
        - For users: 
            - my profile
            - my characters
            - my sessions
            - host session
            - dice roller 
        - For admins (addtionally)
            - member info 
    Each option shall open corresponding page. 
     - When an authenticated user selects "my sessions", system shall display
        - list of sessions 
        - time + date + location of session
        - host user name 
        in separate window
    - When an authenticated user selects "my character", system shall display 
        - character name 
        - character level + xp
        - character items 
        - character gold 
        - character portrait 
- While an authenticated user is logged in, system shall provide navigational elements between pages:
    - landing page
    - events page
    - about us page
    - my profile
- When an authenticated user selects "dice roller", the system shall display options 
    - dice type (d4,d6,d8,d12,d20,d100)
    - dice amount (1-100)
    - roll

## Data and data representation 
 1. System shall validate each field in sign-up form with regex patterns server side with criteria for each field
        - username 
            - no longer than 16 chars
            - no spaces
        - email
            - at least one @
            - at least 1 char before and after @
            - must end in suffix .[dk, com, org]
        - password 
            - at least 8 character
            - one special character
            - one uppercase character
2. When an account or event is created, the following fields are checked for duplicates in the database 
    - username 
    - email
    If system finds duplicate, system shall "error" operation and user shall be provided with error window containing plaintext message: "System error: cannot create account, please enter new details" 
3. When a user registers, system shall store the following information in database: 
    - joined date
    - username
    - role flag
- When user selects "my characters", system shall show window with character information 
    - Name 
    - Portrait 
    - Class
    - exp/level 
    - items 

## Security
1. System shall assign the first user to register in system the flag of admin (1)
2. When a user registers any besides the first user, system shall assign lowest level access flag to that user. 
3. When system assigns and accesses flag, it shall assign the levels
    - user: 0/1
    - admin: 0/1
- System shall allow admin user to perform "change role" operation on authenticated users with option in dashboard 
    - demote to user 
    - promote to admin
- System shall p
- System shall provide admin with option 
- System shall only provide admins with view of user name, membership status (active/inactive), date joined.

# Nonfunctional Requirements (NFR)
## Interface Requirements 
- System interface shall be rated more than 3 by 50% of user on "ease of use" scale (5 point scale).
- System shall be accessible to colorblind users (e.g. by providing a colorblind mode)

## Performance Requirements
- System database shall allow at least 10k records
- System shall allow at least 1k user to be loggin in simultanously
- System database schema shall have reduced redundancy (BCNF or 3NF forms if possible)
- System shall not take more than 2 seconds to perform registration operation for new users
- System uptime over a week shall be at least 95% 

## Security Requirements 
- System shall authenticate users using an authentication algorithm 
- Application should store user passwords using an encryption algorithm
- System shall not allow admins to see other user passwords
- System shall not allow users to see admin dashboard

## Legal requirements
- System shall comply with GDPR e.g. by deleting non-member profiles in database after 6 months
- While a user has not ticked consent box, the system shall not perform the register operation

## Design and Implementation Constraints
- System shall be implemented with typescript, node and mySQL

## Quality Assurance Requirements
- System shall not lose database records when server is turned off 
- System shall perform automated database backup every 24 hours
- System shall be tested on all critical functions
- System shall be tested using unit testing 
- System shall be tested using integration testing 
- System shall be tested using system testing 
- System shall be tested using integration testing 
- System shall be tested using automated testing

## Documentation Requirements
- System shall provide documentation on critical functions
- When system provides documentation on functions, classes or object, these must be documented with at least the purpose of the code, and the meaning of any parameters or fields. 

### TODO: 
- Create nice value chain picture [Value Chain section](#value-chain)
- Use system design book to provide illustrations for system operations

### TIPS learned 
- Always refine business and user requirements first - that will make it way easier to define requirements later
- All system requirements should follow from user + business requirements. It is easiest to just iterate through those first to ensure good coverage in the first requirement specification