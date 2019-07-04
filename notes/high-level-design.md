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

You can help increase the separation between the clients and server if you introduce another layer between the two create to ccreate the three-tier architecture. In a three-tier architecture, the middle tier provides insulation between the clients and server. The separation provided by the middle tier lets different teams work on the client and server without interfering with each other roo much. In addition to providing separation, a middle tier can perform other actions that make the data easier to use by the client and server.

Sometimes, the client tier is called the presentation tier (because it presents information to the user); the middle tier is called the logic tier (because it contains business logic such as aggregating data for the presentation tier); and the third tier is called the data tier (particularly if all it does is provide data)

You can define other multitier architectures (or N-tier architectures) that use more than three tiers if that would be helpful. For example, a data tier might store the data, a second tier might calculate aggregates and perform other calculations on the data, a third tier might use artificial intelligence techniques to make recommendations based on the second tier's data, and a fourth tier would be a presentation tier that lets users see the results.

Multitier architectures are a best practice, largely because of the separation they provide between the client and server layers. Most applications don't use more than three tiers.

### 3. Component-Based

In component-based software engineering(CBSE), you regard the system as a collection of loosely coupled components that provide services for each other. A component-based architecture decouples the pieces of code much as a multitier architecture does, but the pieces are all contained within the same executable program, so they communicate directly instead of across a network.

### 4. Service-Oriented

A service-oriented architecture(SOA) is simila to a component-based architecture except the pieces are implemented as services. A service is a self-contained program that runs on its own and provides some kind of service for its clients. Sometimes, services are implemented as web services. Those are simply programs that satisfy certain standards so they are easy to invoke over the Internet.

### 5. Data-Centric

Data-centric or database-centric architectures come in a variety of flavors that all use data in some central way.

- Storing data in a relational database system. This is so common that it's easy to think of as a simple technique for use in other architectures rather than an architecture of its own.
- Using tables instead of hard-wired code to control the application.
- Using stored procedures inside the database to perdorm calculations and implement business logic. This can be a lot like putting a middle tier inside the database.

### 5. Event-Driven

In an event-driven architecture (EDA), various parts of the system respond to events as they occur.

### 6. Rule-Based

A rule-based architecture uses a collection of rules to decide what to do next. These systems are sometimes called expert systems or knowledge-based systems.Rule-based systems work well if you can identify the rules necessary to get the job done. Sometimes, you can build good rules even for complicated systems; although that can be a lot of work.

Rule-based systems don't work well if the problem is poorly defined so you can't figure out what rules to use. They also have trouble handling unexpected situations.

Rule-based systems are great for handling common simple scenarios, but when they encounter anything unexpected they're quite useless.

### 7. Distributed

In a distributed architecture, different parts of the application run on difeerent processors and may run at the same time. The processors could be on different computers scattered across the network, or they could be different cores on a single computer. Service-oriented and multitier architectures are often distributed, with different parts of the system running on different computers. Component-oriented architectures may also be distributed, with different components running on different cores on the same computer.
In general, distributed applications can be extremely confusing and hard to debug. A distributed architecture can improve performance as long as you don't run a foul of race conditions and other potential problems.

### 8. Mix and Match

An application doesn't need to stick with a single architecture. Different pieces of the application might use different design approaches.

## Reports

Almost any nontrivial software project can use some kinds of repots. As in the case with high-level user interface design, you don't need to specify every detail for every report here. Try to decide which reports you'll need and leave the details for low-level design and inmplementation.

## Other Outputs

In addition to normal reports, you should consider other kinds of outputs that the application might create. The application could generate printouts, web pages, data files, image files etc.

## Databases

Database design is an important part of most applications. The first part of database design is to decide what kind of database the program will need.You need to specify whether the application will store data in text fi les, XML fi les, a full‐fl edged relational database, or something more exotic such as a temporal database or object store.

If you decide to use an external database, you should specify the database product that you will use. If you use a relational database, you can sketch out the tables it contains and their relationships during high-level design.Later you cn provide more details such as the specific fields in each table and the fields that make up the keys linking the tables.

Often the tables in the database correspond to classes that you need to build in the code.At this point, it makes sense to write down any important classes you define. Use good database design practices to ensure that the database is properly normalized.

Meanwhile there are 3 common database-specific issues that you should address during high-level design: audit trails, user access, and database maintenance:

### Audit Trails

An audit trail keeps track of each user who modifies(and in some applicaions views) a specific record. Auditing can be as simple as creating a history table that records a user's name, a link to the record that was modified, and the date when the change occurred. Some database products can even create audit trails for you. A fancier version might store copies of the original data in each table when its data is modified.

Later, you can compare the customer's records over time to build an audit trail that re-creates the exact sequence of changes made for that customer.

### User Access

Many applications also need to provide different levels of access to different kinds of data. One way to handle access is to build a table listing the users and the privileges they should be given. The program can then disable or remove the buttons and menu items that a particular user shouldn't be allowed to use.

Many databases can also restrict access to tables or even specific columns in tables

### Database Maintenance

Over time, a database becomes disorganized. Every now and then, you need to reorganize so that you can find things efficiently.If you use audit trails and the records require a lot of changes, the database will start to fi ll up with old versions of records that have been modifi ed. Even if you don’t use audit trails, over time the database can become cluttered with outdated records.

In that case, you may want to move some of the older data to long‐term storage to keep the main database lean and responsive. Depending on the application, you may also need to design a way to retrieve the old data if you decide you want it back later.

You can move the older data into a data warehouse , a secondary database that holds older data for analysis. In some applications, you may want to analyze the data and store modifi ed or aggregated forms in the warehouse instead of keeping every outdated record.

Removing old data from a database can help keep it responsive, but a lot of changes to the data can make the database’s indexes ineffi cient and that can hurt performance. For that reason, you may need to periodically re‐index key tables or run database tuning software to restore peak
performance. Finally, you should design a database backup and recovery scheme.

## Configuration Data

You can reduce your workload if you provide configuration screens so that users can fine-tune the application without making you write new code.
Store parameters to algorithms, key amounts, and important durations in the database or in confi guration files. Make sure that only the right users can modify the parameters. In many applications, only managers should change these values.

## Data Flows and States

Many applications use data that flows among different processes. You can also think of a piece of data such as a customer order as moving through a sequence of states. The states often correspond to the process in the related data flow. These kinds of diagrams elp describe the system and the way processes interact with the data.

## Training
Although it may not be time to start writing training materials, it's never too early to think about them. The details of the system will probably change a lot between high-level design and final installation, but you can at least think about how you want training to work.

# UML