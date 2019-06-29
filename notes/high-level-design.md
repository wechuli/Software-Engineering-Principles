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