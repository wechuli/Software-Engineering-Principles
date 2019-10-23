# Maintenance

Maintenance may not always be a lot of fun, but it's important because maintenance is often relatively expensive. Often maintenance accounts for 75 percent of a project's total cost

To safely modify old code, you need to spend time studying it. If you don't dig into the code and make sure you understand how it works, you're just as likely to add bugs to the code as remove them. After you make your changes, you need to test them to verigy that they work. You also need to thoroughly test the rest of the application to make sure your changes didn't break anything.

You can reduce maintanance costs by doing a good jon when you write the initial code. For example, develop simple but flexible designs, use good programming practices, insert comments to make the code easy to read and provide documentation for future generations of maintenance programmers can figure out what you were thinking when you wrote the code.

## Task Categories

At a high level, the tasks that go into long-term maintenance is roughly the sane as those that go into initial development. You gather requirements, make designs, write some code, test the code and deploy a new version. During maintenance, you tend to spend more time on bug fixes and feature enhancements than on writing completely new code.

Generally, maintenance tasks are grouped into the following four categories:

- **Perfective** - Improving existing features and adding new ones
- **Adaptive** - Modifying the application to meet changes in the application's environment
- **Corrective** - Fixing bugs
- **Preventive** - Restructuring the code to make it more maintenable

The relative effort spent on each of these categories depends on the project.

### Perfective Tasks

This is often the biggest part of maintenance. Users will definitely want tweaks, adjustments and improvements Users may also want completely new features that weren't in the original specification. The tasks that fall into the perfective category tend to be one of two sorts: feature improvments and new features.

#### Feature Improvements

Feature improvements involve modifying existing code, so in some ways they're similar to bug fixes. You need to carefully study the existing code so that you're sure you understand what it does and how it does it. You need to plan the modifications you're going to make. Don't just start ripping out old code and typing in new. When you're reasonable certain theat your changes won't break things, you can make your modifications.

Remember that changing old code is more likely to introduce bugs than writing new code, so you need to test your changes thoroughly.

#### New Features

Adding new features to an application is a lot like writing code for the initial application, so you should follow the same steps:

1. Make a specification explaining what you will do
2. Get the users sign off om the specification so that they agree that you're doing the right thing
3. Make high-level designs that provide a framework for development. It should keep pieces lossley coupled and provide enough flexinility to do what you need it to do.
4. Create low-level designs that indicate how to create the features you need
5. Write the code while following good programming practices so that you don't end up with a tangled web of mysterious and uncommented code
6. Test thoroughly to flush out bugs as quickly as possible
7. Use good practices (such as staging and gradual cutover) to deploy the new version of the program.

### Adaptive Tasks

Adapative tasks help keep the application usable when the things around it change.If the users’ hardware, operating system (OS), database, other tools (such as spreadsheets or reporting tools), network security, or other pieces of the users’ environment change,it could break your application,so you have to fix it.

Unfortunately, the tools on which your application relies may also be interrelated, so changes to one may affect the others. You can take a couple approaches to make these scenarios less likely. First, you can minimize the use of external tools.

Second, you can just ignore new releases of operating systems, databases, toolkits and any other external tools that you use.

These days, many products install new releases automatically, so its harder to avoid having some product upgrade itself and break something.

### Corrective Tasks

Corrective tasks are simply bug fixes.

To fix a bug; find it, study the code so that you're sure you understand it, fix the bug, test and release a new version of the application with the bug fixed.

One of the worst ways to fail to fix a bug is to lose track of it. To avoid losing bugs, you need a bug tracking system.
You can assign a state to each bug to keep track of its status within the system. The following list describes typical states that a bug tracking system might use:

- **New** - The bug just arrived and has not yet been assigned to anyone
- **Assigned** - The bug has been assigned to someone to fix
- **Reproduced** - The bug has been reproduced by a team member. The bug's descrition includes instructions for reproducing the bug.
- **Cannot Reproduce** - A team memeber has examined the program and can't make the bug occur.
- **Pending** - A request for more information has been sent to the customer who reported the bug.
- **Fixed** - The bug has been fixed but not tested yet.
- **Tested** - the fix has been thoroughly tested and the bug us verified as gone
- **Deferred** - The bug should not be fixed, or atleast not yet.
- **Closed** - The bug has been either fixed, deferred or otherwise abandoned
- **Reopened** - The bug reappeared after neing closed. The bug should probably be treated as if it were a new bug.

Bug tracking applications typically come with an assortment of features. For example, they may reproduce reports showing bugs in various states, bugs cleared over a period of time, bugs assined to a particular developer. Some can notify developers via e-mail or some other method when bugs are assinged to them. Some systems can even automaticlly mode bugs from one state to another.

Priority is also key. Some bugs are more important than others. If one bug makes the application crash every day or two and a second is more benign, the first bug probablt deserves higher priority.

### Preventive Tasks

Preventive tasks involve restructuring the code to make it easier to debug and maintain in the future aka refactoring.

Despite the dangers, there are several reasons why you might want to refactor code and a few reasons not to. The following sections describe some of the most important of those reasons'

#### Clarification

If a piece of code is confusing, you should add comments to it explaining how it works. You should do that as you're writing code or immediatelt after you finish writing it, while the code is still fresh in your mind. Later, when people need to read the code (including you after you've forgotten how it works), they have a chance of understandinf how the code works.

To write good comments, you need to spend a lot of time studying the code carefully so that you're sure you understand how it works.

#### Code Reuse

Sometimes when you're modifying code, you realize you've done something similar before. Instead of repeating yourself, it may make more sense to extract the common code into a new class or method that you can call from multiple locations. Then when you need to do the same thing a thirdm forth time, you won't need to write the same code all over again.

The real benefit of code reuse it in maintaining the code later.

The DRY(don't repeat yourself) principle says you should extract common code any time you repeat yourself.
