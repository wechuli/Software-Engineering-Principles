# Requirement Gathering

- Why requirements are important
- The characteristics of good requirements
- The MOSCOW method for prioritizing requirements
- Audience-oriented, FURPS and FURPS+ method for categorizing requirements
- Methods for gathering customer goals and turing them into requirements
- Brainstorming techniques
- Methods for recording requirements such as formal specifications, user stories, and prototypes

Requirements are the features that your application must provide. At the beginning of the project, you gather requirements from the customers to figure out what you need to build. Throughout development, you use the requirements to guide development and ensure that you're heading in the right direction. At the end of the project, you use the requirements to verify that the finished application actually does what it's supposed to do.

## Properties of Useful requirements

### Clear

Good requirements are clear, concise and easy to understand. To be clear, requirements cannot be vague or ill-defined. Each requirement must state in concrete, no-nonsense terms exactly what it requires.

### Unambigous

In addition to being clear and concrete, a requirement must be unambigous. If the requirement is worded so that you can't tell what it requires, then you can't build a system to satisfy it. As you write requirements, do your best to make them unambigous. Read them carefully to make sure you can't think of any way to interpret them other than the way you intend.

### Consistent

A project's requirements must be consistent with each other. That means not only that they cannot contradict each other, but they also don't provide so many constraints that the problem is unsolvable. Each requirement must also be self-consistent. In a complex project, it's not always obvous if a set of requirements is mutually consistent. Sometimes any pair of requirements is satisfiable but larger combinations of requirements are not
A common software engineering expression is "Fast,good,cheap.Pick two"
Try to kepp new requirements consisten with existing requirements.

### Prioritized

When you start working on the project's schedule, it's likely you'll need to cut a few nice-to-haves from the design. You might like to include every feature but don't have the time or budget, so something's got to go. At this point, you need to prioritize the requirements.

The MOSCOW is an acronym to help you remember a common system for prioritizing application features.
M- Must. These are required features that must be included. They are necessary for the project to be considered a success
S-Should. These are important features that should be included if possible
C-Could. These are desirable features that can be omitted if they won't fit in the schedule.
W-Won't These are complete;y optional features that the customers have aggreed will not be included in the current release.

### Verifiable

Requirements must be verifiable.Being verifiable means the requirements must be limited and precisely defined.

### Words to Avoid

- **Comparatives** - Words like faster, better, more and shinier. How much faster? Define "better" ? How much more?
- **Imprecise adjectives** - Words like fast, robust, user-friendly, efficient, flexible and glorious. These are just other forms of the comparatives.
- **Vague commands** - Words like minimize, maximize, improve and optimize.

## Requirement Categories

