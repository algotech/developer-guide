# coding-standards

## Git

### The art of committing

 - Commit content
   - A logically connected change
   - Must not fail a build
   - Break up every work into small tasks
     - no more than few hours of work per commit
   - Isolate meaningless commits
     - The golden rule is to avoid meaningless commits
     - However, sometimes, you need to commit something that is not a real implementation
     - Only a cleanup, such as deleting old comments, formatting, rearrangement, and so on
     - In this cases, it is better to isolate this kind of code change in separate commits
 - Commit message
   - Should clearly specify the essence of the commit
   - Describe the change (what the code does), not what you have done
   - Every commit is a sentence in the repository history
   - Always start with a capital letter and finish with a period
   - Use the imperative present tense (fix, add, implement) describing the change in a small subject sentence
   - Very good examples:
     1. Send an email to the user with a link to renew the password.
     2. Add the newsletter signup in homepage.
     3. Fix default date issue in the appointment datepicker.
   - Acceptable examples:
     1. Add the renew password reminder feature.
     2. Add the newsletter signup.
     3. Fix appointment picker bugs
   - Unacceptable examples:
     1. Apply review comments
     2. A minor issue
     3. Solve a bug related to X

### The art of branching - GitHub flow

 - Anything in the `master` branch is deployable
   - There are no `hotfix`, `develop`, or other particular branches
   - Bug fixes, new implementation, and so on are constantly merged onto the `master` branch
   - You never push into this branch
 - Create descriptive branches off the master
   - You always branch from the `master` branch
   - To better identify them, you have to use descriptive names to get meaningful topic branches
   - Proper names (note the use of dashes):
     - `new-user-creation`
     - `most-starred-repositories`
     - `renew-password-email`
 - Push to named branches constantly
   - You push feature branches to the remote regularly, even if you are the only developer involved and interested in it
 - Open a pull request at any time
 - Merge only after a pull request review
 - Deploying immediately after review
 
 ### Tools
 
  - `.dotaliases` for git: https://github.com/algotech/dotaliases/blob/master/doc/bash/git_aliases.md
  - SourceTree: https://www.sourcetreeapp.com/

## Code review

A guide for reviewing code and having your code reviewed. We have to accept that many programming decisions are opinions. Discuss tradeoffs, and reach a resolution quickly.


### When having your code reviewed

 - Be grateful for the reviewer's suggestions.
 - Don't take it personally. The review is of the code, not you!
 - Assume the best intention from the reviewer's comments.
 - Push commits based on earlier rounds of feedback as isolated commits to the branch. Do not squash until the branch is ready to merge. Reviewers should be able to read individual updates based on their earlier feedback.
 - Seek to understand the reviewer's perspective.
 - Try to respond to every comment.

### When reviewing code

 - Understand why the change is necessary (you should at least read the ticket).
 - Identify ways to simplify the code while still solving the problem.
 - Seek to understand the author's perspective.
 - Ask good questions; don't make demands.
 - Offer alternative implementations, but assume the author already considered them.

### Code review checklist

This code review checklist helps the code reviewers and software developers (during self code review) to gain expertise in the code review process.

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
 - Are all data inputs validated against security threats such as SQL injections and Cross Site Scripting (XSS)?

#### Coding

 - Do all the varialbes say what they are for and not what data type they have?
 - Do all the methods have a clear name for what they are going to do?
 - Are there any hardcoded string/integer values?
 - Is there any code ownership comment (like `Created by X`) in the code? We use Git for that.
