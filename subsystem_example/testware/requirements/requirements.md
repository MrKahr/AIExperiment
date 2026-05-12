Author: [MH]
# NOTE
It is important that you read through all of these requirements before you build anything. Also, each requirement has been ranked by importance as specified by DS.

## Terminology
DS: Dungeon Sessions, the volunteer organization that hosts Dungeons and Dragons sessions

GM: Game master, the person responsible for creating the story world and interacting with the players to continue the story. 

DnD: A tabletop roleplaying game developed by Gary Gygax. 

PC: A character in the game story controlled by a player

NPC: A character in the game story controlled by a player

## Introduction and Purpose
The purpose of this web-based system is allow registered members of DS to perform dice rolls of many different dice types easily. DS current roll their dice by hand to determine the outcome of actions in DnD. It is currently difficult for members to keep track of their dice rolls over many sessions and roll many dice simultaneously. This is a problem because Admins cannot verify that members really did perform a really difficult action several sessions ago, as well as perform large battles because many dice have to be rolled simultaneously.  

## User Requirements (UR) - Prioritized
0. Users can register accounts with mandatory profile data: mail, name and password.
1. Registered users can gain authenticated status by entering name and password into login screen.
2. Authenticated users may simulate rolls and view name and mail of other users. 
3. Users can simulate dice rolling of n-sided die with $n \in N$ (at least d4,d6,d8,d10,d12,d20,d100).
4. Admins can ban users preventing them from accessing features that requires user authentication.
5. Admins can view any users dice roll history. 
6. Admins can unban user restoring their access to features that require authentication.
7. Admins can search database for user by entering name, or mail


## User Roles
| Role | Description | Permissions | Restrictions |
|------|-------------|-------------|--------------|
| Admin | Moderates members, enforces code of conduct and verificies claim about dice rolls | view members, view members details, search user, reset password, ban member, unban member, view roll history | see user password, modify dice roll history, delete user |
| Member | Registers and authenticates credentials, and rolls dice using simulator | register,  reset password, see user password, view roll history | view members, ban member, unban member  |


## User stories/cases
## User Requirements (UR) - Prioritized
0. Users can register accounts with mandatory profile data: mail, name and password.
1. Registered users can gain authenticated status by entering name and password into login screen.
2. Authenticated users may simulate rolls and view name and mail of other users. 
3. Users can simulate dice rolling of n-sided die with $n \in N$ (at least d4,d6,d8,d10,d12,d20,d100).
4. Admins can ban users preventing them from accessing features that requires user authentication.
5. Admins can view any users dice roll history. 
6. Admins can unban user restoring their access to features that require authentication.
7. Admins can search database for user by entering name, or mail

### Case 1: I want to join DS - UR [0,1]
I have been refered to join DS by a friend of mine. I want to register to their web-based tool to be able to roll dice to perform actions in our shared story in our Dungeons game. I have a good foundational knowledge of how to use web-based applications, I can navigate the a website using the navigation bar and expect the registration process to be similar to other web-based apps (e.g. DnD beyond)

### Case 2: I want to -  UR [2,3]
I have registered my account and I want to use the system to roll dice during my DnD games. 

### Case 2: UR (4,6)

### Case 3: UR (5,7)

## Functional requirements - Place in table
## Non-functional requirements - Place in table

# Acceptance Criteria
## Dice rolling 
## Member management 
## 

## Future features
- View probability distributions of N dice of type Y
- System keeps track of users whose rolls are outside 95% confidence interval and flags as potential cheaters