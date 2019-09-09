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

## Ishikawa Diagrams