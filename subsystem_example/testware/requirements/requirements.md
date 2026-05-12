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

## User Requirements (UR) - Prioritized
0. Users can register accounts with mandatory profile data: mail, name and password.
1. Registered users can gain authenticated status by entering name and password into login screen.
2. Authenticated users may simulate rolls and view name and mail of other users. 
3. Users can simulate dice rolling of n-sided die with $n \in N$ (at least d4,d6,d8,d10,d12,d20,d100).
4. Admins can ban users preventing them from accessing features that requires user authentication.
5. Admins can view any users dice roll history. 
6. Admins can unban user restoring their access to features that require authentication.
7. Admins can search database for user by entering name, or mail

## Use cases
### Case 1: I want to join DS - UR [0,1]
I have been refered to join DS by a friend of mine. I want to register to their web-based tool to be able to roll dice to perform actions in our shared story in our Dungeons game. I have a good foundational knowledge of how to use web-based applications and I can navigate a website using the navigation bar. I expect the system to provide me with way to input my credentials and tell me if I am doing anything wrong. 

### Case 2: I want to roll some dice -  UR [2,3]
I have registered my account and I want to use the system to roll dice during my DnD games. I want the system to keep track of my rolls, especially when I perform many rolls of different dice that are annoying to track by ha nd. I expect the system to be able to roll all the dice I know and to know that 1s and 20s are special natural numbers in DnD.

### Case 3: I want to enfore our CoC - UR [4,6]
I have been a part of DS for the last 3 years, and I have been made admin of the system recently. I want to ensure that members who behave against our CoC for DnD sessions are banned from using our systems. I also want to ban members that abuse the dice rolling system. I have a foundational knowledge of system administration, and I know DS' goals and members well. 

### Case 4: UR (5,7)
I have been a part of DS for the last 3 years. I want to check members dice rolling history especially when I need to confirm a claim made by a player. To find out whether a player is being disingenious, I need to make a lookup in our database of players to find the player whose claim I need to verify. Then I want to see their roll history. I have a foundational knowledge of system administration, and I have experience using UI to search for entities in a database.

## Functional requirements
| ID   | Description | Categories  | Dependencies |
|------|-------------|-------------|--------------|
| FR1  |
| FR2  |
| FR3  |

## Non-functional requirements
| ID   | Description | Categories  | Dependencies |
|------|-------------|-------------|--------------|
| NFR1 | 

# Acceptance Criteria
## Registering
## Dice rolling 
## Member management 

## Future features
- View probability distributions of N dice of type Y
- System keeps track of users whose rolls are outside 95% confidence interval and flags as potential cheaters