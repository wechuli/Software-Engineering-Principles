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
