# Development

    "A good programmer is someone who always looks both ways before crossing a one-way street"
                                                            - Doug Linder


    "Always code as if the guy who ends up maintaining your code will be a violent psychopath who knows where you live"
                                                            -Martin Golding

Testing often begins before development is completely finished. In fact, it's best to test software early and often. It's widely known that bugs are easiest to find and fix if they're detected soon after they're created, so if possible you should test every method you write as soon as it's finished(sometimes even before it's finished)

## Use The Right Tools

### Hardware

Few things are as frustruting as trying to write software on inadequate hardware. Programmers need fast computers with lots of memory and disk space. A programmer with an underpowered computer or insufficiant memory takes longer to do everything.

### Network

### Development Environment

### Source Code Control

A good source code management system enables you to go back through past versions of the software and see exactly what changes were made and when.

### Profilers

Profilers let you determine what parts of the program use the most time, memory, files or other resources. They can save you a huge amount of time when you are trying to tune an application's performance.

### Static Analysis Tools

Profilers monitor a program as it executes to see how it works. Static analysis tools study code without executing it. They tend to focus on the code's style.

### Testing Tools

Testing tools, particularly automated tools, can make testing a whole lot faster and more reliable.

### Source Code Formatters

Some development environments do a better job of formatting code than others. That formatting makes code easier to read and understand. That in turn reduces the number of bugs in the code and makes finding and fxing bugs easier.

### Refactoring Tools

The term refactoring is programmer-speak for "rearranging code to make it easier to understand, more maintainable, or generally better". Some refactoring tools let you do things like easily define new classes or methods or extract a chunk of code into a new method. Refactoring tools can be particularly useful if you're managing existing code(as opposed to writing new code)

### Training

Training makes programmers more effective and keeps them happy.

## Selecting Algorithms

After low-level design is mostly complete, you should have a good sense of what classes you need and the task those classes need to perform. The next step is writing the code to perform those tasks.

For more complicated problems, the first step is researching possible algorithms. An algorithm is like a recipe for solving a hard programming problem e,g

- Sorting and arranging pieces of data
- Quickly locating items in databases
- Finding optimal paths through street, power, communication or other networks
- Designing networks to provide necessary capacity and redundancy to prevent single points of failure
- Encrypting and decrypting data
- Picking optimal investment strategies
- Findning least cost construction and production strategies

Fortunately, these sorts of algorithms have been extensively studied for years, so you usually don't need to write your own from scratch. You can use the internet and algorithm books to look for an approach that fits your problem.

You'll probably still need to do some work plugging the algorithm into your application, but there's no need for you to reinvent everything from scratch. However, even if you don't need to build an algorithm from the ground up, you should know some of the characteristics that make an algorithm a good choice for you.
The following describe some of the charcteristics:

### Effective

Obviously, an algorithm won't do much good if it doesn't solve your particular problem. If an algorithm doesn't meet your needs exactly, look for an algorithm that does.

If you can’t fi nd an algorithm that fi ts your problem, and you can’t adjust your problem to fi t the available algorithms, then you may need to write your own algorithm or modify an existing one. Complicated algorithms often include some of the most highly studied and optimized code you
will ever encounter, so modifying them can be diffi cult.

### Efficient

To be useful, an algorithm must satisfy your speed, memory, disk space and other requirements.

### Predictable

Some algorithms produce nice, predictable results every time they run. Other algorithms may be less predictable. Some algorithms may not produce the same results every time you run them.

### Simple

Ideally, an algorithm like any other piece of code should be elegantly simple. Simple code is easy to understand and easy to debug. It's easier to modify and it's easier to understand how the algorithm's performance varies for different inputs

### Prepackaged

If you can find an algorithm that is implemented inside your programming language or in a library. use it. There's no need to write, test, debug and maintain your own code if someone else can do it for you.

Prepackaged algorithms also tend to be more thoroughly studied and tested than anything you have time to write. A software vendor may spend hundreds of person‐hours testing code that you would probably write, test, and shove out the door in a few hours. Its results may not always be better than yours, but if there is a problem you can ask the vendor to fi x it instead of spending more time on it
yourself.

## Top-Down Design

