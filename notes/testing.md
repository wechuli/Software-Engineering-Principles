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

Bugs are easiests to fix if you catch them as soon as possible. After a bug has been in the code for a while, you forget how the code is supposed to work. That means you'll need to spend extra time studying the code so that you don't break anything.

In order to catch bugs as soon as possible, you can use several levels of testing. These range from tightly focusses unit testing that examines the smallest possible pieces of code, to system and acceptance testing that exercises the system as a whole.

### Unit Testing

A unit test verifies the correctness of a spcific piece of code. As soon as you finish writing a piece of code, you should test it. Test it as thoroughly as possible because it will get harder to fix later.\

Usually unit tests apply to methods. You write a method and then test it. If you can, you may even want to test parts of methods. That lets you catch bugs minutes or even seconds after they hatch.

If you’re using an object‐oriented programming language, be sure to test code that doesn’t act like a normal method. For example, be sure to test constructors (which execute when you make a new object), destructors (which execute when you destroy an object), and property accessors (which execute when the program gets or sets a property’s value).

You can often do a better job on a method's unit tests if you write them before you write the method. That way, you won't know what assumptions the code makes, so you won't make the same assumptions when you write the tests.

You may also want to add more test cases after you write the code, so you can look for situations that the code might not handle correctly.

Typically a test is another piece of code that invokes the code you are trying to test and then validates the result. After you write the tests and use them to verify that your new code works, you should save the test code for later use. Sometimes you may want to incorporate some or all the unit tests in regression testing.

### Integration Testing

After you write a chunk of code and use unit tests to verify that it works, it's time to integrate it into the existing codebase. An integration test verifies that the new method works and plays well with others. It checks that existing code calls the new method correctly, and that the new method can call other methods correctly.

Integration typically focuses on the new code and other pieces of code that interact with it, but it should spend some time verifying that the new code didn't mess up anything that seems unrelated.

**Regression testing** is used to test the program's entire functionaility to see if anything changed when you added new code to the project. These tests look for ways the program may have "regressed" to a less useful version with missing or damaged features.

Ideally, when you finish unit testing a piece of code, you would then perform integration testing to make sure it fits in where it should and that it didn't break anything obvious. Then you perform regression testing to see if it broke something non-obvious.

Unfortunately, performing regression testing on a large project can take a lot of time, so developers often postpone regression testing until a signifi cant amount of code has been added or modified.Then they run the regression tests. Of course, at that point there may be a lot of bugs and it may be hard to fi gure out which change caused which bug. Some of the “new” code may also not be all that new, so some of the bugs may be a bit older and therefore harder to fi x.To fix bugs as quickly as possible, you need to perform regression testing as often as possible.

### Automated Testing

You might not have time to run through every test every day. Automated testing tools let you define tests and the results they should produce. After running a test, the testing tool can compare the results it got with expected results. Some tools can even compare images to see if a result is correct.

Some tesing tools can run load tests that simulate a lot of users all running simultaneously to measure performance. For example, load tests can tell if too may users trying to access the same database will cause problems in your final release.

### Component Interface Testing

Component interface testing studies the interactions between components. This is a bit like regression testing in the sense that both examine the application as a whole to look for trouble, but component interface testing focuses on component interactions.

A common strategy for component interface testing is to think of the interactions between components as one component sending a message(a request or a response) to another. You can then make each component record its interactions(plus a timestamp) in a file. To test the component interfaces, you exercise the system and then review the timeline of recorded events to see if everything makes sense.

Planning ahead of time for component interface testing can also help with the application's design. thinking in terms of loggable messages passed between components helps keep the components decoupled and gives them a clearer separation. That makes them easier to implement and test separately.

### System Testing

System testing is an end-to-end run-through of the whole system. Ideally, a system test exercises every part of the system to discover as many bugs as possible.

A thorough system test may need to explore many possible paths of interaction with the application. Unfortunately, even simple programs usually contain a practically unlimited number of possible paths of interaction. In the end, you'll probably have to test the most common and most important scenarios, and leave some combinations untested.

### Acceptance Testing

The goal of acceptance testinf is to determine whether the finished application meets the customer's requirements. Normally, a user or other customer representative sits down with the application and runs through all the user cases you identified during the requirements gathering phase to make sure everything works as advertised.

Acceptance testing is usually straightforward; although, depending on the nu,ber of use cases, it can take a long time.

One mistake developers sometimes make is waiting until the application is finished before starting acceptance testing. You do need to perform acceptance testing then, but if that’s the first time the customer sees the application, there may be problems. Customers may decide that their interpretation of a use case is different from yours. Or they may decide that what they need is different from what they thought they needed during requirements gathering.

In those cases, you’re much better off if you do a quick run‐through of each use case as soon as the application can handle it. Then if you need to change the requirements, you can do it while there’s still some time left in the development schedule and not at the end of the project when all of the programmers have scheduled overseas vacations.

### Other Testing Categories

Unit test, integration test, component interface test and system test categorize tests based on their scale with unit test being at the smallest scale and system test including the entire application.
An acceptance test differs from a system test in the point of view of the tester. A system tester is typically a developer, whereas an acceptance tester is a customer representative.

The following list summarizes other categories of testing that differ in their scope, focus, or point of view:

- **Accessibility test** - Tests the application for accessibility by those with visual, hearing, or
  other impairments.
- **Alpha tes**- First round testing by selected customers or independent testers. Alpha tests usually uncover lots of bugs and defects, so they generally aren’t open to a huge number of users because that might ruin your reputation for building good software.
- **Beta test** - Second round testing after alpha test. Generally, you shouldn’t give users beta versions until the application is quite solid or you might damage your reputation for building good software. Sometimes, beta tests are used as a sneaky form of a limited trial to build excitement for a new release in the user community.
- **Compatibility test**- Focuses on compatibility with different environments such as computers running older operating system versions. Also checks compatibility with older versions of the application’s fi les, databases, and other saved data.
- **Functional test** - Deals with features the application provides. These are generally listed in
  the requirements.
