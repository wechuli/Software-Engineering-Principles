## Outline

- Goals of testing
- Reasons why you might not want to remove a bug
- How to prioritize bugs
- Kinds of tests and testing techniques
- Good testing habits
- Methods for estimating number of bugs

It's a software engineering axiom that all nontrivial programs contain bugs. The industry average number of bugs per thousand lines of code is typically estimated at about 15 to 50.

Even though you can't wipe out every bug, you can catch the ones that will be most irritatinf to users. You can reduce the number of high-profile bugs to the point where users see them only rarely. If you program uses a good design, it should also recover from bugs gracefully so that the program doesn't crash.

## Testing Goals

Ideally, you would sit down, write code that perefectly satisifies the requirements and you'd be done. Unfortunately, that rarely happens. More often than not, the first attempt at the software satisfies some but not all the requirements. It may also incorrectly handle situations that weren't specified in the requirements. For example, the code may not work in every possible situation.

That's where testing comes in. Testing lets you study a piece of code to see whether it meets the requirements and whether it works correctly under all circumstances.Usually, the second goal means a method works properly with any set of inputs.

To get a complete picture of how a piece of code performs, you can carry out several different kinds of tests using a variety of techniques. It’s worth knowing that it’s not always worth removing every single bug from a program. Instead the goal is often to reduce the number bugs and their frequency of occurrence so that users can get their jobs done with a minimum of annoyance.

## Reasons Bugs Never Die

Simply put, a bug is a flaw in a program that causes it to produce an incorrect result or to behave unexpectedly. It's not always worth the effort to remove every bug in your program.Removing some bugs is just more trouble than it's worth.The following sections describe some reasons why software developers don’t remove every bug from their applications.

### Diminishing Returns

Finding the first few bugs in a newly written piece of software is relatively easy(and therefore cheap). After a few months of testing, finding bugs may become extremely difficult. At some point, finding the next bug would cost you more than you'll ever earn by selling the software.

### Deadlines

In a just and fair world, software would be released when it was ready. In the real world, however, companies are often driven by deadlines imposed by management, competition, or a marketing department.

You might delay a release to fi x high‐profi le bugs, but if the remaining bugs aren’t too bad, you might be forced to release before you would like.

### Consequences

Sometimes a bug fi x might have undesirable consequences.

### It's Too Soon

If you just released a version of a program, it may be too soon to give the users a new patch to fix a minor bug. User's won't like you if you release new bug fixes every 3 days. As a rule of thumb:

- If a bug is a security flaw, release a patch immediately, even if you just released a patch yesterday.
- If a bug makes users swear at your program more than once a day, release a patch as soon as possible.
- If a bug is annoying enough to make users smirk at your program occasionally, fi x it in a
  minor release (as often as twice a year). Include a huge fanfare about how great you are for
  looking after the users’ needs.
- If a bug is just a nice‐to‐have new feature or a performance improvement, fi x it in the next
  major release (at most once per year). Explain how responsive you are and that the users’
  needs are your number one concern.

Too may releases will annoy users, so you may need to wigh the benefit of any bug patch against the inconveniences.

### Usefulness

Sometimes users come to rely on a particular bug to do something sneaky that you didn;t intend them to do. They won't thank you is you remove their facorite feature, even if it started out as a bug.

    Any sufficiently advanced bug is indistinguishable from a feature.

If the users have adopted a bug and are using it in their favor, formalize it and add it to the application’s requirements. You may extend its behavior to give the users an even better feature and take credit for it.

### Obsolescence

Over time ,s ome features may become less useful. Eventually they may go away entirely. In that case, it may be better to just let the feature die rather than spending a lot of time fixing it.

### It's Not a Bug

Sometimes users think a feature is a bug when actually they just don't understand what the program is supposed to do.

This is really a problem of user education. Sometimes the documentation isn’t correct and sometimes it’s missing entirely. Sometimes the user isn’t willing to read all the way through both paragraphs of documentation and see that the feature is clearly described.

If the documentation is incomplete or unclear, this is a “documentation bug” that you can fix the next time you release a new version of the documentation.

You can greatly decrease this problem by using a good user interface design. If the application groups features logically so users can fi nd them easily, the users won’t complain that a feature is missing when it isn’t. If features are named clearly so it’s obvious what they do, users won’t complain that a feature doesn’t do what they think it’s supposed to do.

### It Never Ends

If you try to fix every bug, you'll never release anything. At some point, you need to stop tesing, cross your fingers, and publish your application. It's almost guaranteed to be imperfect, but hopefully it's better than nothing.

### It's Better Than Nothing

Your application may not be perfect, but hopefully it's better than nothing. In some cases, it may be so much better than nothing that it's worth releasing the application even though it's seriously flawed. This is particularly true if your application is for in-house use.

### Fixing Bugs Is Dangerous

When you fix a bug, there's a chance that you'll fix it incorrectly, so your work doesn't actually help. there's also a chance that you'll introduce one or more new bugs when you fix a bug.

In fact, you're siginifaclty more likely to add a bug to a program when you're fixing code than when you're writing new code from scratch. When you write new code, you understand what you want the code to do and how it should work. When you are fixing code sometime later, you don't have the same level of understanding.

To reduce the problem, you need to study the code thoroughly to try to regain the understanding you originally had.

Finally, whether you fix the bug correctly, other pieces of code may rely on the buggy behavior. When you change the code, you may break other pieces of code that were(at least apparently) working before.

### Which Bugs to Fix

There may be some good reasons not to fix every bug, but in general bugs are bad, so you should remove as many of them as possible. So how do you decide which bugs to fix and which to put in the "fix later" category?

To decide which bugs you should fix, you should use a simple cost/benefit analysis to prioritize them. For each bug, you should evaluate the following factors.

- **Severity** - How painful is the bug for the users? How much work, time, money or other resouces are lost?
- **Work-arounds** - Are there work-arounds?
- **Frequency** - How often does the bug occur?
- **Difficulty** - How hard would it be to fix the bug?
- **Riskiness** - How risky would it be to fix the bug? If the bug is in particularly complex code, fixing it may introduce new bugs.

After you evaluate all the bugs, you can assign priorities. Note that you may want the priorities to change over time.If your next release is a long time away, you can focus on the most severe bugs without work-arounds. If your time is limited, you can focus on the least risky bugs so that you don’t break anything else before the next release.

## Levels of Testing