If you can't find an algorithm to handle your situation, you need to write some code of your own. Even if you do find an algorithm that can be useful, you'll probably need to write some code to prepare for the algorithm and to process the results.

One useful approach to designing algorithms is top-down design, also called stepwise refinement.In top-down design, you start with a high-level statement of a problem and you break the problem down into more detailed pieces.

Next, you examine the pieces and brak any that are toobig into smaller pieces, You continue breaking pieces into smaller pieces until you have a detailed list of the steps you need to perform to solve the original problem.
As you break a task into smaller pieces, you should be on the lookout for opportunities to save some work. If you notice that you’re performing some chore more than once (perhaps while describing multiple main tasks), you should think about pulling that chore out and putting it in a separate
method.Then all the tasks can use the same method. That not only lets you skip writing the same code a bunch of times, it also lets you invest extra time testing and debugging the common code while still saving time overall.

If the main task's description becomes too long, you should break it into shorter connected tasks. Continue performing rounds of refinement, providing more detail for any steps that aren't painfully obvoius, unitl the instructions are so detailed a fifth-grader could follow them.

## Programming Tips and Tricks

### Be Alert
Writing good code can be difficult. To know if you're writing the code correctly, you need to completely understand what you're trying to do, what the code actually does and what could go wrong. You need to know in what situations the code might execute and how those situations could mess up your carefully laid plan.You need to ask yourself, what if an important fi le is locked, a needed value isn’t found in a parameter table, or if a user can’t remember his password.

Keeping everything straight can be quite a challenge. You can make your life a little easier if you write code only while you're wide awake and alert.

### Write for People, Not the Computer
Probably the most important tip is to write code for people, not for computers. The computer doesn't care whether you use meaningful names for variables, indent your code nicely, use comments or spell words correctly. It doesn't care how clever you are, and it doesn't care if your code produces a correct result.

Debugging and maintaining code is far more difficult and time-consuming than writing code in the first place. The main reason is because you know what you are trying to do when you write code. Later when you're called upon to debug it, you might not remember exactly what the code is supposed to do and what it actually does, so it's harder to fix.

Fixing a bug also has a much higher chance of adding a new bug than writing new code does and for the same reason. When you're debugging, you don't have a clear an understanding of what the code is supposed to do. That makes it much easier to change the code in a way that breaks it.

To make debugging and maintaining code easier, you need to write code that is clear and easy to understand. Hopefully, whoever is eventually forced to track down a bug in your code won’t be a violent psychopath, but you can make that person’s job a lot easier if you remember it’s that person
you’re writing for, not the computer.

### Comment First

Many programmers write the bare minimum of comments they think they can get away with and then rush off to write more code.

One way to write comments that explain what the program is supposed to be doing is to write the comments first. This lets you focus on the intent of the code and not get distracted by whatever code is sitting actually there in front of you. It also means you don't need to revise the comment a dozen times. The code itself might change a dozen times, but the intent of the code better not! If it does, then you didn't do enough planning in the high-level and low-level design phases.


### Write Self-Documenting Code

In addition to writing food comments, you can make the code easier to read if you make the code self-documenting. Use descriptive names for classes, methods, properties, variables and anything else you possibly can.

You can also make your code easier to understand if you don’t use magic numbers. (A magic number is a value that just appears in the code with no explanation. For example, it might represent an error code or database connection status.) Instead of using a magic number, use a named constant that has the same value.

### Keep It Small

Write code in small pieces. Long pieces of code are harder to read. They require you to keep more information in your head at one time. They also require you to remember what was going on at the beginning of the code when you're reading statements much later.

If a piece of code becomes too long, break it into smaller pieces. Exactly how long is "too long" varies depending on what you are doing. Many developers used to break up methods that didn't fit on a one-page printout. A more recent tree-friendly rule of thumb is to break up a method if it won't fit your computer's screen all at one time.

### Stay Focused

Each class should represent a single concept that's intuitively easy to understand. If you can't describe a class in a single sentence, then it's probably trying to do too much, and you should consider splitting it into several related classes.

Just as a class should represent a single intuitive concept, a method should have a single clear purpose. Don't write methods that perform multiple unrelated tasks. Even if two tasks are related, it's often better to put them in separate methods so that you can invoke them separately if necessary.

