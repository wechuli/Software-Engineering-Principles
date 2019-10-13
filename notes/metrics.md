# Metrics

- Grouping defects by importance or task
- Using Ishikawa diagrams to discover root causes of problems
- Defining and using attributes, metrics and indicators
- Understanding the difference between process and

Discuss the recently completed project to determine what you can learn from your recent experiences. You need to analyze the project to see what went well, what went badly and how you can encourage the first and discourage the second in the future.

## Defect Analysis

At a philosophical level ,any time an application doesn't do what it's supposed to, you can consider it is a bug. However, when you're thinking about bugs with an eye toward preventing them in the future, it's helpful to differentiate among different ways the program isn't working correctly.

## Kinds of Bugs

At the highest level, you can group all incorrect features into defects. You can then categorize defects into bugs (code that was written incorrectly) and changes (The code is doing what the specification said to do, but the specification is wrong)

There are several ways to classify defects

### Discoverer

One important way to group defects is by who reported them. Bugs that are found and fixed by programmers are often invisible to the customers. The customers never need to know all the dirty little secretd that wen into building the final application.

In contrast, changes that are requested by customers are obviously visible to the customers.

The worst combination is a bug that is discovered by the customers.

### Severity

This categorization is quite obvious. Assign a severity to each defect and focus on those that are most severe. You can simply assign each the severity Low, Medium or High. Focus on the high severity defects and for each one ask how you could have avoided it, how you could have detected it sooner, and(for customer-discovered defects) how you could have found it before the cusomer did.

### Time Created

You can further categorize defects by when they were created. Defects tend to snowball, so those created earlier in the project usually have greater consequences than those created later.

### Age at Fix

Defects are linke cancer: The longer they go undetected, the greater the potential consequences. Group defects by the length of time they existed before they were detected and fixed. Focus on those that remained in hiding the longest.

### Task Type

Another way to categorize defects is by the type of task you were trying to accomplish when it was created. The types of tasks you should use will depend on the project.

Some typical task categories include:

- Specification
- Design - High‐Level
  ➤ Security
  ➤ User Interface
  ➤ External Interface
  ➤ Database
  ➤ Algorithm
  ➤ Input/Output

➤ Programming

- Tools
  ➤ Security
  ➤ User Interface
  ➤ External Interface
  ➤ Database
  ➤ Algorithm
  ➤ Input/Output

➤ Documentation
➤ Hardware

The previous methods for categorizing defects focus on what's most important. The errors discovered by users, have high severity, were created early, and that remained undiscivered for a long time tend to have the greatest impact, so ther're important.

In contrast, task categories don't identify the most important defects. Istead, they try to group defects by common causes. Defects that were added while performing similar tasks may have similar causes and hopefully similar solutions.

For example, suppose you discover that a lot of defects originated in the specifi cation. In that case,
many of them may have a common cause such as not paying attention to the customer, not studying
the user’s current process enough, or unrealistic customer requests. In that case, you may be able to
fi x a whole bunch of defects in future projects by addressing a single issue. Perhaps if you spend a bit
more time running through use cases with the customers before you fi nalize the specifi cation, you
can avoid some of these defects.

#### Ishikawa Diagrams

To figure out in which category a defect belongs, ask what task was being performed when the defect was created. Often, however, a defect is the end of a sequence of events that was started by some primordial mistake.

Sometime discovering the root cause of a defect can be challenging. One tool that can help is the Ishikiwa diagram. They're also called cause and effect diagrams.

To make an Ishikawa diagram, write the name of the defect you’re trying to analyze (Incorrect
Username/Password Validation) on the right of a sheet of paper. (This is the head of the fi sh.)
Next draw a horizontal arrow pointing to the defect name from left to right. (This is the fish’s backbone.)
Now think of possible causes and contributing factors for the defect. Represent them with angled arrows
leading into the spine. (These are the fi sh’s ribs.) Label each arrow with the cause you identifi ed.
For each of the fi sh’s ribs, think about causes and contributing factors for that rib. Add them, again
with labeled arrows. Continue adding contributing factors to each of the factors you’ve already
listed until you run out of ideas

The exact format of the diagram doesn’t matter too much and there are several variations in style.
The only things that are really consistent among most diagrams are

- The effect or outcome is on the right
- There's a backbone
- Arrows(or lines) lead from causes to intermediate causes or effects
- Arrows(or lines) are labeled

![](ishikawa.PNG)

After you build an Ishikawa diagram for a defect, take a close look at each of the possible causes and decide which ones actually helped cause the defect. Highlight causes that did play a role and cross out those that didn't. If you're not sure about a cause, study it further, possibly adding contributing causes to it.

When you're finished, you should have discovered the root cause of the defect.

## Software Metrics

The defect analysis technique described in the previous sections are more or less qualitative. They help you charcterize defects based on their discoverer, severity and age at time of removal.

In contrast, software metrics give you quantitative measurements of a project. Before you learn what kinds of metrics you can analyze, you should know a few metric-related terms.

An attribute is something you can measure. It could be the number of lines of code, the number of defects etc

A metric is a value that you use to study some aspect of a project. Sometimes a metric is the same as an attribute. For example, you might get useful information about a project from the number of bug reports you have received. Often metrics are calculated values. For example, you may want to look at bug reports per week or bug reports per line of code instead of just the total number of bug reports.

After you have metrics, you study them to see if any of them are good indicators of the project’s future. For example, consider the metric “comments per thousand lines of code (KLOC).” If comments per KLOC is 3, that may be an indicator that the project will be hard to maintain.

You can then do two things with your indicators. First, you can use them to predict the future of your current project.

The second thing you can do with indicators is make strategy improvements for future projects.

In summary:

- Measure relevant attributes
- Use the attributes to derive meaningful metrics
- Use metrics to create indicators
- Use indicators to predict the project's future
- Use indicators to make process improvements

### Using Metrics

Metrics have several possible uses. You can use them to:

- Minimize a schedule
- Reduce the number of defects
- Predict the number of defects that will arise
- Make defect removal easier and faster
- Assess ongoing quality
- Improve finished results
- Improve maintenance
- Make sure a project is on schedule
- Detect risks such as schedule slip, excessive bugs or features that won't work and adjust staffing and work effort to address them

Metrics and indicators are often grouped into two categories depending on how you use them: process metrics and project metrics.

### Process Metrics

Process metrics are designed to measure your organization's development process. You collect them over a long time period for many projects, and then use them to fine-tune the way you do software engineering.

### Project Metrics

Project metrics( which are sometimes called product metrics because they are about a specific product) are intended to measure and track the current project. They let you use past performance to predict future results. Based on your predictions, you can adjust your strategy to improve those results.

You can also use project metrics to set goals

## Things to Measure

The things you can measure on a software project are practically limitless. Fortunately, you need to track only a few metrics to get a good sense of how a project is progressing.

At a high level, there are two kinds of metrics you should track: inputs and outputs. Inputs are the things that you spend on the project.
