# Deployment

## Scope

A project's scope can range from a small tool you wrote for your own use, to in-house business software that will be used by hundreds or thousands of users. In addition to the number of users, scope includes the size of the application. It includes the amount of data involved, the number of external systems that are affected and the sheer quantity of code.

Before you begin deployment planning, you should consider the scope of the deployment and plan accordingly.

## The Plan

When the inevitable emergency occurs, how well you recover depends largely on how thoroughly you planned for unexpected situations. If you have a backup plan ready to go, you may work around the problem and keep moving forward. If you don't have a backup plan, you may need to stop the deployment and try again later.

To start deployment planning, list the steps that you hope to follow. Descibe each step in detail as it is supposed to work.

Next, for every step, list the ways that step could fail. Then describe the actions that you will take is one of those failures occurs. Describe work-arounds or alternative approaches that you could use. This part of planning can be extremely hard. It's not always easy to think of work-arounds for every possible disaster.

After you've worked through all the plan's desired steps and anticipated as many problems as possible, write a rollback plan that lets you undo everything you've done. Be sure you can restore any other applications that you've updated and any data that you've converted for the new system.

## Cutover

Cutover is the process of moving users to the new application. There are several ways you can manage cutover. For some applications, you can just post the new version on the Internet and let users grab it. For other projects, you may be able to email a new version to users, or you may be able to just install the new syste, on users' computers.

During the setup time, the users may be unable to do their jobs. To minimize disruption, it’s important that the whole process go as smoothly as possible. The following sections describe four ways you can make life easier for all concerned: staged deployment, gradual cutover, incremental deployment, and parallel testing.

### Staged Deployment

If you can't reduce the impact of catastrophic failures, you can sometimes reduce their likelihood by using staged deployment. In staged deployment, you build a staging area, a fully functional environment where you can practice deployment until you've worked out all the kinks.

After you have the installation working smoothly, you can test the new application in an environment that's more realistic than the one used by the developers. You can use the staging area to find and fix a few final bugs before you inflict them on the users.

You still need a deployment plan in case something unexpected goes wrong. Just because everything works flawlessly in the staging environment doesn't mean it will on the user's machines.

### Gradual Cutover

In gradual cutover, you install the new application for some users while other users continue working with their existing system. You move one user to the new application and thoroughly test it.

When you're sure everything is working well, you move a second user to the new system. When that user is up and running, you install a third user, then a fourth, and so on until everyone is running the new application.

When you're sure everything is working well, you move a second user to the new system. When that user is up and running, you install a third user, then a fourth and so on until everyone is running the new application.

The advantage to this approach is that you don't destroy every user's productivity if something goes wrong. The first few guinea pigs may suffer a bit, but the others will continue with business as usual until you work out any tangles in the installation procedure. Hopefully, you'll stumble across most of the unexpected problems with the first couple of users and deployment will be effortless for most of the others.

One big drawback to this approach is that the system is schizophrenic during deployment. Some users are using one system while others are doing something different. Depending on the application, that can be hard to manage. You may need to write extra tools to keep the two groups logically separated, or you may need to impose temporary rules of operation on the users.

### Incremental Deployment

In incremental deployment, you release the new system's features to the users gradually. First, you install one tool (possibly using staged deployment or gradual cutover to ease the pain). After the users are used to the new tool, you give them the next tool.

This method doesn't work well with large monolithic applications because you usually can't install just part of such a system.

### Parallel Testing

Depending on how complicated the new system is, you might want to run in parallel for a while to shake the bugs out. For example, if you have enough users, you could have a handful of them start using the system in parallel with the old one. They would use the new system to do their jobs just as if the new system were fully deployed.

Meanwhile, another set of users would continue using the old system.The old system is the one that actually counts. The new one is used only to see what would happen if it were already installed.

After a few days, weeks, or however long it takes to give you enough confi dence in the new system, you start migrating the other users to the new system. You can ease the process by using staged deployment and gradual cutover if you like.

