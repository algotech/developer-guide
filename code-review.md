# Code review

A guide for reviewing code and having your code reviewed.
We have to accept that many programming decisions are opinions.
Discuss tradeoffs, and reach a resolution quickly.

 - [When having your code reviewed](#when-having-your-code-reviewed)
 - [When reviewing code](#when-reviewing-code)
 - [Code review checklist](#code-review-checklist)

### When having your code reviewed

 - Be grateful for the reviewer's suggestions.
 - Don't take it personally. The review is of the code, not you!
 - Assume the best intention from the reviewer's comments.
 - Push commits based on earlier rounds of feedback as isolated
 commits to the branch. Do not squash until the branch is ready to merge.
 Reviewers should be able to read individual updates based on their earlier feedback.
 - Seek to understand the reviewer's perspective.
 - Try to respond to every comment.

### When reviewing code

 - Understand why the change is necessary (you should at least read the ticket).
 - Identify ways to simplify the code while still solving the problem.
 - Seek to understand the author's perspective.
 - Ask good questions; don't make demands.
 - Offer alternative implementations, but assume the author already considered them.

### Code review checklist

This code review checklist helps the code reviewers and software developers
(during self code review) to gain expertise in the code review process.

#### Architectural

 - Is all the code easy to understand?
 - Is there any duplicate code?
 - Is the code as modular as possible?
 - Can any of the code be replaced with library functions?
 - Is most of the code in helpers/services/managers/repositories?
 - Are there any missing updates to the documentation/readme files?
 - Are all the necessary tests created according to the project guidelines?
 
#### Security

 - Are all data inputs checked for the correct type, length, format and range?
 - Are invalid parameter values handled?
 - Are all data inputs validated against security threats such as SQL injections
 and Cross Site Scripting (XSS)?

#### Coding

 - Do all the varialbes say what they are for and not what data type they have?
 - Do all the methods have a clear name for what they are going to do?
 - Are there any hardcoded string/integer values?
 - Is there any code ownership comment (like `Created by X`) in the code? We use Git for that.
