# Git
#### ssh keys
add ssh keys so you do not have to type password everytime and also you will need it for getting some of our private modules via npm. https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

# Node, npm
#### nvm
use nvm and no other manual/package etc. Follow this link and use latest LTS version of node. https://github.com/nvm-sh/nvm and https://github.com/nvm-sh/nvm#usage  (go for the latest LTS node version)

# IDE
#### Intellij idea
We encourage intellij idea Ultimate edition (very preferred). If you do not have the license, then at least community edition. If you do not have the hardware resources, you should get them to run intellij. If not, the last case (not preferred) is vscode.

Note that you should have minimum of 4 Gb ram. Minimum 8Gb recommened with most unused plugins disabled (else you it will consume a lot of cpu and memory)

# Operating system
#### Kubuntu
Kubuntu (with k) LTS (ONLY LTS) versions are preferred.
#### Windows
If you use windows, you have to do the following in package.json (we have not made special windows commands yet as we mostly use and encourage Linux. This is the same setup we use on servers. So environment differences would be minimum).

exclude   `.`  (dot) and `/` slash at line starts
replace `/`  slashes wit `\` blackslashes
replace   `;`  with `&`

# Pull requests / merge requests
### prerequisits of PR
In order to get your code merged in master branch, you need to do the following. Do not make a PR Pull request without the following first done.
#### CI
We do contineuous integration on github. Make sure all checks are passed and its a green tick with your pull request and commits.
##### linting
One of the CI steps is linting. You can autofix with npm scripts in package.json and then manually test for any lint errors before making a Pull request.
#### functionality correct
All functionality should be tested before making a PR (self testing)
#### Peer review
Next step is to have a peer review. (switch to branch, pull, check manually, then review code on github)
#### lead review
Next step is the have a final review by lead / manager
#### Close Old PR first
Always try best to close, finalize and get old pull/merge requests first
#### One PR per day
There should be one PR per day. This is mandatory. If you fail to get it approved, you have not achieved the full success of the day. You should file a PR before few hours of the day so it defintily get approved (assuming that it might have some issues and it might take you some time before dayend to resolve those issues and get the PR finally approved).

# Coding and development
## "Getting things done"
#### Do only whats required
Only do whats needed. Nothing less, nothing more. If you see something wrong or a room for improvement, ask permission beforehand for any deviations because if you think something is beneficial, this may not be the case with a different perspective, it may have side effects or simply it may be be very good but not needed at the time or at the cost of the current time. So simply ask lead/manager and discuss first.
#### Improvment
You might be thinking then, how do we improve the code/funcitonality? Of course, you do but in steps. First target is to complete in a 'good way' and not in a 'perfect way'. Perfection is a step by step process and the steps may reach infinity in some cases. We will not be able to afford time loss for completion at the cost of long perfection sessions. So in short, get first stage workable. Get it approved, move to next stage, get it approved and so on. Do not try to reach stage 10 by wanting to learn and experiment for 9 prior stages in one go. If your code is below standards, you will ultimately get PR issues anyway. Remember them and do not repeat them. So you/your code improves any way by default.
#### Smart done
Suppose you have 10 things in your todo list. 5 things 100% done is better than 10 things done 50% each.
#### Definition of done
Completion of a task with minimum acceptable qaulity (does whats needed, passes lint and code review etc).

## Efficiency
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
#### Personal info
Sharing of any personal information or discussing anything not related to work/current tasks is treated miss conduct.


