# Git
#### ssh keys
add ssh keys so you do not have to type password everytime and also you will need it for getting some of our private modules via npm. https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

# Node, npm
#### nvm
Do not install node by any other means but only use nvm. Follow this link and use latest LTS version of node. https://github.com/nvm-sh/nvm and https://github.com/nvm-sh/nvm#usage  (go for the latest LTS node version)

# IDE
#### Intellij idea
We encourage intellij idea Ultimate edition (very preferred). If you do not have the license, then at least community edition. If you do not have the hardware resources, you should get them to run intellij. If not, the last case (not preferred) is vscode.

Note that you should have minimum of 4 Gb ram. Minimum 8Gb recommened with most unused plugins disabled (else you it will consume a lot of cpu and memory)

# Operating system
#### Kubuntu
Kubuntu (with k) LTS (ONLY LTS) versions are preferred. https://kubuntu.com
#### Windows
If you use windows, you have to do the following in package.json (we have not made special windows commands yet as we mostly use and encourage Linux. This is the same setup we use on servers. So environment differences would be minimum).

exclude   `.`  (dot) and `/` slash at line starts

replace `/`  slashes with `\` blackslashes

replace   `;`  with `&`

# Pull requests / merge requests
### prerequisits of PR
In order to get your code merged in master branch, you need to do the following. Do not make a PR Pull request without the following first done.
#### CI
We do contineuous integration on github. Make sure all checks are passed and its a green tick with your pull request and commits.
#### linting
One of the CI steps is linting. You can autofix with npm scripts in package.json and then manually test for any lint errors before making a Pull request.
#### Tests
If your project has unit test/ integration tests/ automation tests enforced, do not file PR without them.
#### functionality correct
All functionality should be tested before making a PR (self testing)
#### Release notes
All PRs should have release notes about the functionality you made in that PR. It should briefly describe about the business flow, technical flow, any third party lib used and reason for its preference. This will have some information that is not available in story points. e.g any library used and why preferred, flow of code, technical precautions etc. This is very brief usually from 25 words to 100 words max. 
#### Peer review
Next step is to have a peer review. (switch to branch, pull, check manually, then review code on github)
#### lead review
Next step is the have a final review by lead / manager
#### Close Old PR first
Always try best to close, finalize and get old pull/merge requests first
#### One PR per day
There should be one PR per day. This is mandatory. If you fail to get it approved, you have not achieved the full success of the day. You should file a PR before few hours of the day so it defintily get approved (assuming that it might have some issues and it might take you some time before dayend to resolve those issues and get the PR finally approved).

# Project management
## Agile
#### story points
#### stand up
#### sprints
## Project management tool
We had used Jira but prefer easy redmine.

# Coding and development
## "Getting things done"
#### Do only whats required
Only do whats needed. Nothing less, nothing more. If you see something wrong or a room for improvement, ask permission beforehand for any deviations because if you think something is beneficial, this may not be the case with a different perspective, it may have side effects or simply it may be be very good but not needed at the time or at the cost of the current time. So simply ask lead/manager and discuss first.
#### Improvment
You might be thinking then, how do we improve the code/funcitonality? Of course, you do but in steps. First target is to complete in a 'good way' and not in a 'perfect way'. Perfection is a step by step process and the steps may reach infinity in some cases. We will not be able to afford time loss for completion at the cost of long perfection sessions. So in short, get first stage workable. Get it approved, move to next stage, get it approved and so on. Do not try to reach stage 10 by wanting to learn and experiment for 9 prior stages in one go. If your code, on the other hand, is below standards, you will ultimately get PR issues anyway... Remember them and do not repeat them. So you/your code improves any way by default. But keep a fine line between personal part of pure self learning (with self motive only) and self experimenting vs completing the task as priority and learning through that (which will be done any way during the process so everyone gets happy).
#### Smart done
Suppose you have 10 things in your todo list. 5 things 100% done is better than 10 things done 50% each.
#### Definition of done
Completion of a task with minimum acceptable qaulity (does whats needed, passes lint and code review etc).
## Coding practices
#### libraries choice
You should have very good reasons to choose a library. In most of the cases, you should ask lead before choosing a library.
#### ES6+ over old
Always use ES6+ syntax over old. Take it as a mandatory rule.
#### TS of JS
If your project is Typescript based, use Typescript wherever possible.
#### Tests
We use Jest as the testing library for unit tests and integration test. For automation test, the choice is of project manager.

# Efficiency
#### consistency
Be consistent in choosing, using, following architecture, libraries, patterns
#### reusable and modular code
Do not repeat your self
#### CPP 
commit, pull, push in same sequence. Do this as frequently as you can. Sequence is important. Commit first, then pull (from your branch AND from master at least), then push (to your branch). E.g For a team of X number of people, you should do it X times a day. Ie in a team of 3 people, you should do this at least 3 times a day. 

# Directory structure
### Frontend react based
To be continued
### Backend nodejs
To be continued

# Configuring development environment
#### CORS restrictions
If you get CORS errors, you can install browser plugin (one called `allow cors` for chrome). You have to hit the big icon and make it colored to activate it.
#### Localhost nginx config (not needed unless asked)
To be continued

# Online remote groups
#### Noise due to group talk
If you feel theres too much voice conversations in remote group, you can mute the volume but you should be alert for any chat messages. If some one wants to talk to you, (s)he should ping you on chat. You should do the same.
#### Stay connected all the time
You should stay connected to group collaboration software all the time
#### Personal info
Sharing of any personal information or discussing anything not related to work/current tasks is treated miss conduct.