### Avoid Side Effects

A side effect is an unexpected result of a method call. For example, suppose you write a ValidateLogin method that checks a username and password in the database to see if the combination is valid. Oh, and by the way, it also leaves the application connected to the database. Leaving the database open is a side effect that isn’t obvious from the name of the ValidateLogin method.

Side effects prevent a programmer from completely understanding what the application is doing. Because understanding the code is critical to producing high-quality results, avoid writing methods with side effects.Sometimes, a method may need to perform some action that is secondary to its main purpose, such as opening the database before cheking a username/password pair. There are several ways you can remove the hidden side effects.

First, you can make the side effect explicit in the method’s name. For example, you could call this method OpenDatabaseAndLogin . That’s not an ideal solution because the method isn’t performing one well‐focused task, but it’s better than having unexpected side effects. (Any time you have “And” or “Or” in a method name, you may be trying to make the method dotoo much.)

Second, the ValidateLogin method could close the database before it returns. That removes the hidden side effect; although it may reduce performance because you may want the database to be open for use by other methods.

Third, you could move the database opening code into a new method called OpenDatabase . The program would need to call OpenDatabase separately before it called ValidateLogin , but the process would be easy to understand. 

Fourth, you could create an OpenDatabase method as before and make that method keep track of whether the database was already open. If the database is open, the method wouldn’t open it again. Then you could make every method that needs the database (including ValidateLogin ) call OpenDatabase . Methods such as ValidateLogin would encapsulate the call to OpenDatabase so you wouldn’t need to think about it when you called ValidateLogin . There’s still some extra work going on behind the scenes that you may not know about, but with this approach you don’t need to keep track of whether the database is open or closed.

It may take a little extra work to remove side effects from a method, but it’s worth it to make the code that calls the method easier to understand.

### Validate Results

Murphy's law states, "Anything that can go wrong will go wrong". By that logic, you should always assume that your calculations will fail. Maybe not every single time, but sooner or later they will produce incorrect results.

Sometimes, the input data will be wrong. It may be missing or come in an incorrect format. Other times your calculations will be flawed. Values may not be correctly calculated or the results may be formatted incorrectly.

To catch these problems as soon as possible, you should add validation code to your methods. The calidation code should look for trouble all over the place. It should examine the input data to make sure it's correct, and it should verify that the result your code produces is right. It can even verify that calculations are proceeding correctly in the middle of the calculation.

The main tool for validating code is the assertion. An assertion is a statement about the program and its data that is supposed to be true. If it isn't, the assertion throws an exception to tell you that something is wrong.

        The term exception is programmer‐speak for an unexpected error caused by the
    code. Exceptions can be caused by all sorts of situations such as trying to open
a fi le that doesn’t exist, trying to open a fi le that is locked by another program,
performing an arithmetic calculation that divides by zero, using up all the
computer’s memory, or trying to use an object that doesn’t exist.
When an exception occurs, the program’s execution is interrupted. If you have
an error handler in place, it can examine the exception information to fi gure out
what went wrong and it can try to fi x things. For example, it might tell the user
to close the application that has a fi le locked and then it could try to open the
fi le again.
If no error handler is ready to catch the exception, the program crashes.

One type of assertion that can sometimes be useful is an invariant. an invariant is a state of the program and its data that should remain unchanged over some period of time.

Assertions and other validation code, can make it easy to find bugs right after they are written when they're easiest to fix.

However, bugs do occur, so obviously they must be lurking in some of the code that was just written. If only you could convince programmers to add validation code to their methods, you might catch the bugs before they become established.
One way to encourage programmers to write validation code is to have them write it before writing the rest of a method’s code. (This is similar to the way you can often get better comments if you write them before you write the code.) Writing the validation code fi rst ensures that it happens.

This also has the advantage that you probably don’t yet know exactly how the fi nal code will work. You don’t have it all in your head whispering seductively, “You did a great job writing me. There’s really no need to validate the results.” You also don’t have preconceptions about how the code works, so you won’t be infl uenced in how you write the validation code. You can look for incorrectresults without making assumptions about where errors are impossible.