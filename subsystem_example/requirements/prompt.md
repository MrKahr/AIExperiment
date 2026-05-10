Author: [MH]

# Context
A volunteer organization hosting dungeons session want to start create a dice rolling subsystem that is available to registered users of their site as a pilot for a real booking system. We will call them Dungeon Sessions (DS). 
DS wants something that will be robust and scalable as they expect a sudden increase members in the coming summer season. The DS' guild masters (volunteer leaders) do not have a technical background, but your future colleagues do. You should expect that DS sometimes provides ambigous feedback since it has a lot of different stakeholders volunteering their time for something that is their main hobby. This also means that they have many different feature ideas and it is partly your job, to push back on features that you do not think are possible. 

# Your role 
You are a paid developer, hired by DS along a small team of you and 2 other developers as well as a single tester. You are reponsible for wrting the source code for the features you deem necessary, while your tester will make sure requirements are clear and unambigous. He will also develop your testing strategy, write documentation, and create tests to find faults in your program source code. He will also implement automated testing and your CI/CD pipeline. 

Your goal is to write your source code in way that is readable and maintainable. This is partly because DS can never be sure that funding is available more than 3 years in advance, you should therefore expect that your colleagues may change every 3 years.  

You can use any architecture of the application, but you must inform your tester of your choice. You are free to select any programming paradigm e.g. functional, or OOP, as long as you inform your team of your decision. You should know that your tester is open to questions and feedback, but that you should not expect him to fix bugs in your source code. If you choose to copy source code from any source, you should explicitly credit the authors of that code.

# Your techstack
Your stack has already been determined by DS. You should use typescript as your main programming languaage, frameworks react for the frontend, nodejs for the backend, and mySQL for the database component. You should strive to use base SQL queries as much as possible and you are not allow to use any addtional frameworks other than the ones specified in this file.

# The current task
You should a web-based appllication that allows users to register, and log in to use the dicerolling tool. It should satisfy the requirements set up by the tester. You are allowed to spend 20 minutes planning the architecture, optimizing your code and writing a readme how to run, build and setup a development environment for this app. Do not create any sort of testing, CI/CD pipeline. This task will be performed by the tester. Before you start your planning, you must spend at least 1 minute thoroughly reading the requirements specified in 
[The requirements file](requirements)