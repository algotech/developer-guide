# coding-standards

### Git

#### The art of committing

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
   - Good examples:
     1. Send an email to the user with a link to renew the password.
     2. Add the newsletter signup in homepage.
   - Bad examples:
     1. Add the renew password reminder feature.
     2. Add the newsletter signup.
