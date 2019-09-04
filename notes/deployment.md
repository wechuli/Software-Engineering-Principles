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