In general, requirements tell what an application is supposed to do. Good requirements share certain characteristics(they're clear, unambigous, consistent, prioritized and verifiable), but there are several kinds of requirements that are aimed at different audiences of that focus on different aspects of the application.

### Audience-Oriented Requirements

These categories focus on different audiences and the different points of view that each audience has. They use a somewhat business-oriented perspective to classify requirements according to the people who care the most about them.

#### Business Requirements

Business requirements lay out the project's high-level goals. They explain what the customer hopes to achieve with the project.

#### User Requirements

User requirements describe how the project will be used by the eventual end users. They often include things like sketches of forms, scripts that show the steps users will perform to accomplish specific tasks, use cases, and prototypes.Sometimes these requirements are very detailed, spelling out exactly what an application must do under different circumstances. Other times they specify what the user needs to accomplish but not necessarily how the application must accomplish it.
Vague requirements are bad, but flexible requirements let you explore different options before you start writing code. To keep requirements as flexible as possible, try to make the requirements spell out the project's needs without mandating a particular approach.

### Functional Requirements

Functional requirements are detailed statements of the project's desired capabilites. They're similar to the user requirements but they may also include things that the users won't see directly. These are things the application should do.

### Nonfunctional Requirements

Nonfunctional requirements are statements about the quality of the application's behavior or constraints on how it produces a desired result. They specify things such as the application's performance, reliability and security charateristics.

### Implementation Requirements

Implementation requirements are temporary features that are needed to transition to using the new system but that will be later discarded. The tasks descibed in implementation requirements don't always involve programming. Other implementation requirements include hiring new staff, buying new hardware, preparing training materials, and actually training the users to use the new system.

## FURPS

FURPS is an acronym for this system's requirement categories: functionality, usability, reliability, performance and scalability.

- _Functionality_ - What the application should do. These requirements describe the system's general features including what is does, interfaces with other systems, security etc
- _Usability_ - What the program should look like. These requirements describe user-oriented features such as the application's general appearance, ease of use, navigation methods and responsiveness.
- _Reliability_ - how reliable the system should be. These requirements indicate such things as when the system should be available, how often it can fail and how accurate the system is
- _Performance_ - How efficient the system should be. These requirements describe such things as the application's speed, memory usage, disk udage and database capacity.
- _Supportability_ - How easy it is to support the application. These requirements include such things as how easy it will be to maintain the application, how easy it is to test the code and how flexible the application is

## FURPS+

FURPS was extended into FURPS+ to add a few requirements categories that software engineers though were missing.

- _Design Constrains_- These are constraints on the design that are driven by other factors such as the hardware platform, software platform, network characteristics or database.
- _Implementation requirements_ - These are constraints on the way the software is built.
- _Interface requirements_ - These are constraints on the system's interface with other systems. They tell what other systems will exchange data with the one you're building. They describe things like the kinds of interactions that will take place, when they will occur, and the format of the data that will be exchanged.
- _Physical requirements_ - these are constrains on the hardware and physical devices that the system will use

##

- Functionality
- Usability
- Reliability
- Performance
- Supportability
- Design
- Implementation
- Interface
- Physical

Using requirements categories as a checklist can help you notice if you are missing certain kinds of requirements.

## Common Requirements

The following list summarizes some specific requirements that arise in many applications

- **Screens** - What screens are needed?
- **Menus** - What menus will the screens have ?
- **Navigation** - How will the users navigate through different parts of the system. Will they click buttons, use menus, or click forward and backward arows? Or some combination of those methods?
- **Work flow** - How does data move through the system
- **Login** - How is login information stored and validated?
- **User types** -Are there different kinds of users? Do they need different privileges?
- **Audit tracking and history** - Does the system need to track who made changes to the data?
- **Archiving** - Does the system need to archive older data to free up space in the database?Does it need to copy data into a data warehouse for analysis?
- **Configuration** - Should the application provide configuration screens that let the system administrators change the way the program works.

## Gathering requirements

The following describe several techniques you can use to gather and refine requirements

### Listen to Customers(and Users)

Sometimes customers come equipped with fully developed requirements spelling out exactly what the application should do, how it should work and what is should look like. More often, they just have a problem that they want solved and a vague notion that a computer might somehow help.
Start by listening to the customers. Learn as much as you can about the problem they are trying to address and any ideas they may have about how the application might solve the problem. Initially, focus as much as possible on the problem, not on the customers' suggested solutions,so you can keep the requirements flexible. Take lots of notes while you're listening to the customers.

### Use the Five Ws(and One H)

- **Who** - ask who will be using the software and get to know as much as you can about those people. Find out is the users and the customers are the same and learn as much about the users as you can.
- **What** - Figure out what the customers need the application to do.Focus on the goals as much as possible rather than the customers' ideas bout how the solution should work.
- **When** - Find out when the application is needed. If the application will be rolled out in phases, find out which features are needed when.
- **Where** - Find out where the application will be used. Will it be used on desktop computers or in a mobile phone
- **Why** - Ask why the customers need the application.
- **How** - Sometimes customers may have a better idea of how a certain problem should be implemented.

### Study Users

Interviewing customers(and users) can get you a lot of information, but iften customers won't tell you everything they do or need to do. By studying users as they work, you can learn more about what they need to do and how they are currently doing it. Then with your software-engineering perspective, you can look for solutions that might not occur to the users. As you study the users, pay attention to how they do things. Look at the forms they fill out(paper or online). Figure out where they spend most of their time. Look for the tasks that go smoothly and those that don't. You can use that information to identify areas in which your project can help.

## Refining Requirements

After you've talked to the customers and users and watched the users at work, you should have a good understanding about the users' current operations and needs. Next, you need to use what you've learned to develop ideas for solving the user's problems. You need to distill the goals(what the customers need to do) into approaches(how the application will do it)
Moving from goals to requirements often forces you to make some design decisions. The follwing describe 3 approaches for converting goals into requirements

### Copy Existing Systems

If you're building a system to replace an existing system or a manual process, you can often use many of the behavious of the existing system as requirements for the new one.
This approach has a few advantages:

- It's reasonable straightforward. You can dig through the existing application and find out what it does.
- This approach also makes it more likely that the requirements can actually be satisifed.
- This approach provides an unambigious example of what you need to do.

There are some disadvantages to this approach:

- Users are often reluctant to give up even the tiniest features in an existing program.

Using an existing system to generate requirements can be a git time-saver, as long as the development team and the customers all agree on which parts of the existing system will be included in the new one.
