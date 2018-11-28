# Bug reporting guidelines

## What
This is a set of guidelines for bug reporting. You can read it and also use it as a reference, just like the commits document.

## Why
**TL;DR**: Bad bug reporting wastes time.

**Long version**:
* Bad bug reporting wastes **the developer’s time**, because they don’t have all the data. They need to “guess” parts of what you did to reproduce the bug. Sometimes they get stuck and can’t reproduce, so…
* Bad bug reporting wastes **the reporter’s time**, because they need to re-write the issues and restart the whole process of reproducing a bug which they already reproduced on their first report.
* Bad bug reporting wastes **everybody’s time**, because this ping-pong match between the reporter and the developer can last for days and it usually gets frustrating.

## Reproduce
Make sure you are reporting a bug that can be reproduced. Make sure you have a set of steps that reproduces the bug. Try similar steps to identify how generic the bug is.

E.g. if you can not log in with a user/password combination, try other combinations. Maybe the entire login part is broken, maybe it is just the one user. Try using both Postman and the Frontend application, if both exist, to identify whether you should report the error on frontend or backend.

## Short, but precise title
Please use one-sentence titles that describe the actual error.

**Bad**:
* “Server crashes on login”
* “Frontend stops working when using Chinese”
* “Error on backend”
* “HUGE BUG ON THE APP!!! FIX NOW” (please don’t do this. I will want to kill you.)

**Good**:
* “NotFoundUser error when logging in with username john@john.com” or “Redirected to guest page when logging in with john@john.com”
* “Frontend becomes unresponsive when special characters are entered in the address form”

## Meaningful description
A description of about 3-10 lines should cover the following:
### Steps to reproduce
Include the setup:
* environment (local, dev, test, production etc., whatever your setup may be)
* database used (if not standard). If the database is not available to the dev that solves the bug, have the courtesy of providing a dump.
* logged in account used, if applicable. If the password is not available to the dev that solves the bug, have the courtesy of providing it.

Add any steps to reproduce, including accessed URLs and inputs used in forms, in chronological order. Do not skip steps, even if they seem trivial. One checkbox can change the entire flow and waste time trying to reproduce.

### Consequences
What happens after completing the steps to reproduce.

E.g. “The user is redirected to the guest page.”

### Expected/suggested behaviour
What should have happened after completing the steps to reproduce.

E.g. “The user should have been redirected to the admin panel.”

## Attachments
Screenshots, log files, error messages. If the description is not explicit as to indicate the page where the error occurs, please do not crop out the URL (or other indicators of where we are in the app).

## Miscellaneous issue reporting best practices
* attach correct labels, including realistic priority labels. Do not mark all bugs as highest priority, nor all lowest, but keep a sane balance.
* make sure you use the correct Kanban column on the board and labels such as “question”, “help needed”, “enhancement”, “quickfix” etc.
* tag and assign colleagues accordingly
* follow-up with a comment if the bug is ignored
* etc.

## Template
A bug reporting template following these guidelines can be found here:

 - [Bug reporting template](bug-reporting-template.md)