## Deployment Tasks

The tasks you need to perform for a successful deployment depend on the application you're installing.

The following list itemizes some of the things you might need to deal with for a large deployment

- **Physical environment** - These are physical things that the users need.
- **Hardware** - includes newtork hardware, printers, scanners,disk farm,database hardware, hard drives etc
- **Documentation** - This can include some combination of physical and online documentation. It might include training materials, user manuals, help guides and cheat sheets listing common commands
- **Training** - If the application is complicated or very different from what users currently have installed, you may need to train the users.
- **Database**-Most nontrivial applications include some sort of database. Depending on the
  database, you may need to install database software on one or more central database servers
  and on the users’ computers. You may also want extra hardware and software to provide
  extra data security features such as backups, shadowing, and mirroring.
- **Other people's software** - This is software that you didn’t write. It includes systems that
  interact with your application (purchasing systems, web services, fi le management tools,
  cloud services, and printing and scanning tools) and other software that users need to be productive (e‐mail, chat, browsers, search engines, trouble‐shooting databases, and word
  processors). Plus, of course, the operating system.
- **Your Software** - This is the application you’ve built. It includes the application itself, plus
  any extra tools you’ve created. It also includes monitoring and testing tools that let you make
  sure the application is working correctly.

## Deployment Mistakes

The basic steps for successful deployment are 1. make a plan 2. anticipate mistakes and 3. work through the plan overcoming obstacles as they arise. If something goes wrong and you don't have an easy fix, rollback whatever you've done, study the problem and try again later. You can reduce the inconvenience for users by using staged deployment, gradual cutover , incremental deployment and parallel testing.

The following list summarizes some of the easiest ways to torpedo an otherwise viable project:

- **Assume everything will work** - This may seem like a rookie’s mistake, but many people assume their deployment plan will just magically work. Maybe you’ll get lucky and that will be true, but you should probably assume it won’t.
- **Have no rollback plan** - Rolling a deployment back can be a real hassle, but it’s usually better than living with whatever damage you do during a failed deployment.
- **Allow insufficient time** - If everything goes smoothly, you won’t need much time, but when something goes wrong, all bets are off. A deployment that should take hours could take days or even weeks. Allow extra time for unexpected problems. Then hedge your bets by scheduling the end of deployment on a Friday so that you can work into the weekend if the plan goes off the rails.
- **Don't know when to surrender** - It’s easy to work around one or two small issues that don’t play out as expected, but how do you know when to stop? If you keep pushing through (or around) little issues (and sometimes big ones), eventually all the compromises add up to give you a terrible result. Defi ne conditions under which you’ll fold and try again later. For example, you might quit after 4 hours or after three things go wrong. Or you might use a point system with 1 point for a trivial change, 2 points for a small work-around, and 5 points if you can’t get something to work. When you get to 5 points, quit for the day.
- **Skip staging** - Staging can be time‐consuming and expensive, particularly if you need to install new hardware and software. However, for a complicated deployment, staging is crucial. It lets you work out all the deployment glitches so that you don’t need to completely trash the users’ computers.
- **Install lots of updates all at once** - It’s tempting to install a lot of updates at the same time so that you don’t need to inconvenience the users repeatedly. Unfortunately, the more things you try to do at once, the more likely it is you’ll run into problems. Limit the number of things you try to deploy all at once. Save the rest for a later deployment.
- **Use an unstable environment** - If the tools you use don’t work together consistently, then you have other problems you should fi x before you start a new deployment. Sometimes fi nding the right combination of tools that can work together can be challenging. Adding a new application will only make things worse.
- **Set an early point of no return** - If you explicitly set a point of no return, you don’t need to figure out how to roll back any changes after that point. Unfortunately, you don’t always know how bad things might get near the end of the deployment. The last installation task could be a total disaster that takes you days to fi gure out. You should set the point of no return as late as possible in the deployment schedule so that you can retreat whenever necessary. Even better, don’t have a point of no return!