- **Destructive test** - Makes the application fail so that you can study its behavior when the worst happens. (Obviously, if you have good backups, you won’t actually destroy the code. You’ll destroy the application’s performance.)
- **Installation test** - Makes sure you can successfully install the system on a fresh computer.
- **Internationalization test** - Tests the application on computers localized for different parts of the world. This should be carried out by people who are natives of the locales.
- **Nonfunctional test** - Studies application characteristics that aren’t related to specifi c functions the users will perform. For example, these tests might check performance under a heavy user load, with limited memory, or with missing network connections. These often identify minimal requirements.
- **Performance test** - Studies the application’s performance under various conditions such as normal usage, heavy user load, limited resources (such as disk space), and time of day. Records metrics such as the number of records processed per hour under different conditions.
- **Security test** - Studies the application’s security. This includes security of the login process,
  communications, and data.
- **Usability test** - Determines whether the user interface is intuitive and easy to use.

## Testing Techniques

The following sections describe some approaches to designing tests to find as many bugs as possible.

### Exhaustive Testing

In some cases, you may be able to test a method with every possible input. This sort of exhaustive testing conclusively proves that a method works correctly under all circumstances, so it's the best you can possibly do. Unfortunately, most methods take too many combinations of input parameters for you to exhaustively try them all.

Because most methods take too many possible inputs, exhaustive testing won't work most of the time. In those cases, you need to turn to one of the following methods.

### Black-Box Testing

In black-box testing, you pretend the method is a black box that you can;t peek inside. You know what is it supposed to do but you have no idea how it works. You then throw all sorts of inputs at the method to see what it does.

You can start black-box testing by sending it a bunch of random inputs. Remember that you need to perform these tests only occasionally, not every time the program runs, so you can test a lost of random values.

Even if you don't know how the method works, you can try to guess values that might mess it up. Typically ,those involve special values like 0 for numbers and blank for strings. They may also include the largest and smallest possible values. For strings, that might mean a string that's all blanks or all ~ characters.

If a method takes a variable number of inputs, make sure it can handle 0 inputs and a really large number of inputs. If it takes an array or list as aparameter, see what it does if the array or list os empty or missing.

### White-Box Testing

In white-box testing, you get to know how the method does its work. You then use your extra knowledge to design tests to try to make the method crash and burn.

White-box testing has the advantage that you know how the method works, so you can try to pick particularly difficult test cases. Unfortunately, it has the disadvantage that you know how the method works, so you might skip some tests cases that you assume work.

Use white-box testing to create tests you know will be troublesome, but don't skip tests that you "know" the method can handle.

### Gray-Box Testing

Gray-box testing is a combination of a white-box and black-box testing. Here you know some but not all the internals of the method you are testing. Your partial knowledge of the methods lets you design specific tests to attack it.

## Testing Habits

### Test and Debug When Alert

You should test and debug when you are alert. Then when something goes wrong, you'll be more likelt to understand what the program is supposed to be doing, what it is actually doing and how to fix it. Debugging while tired is a good way to add new bugs to the program.

### Test You Own Code

Before you check your code in, test it yourself. This is the last chance you have to find your own bugs before someone else does.

### Have SomeOne Else Test Your Code

It's important to test your own code, but you're too close to your code to be objective. You have assumptions about how it works that unconscously influence the tests you perform. To find as many bugs as possible, you also need someone with a fresh perspective to test it.

Mistakes happen all the time, particularly in software development. It's important to thank the tester for pointing out this flaw, fix it and move on with no hard feelings.

#### The Rules of Egoless Programming

1. Understand and accept that you will make mistakes. Everyone makes mistakes. Try to avoid mistakes,
   but realize that they will occur anyway. No one else programs without any mistakes, so why should you?
2. You are not your code. Just because you wrote a piece of flawed code, that doesn't make you a bad person. Don't take the bug home with you.
3. No matter how much “karate” you know, someone else will always know more. Even the greatest programmers of all time sometimes learn from others.
4. Don't rewrite code without consultation. By all means fix bugs, but don’t rewrite sections of code without consulting with your team. Bulk rewrites should be performed only for good reasons (like replacing a buggy section of
   code or rearranging code so that it can be broken up into separate methods), not because you don’t like someone’s indentation or variable names. If it ain’t broke, don’t fi x it.
5. Treat people who know less than you with respect, deference and oatience.Even you started out as a programming novice. You made simple mistakes, did things the hard way because you didn’t know better, and asked naive questions
   (if you were smart enough to ask questions). Be patient and don’t reinforce the stereotype that good programmers are all prima donnas
6. The only constant in the world is change. After a while, programmers tend to become comfortable with what they know. Unfortunately, change happens anyway whether you like is or not. Embrace change and see of it van work in your favor.
7. The only true authority stems from knowledge, not from position.Don’t use your position (as lead developer, senior architect, or even corporate vice president) to force your point of view down others’ throats. Base your
   decisions on facts and let the facts speak for you.
8. Fight for what you believe, but gracefully accept defeat. Programming tasks rarely have a single unambigous solution. There’s always more than one way to tackle a problem. If the group doesn’t decide to take your
   approach, don’t worry about it. If the result is good enough, then it’s good enough.
9. Don't be "the guy in the room". Sometimes you may need to close your dooe and bang out some code, but don't go into hibernation. Stay engaged with the other developers so you can collaborate with them effectively.
10. Critique code instead of people - be kind to the code, not to the code.


### Fix Your Own Bugs