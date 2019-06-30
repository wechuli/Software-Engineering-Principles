# High Level Design

High-level design provides a view of the system at an abstract level. It shows how the major pireces of the finished application will fit together and interact with each other.

A high level design should also specify assumptions about the environment in which the finsihed application will run. The high-level design doesn not focus on the details of how the pieces of the application will work. those details can be worked out later during the low-level design and implementation.

## The Big Picture

You can view software development as a process that chops up the system into smaller and smaller pieces until the pieces are small enough to implement. Using that viewpoint, high-level design is the first step in the chopping up process.

The goals is to divide the system into chunks that are self-contained enough that you could give them to separate teams to implement. In some projects, you may want to assign multiple pieces of the project to a single team, particularly id the pieces are closely related.

## What to Specify

Exactly what you should specify in the high level design varies somewhat, but some things are constant for most projects. The following sections describe some of the most common items you might want to specify in the high-level design.

### Security

Your high-level design should sketch out all the application's security needs.

- Operating System Security
- Application Security
- Data security
- Network Security
- Physical security

All these forms of security interact with each other, sometimes in non-obvious ways.

### Hardware

You need to specify the hardware that will run your application.Sometimes, this will be relatively straightforward. For
example, your application might run on a laptop or in a web page that could run on any webenabled hardware. Other times the hardware specifi cation might include multiple devices connected via the Internet, text messages, a custom network, or by some other method.

### User Interface

During high-level design, you can sketch out the user interface, at least at a high level. For example, you can indicate the main methods for navigating through the application.

In addition to the application's basic navigational style, the high-level user interface design can describe special features such as clickable maps, important tables, or methods for specifying systaem settings(such as sliders, scrollbars or text boxes)

This part of the design can also address general appearance issues such as color schemes, company logo placement and form skins. Unless you have a good reason to change the way most applications already work, stick with what the users already know.

You don't need to specify every label and text box for every form during high-level user interface design. You can handle that during low-level design and implementation.

### Internal Interfaces

When you chop the program into pieces, you should specify how the pieces will interact. Then the teams assigned to the pieces can work separately without needing constant coordination.

It's important that the high-level design specifies these internal interactions clearly and unambiguosly so that the teams can work as independently as possible. It's worth spending some extra time to define these sorts of internal interfaces carefully before developers start writing code. Unfortunately, you may not be able to define the interfaces before writing at least some code. In that case, you may need to insulate two project teams by defining a temporary interface. After the teams have written enough code to know what information they need to exchange, they can define the final interface.

### External Interfaces

Many applications must interact with external systems.

In a way, external interfaces are often easier to specify than internal ones because you usually don't have control over both ends of the interface. If your application needs to interact with an existing system, then that system already has interface requirements that you must meet.

### Architecture

An application's architecture describes how its pieces fit together at a high level. Developers use a lot of 'standard' types of architectures. Many of these address particular characteristics of the problem being solved.

#### 1. Monolithic

In a monolithic architecture, a single program does everything. It displays the user interface, accesses data, processes customer orders, prints invoices, etc and everything else.
There are some obvious drawbacks to this approach:

- The pieces of the system are tied closely together, so it doesn't give you a lot of flexibility.
- A monolithic architecture also requires that you understand how all the pieces of the system fit together from the beginning of the project.
  Monolithic applications do have some advantages:\
- Because everything is built into a single program, there's no need for complicated communication across networks.
- Monolithic architectures are also useful for small applications where a single programmer or team is working on the code

### 2. Client/Server

A client/server architecture separates pieces of the system that need to use a particular function(clients) from parts of the system that provide those functions(servers). That decouples the client and server pieces of the system so that developers can work on them separately. The two-tier architecture makes it easier to support multiple clients with the same server, but it ties clients and servers relatively closely together. the clients must know what format the server uses, and if you change the way the server presents its data, you need to change the client to match.

You can help increase the separation between the clients and server if you introduce another layer between the two create to ccreate the three-tier architecture.
