- [Git](#git)
      - [ssh keys](#ssh-keys)
- [Node, npm](#node--npm)
      - [nvm](#nvm)
- [IDE](#ide)
      - [Intellij idea](#intellij-idea)
- [Operating system](#operating-system)
      - [*ubuntu LTS](#-ubuntu-lts)
      - [Windows (NOT preferred)](#windows--not-preferred-)
- [Pull requests / merge requests](#pull-requests---merge-requests)
  * [PR per feature](#pr-per-feature)
      - [PR part 1](#pr-part-1)
      - [PR part 2](#pr-part-2)
      - [PR part 3](#pr-part-3)
      - [Combined PR of multiple tickets](#combined-pr-of-multiple-tickets)
  * [prerequisits of PR](#prerequisits-of-pr)
      - [Create branch](#create-branch)
      - [Pull from branch and master](#pull-from-branch-and-master)
      - [CI](#ci)
      - [linting](#linting)
      - [Tests](#tests)
      - [Self testing](#self-testing)
      - [Release notes](#release-notes)
      - [Peer review](#peer-review)
      - [lead review](#lead-review)
      - [Issues in PR](#issues-in-pr)
      - [Close Old PR first](#close-old-pr-first)
  * [Daily PRs routine](#daily-prs-routine)
      - [One PR per day](#one-pr-per-day)
      - [PR 2 after PR 1 approval only](#pr-2-after-pr-1-approval-only)
      - [Early review](#early-review)
      - [How to solve PR issues](#how-to-solve-pr-issues)
- [QA Quality Assurance](#qa-quality-assurance)
      - [No such thing](#no-such-thing)
- [Naming conventions](#naming-conventions)
      - [Git commit message](#git-commit-message)
      - [Branch name](#branch-name)
      - [PR title](#pr-title)
      - [Function names](#function-names)
      - [Variable names](#variable-names)
      - [Css variable names](#css-variable-names)
      - [Directory names](#directory-names)
      - [Notes for names](#notes-for-names)
- [Comments](#comments)
  * [Code comments](#code-comments)
      - [Commented code for later use](#commented-code-for-later-use)
- [Docs](#docs)
  * [API docs](#api-docs)
  * [Code docs](#code-docs)
- [Project management](#project-management)
  * [Agile](#agile)
      - [story points](#story-points)
        * [Why can't we just start coding. Why spend so much time in plan?](#why-can-t-we-just-start-coding-why-spend-so-much-time-in-plan-)
      - [stand up](#stand-up)
      - [sprints](#sprints)
      - [Ownership](#ownership)
      - [Deviations](#deviations)
      - [Timelines](#timelines)
      - [I got late due to problems](#i-got-late-due-to-problems)
      - [How can I improve estimate and execution](#how-can-i-improve-estimate-and-execution)
    + [Change in requirements](#change-in-requirements)
      - [I created something and it got changed. Why?](#i-created-something-and-it-got-changed-why-)
      - [Ok but if it had to change, why did we do it like that in the first place?](#ok-but-if-it-had-to-change--why-did-we-do-it-like-that-in-the-first-place-)
  * [Project management tool](#project-management-tool)
      - [Task / issue types](#task---issue-types)
      - [Task understanding](#task-understanding)
      - [Execution](#execution)
      - [Do it yourself](#do-it-yourself)
      - [Priority](#priority)
      - [How to see my tasks](#how-to-see-my-tasks)
      - [Your work time](#your-work-time)
  * [Estimation](#estimation)
- [You](#you)
  * [Who are our favourites? Top qualities?](#who-are-our-favourites--top-qualities-)
- [Coding and development](#coding-and-development)
  * [Getting things done](#getting-things-done)
      - [Do only whats required](#do-only-whats-required)
      - [Improvment](#improvment)
      - [Smart done](#smart-done)
      - [Definition of done](#definition-of-done)
  * [Coding practices](#coding-practices)
      - [libraries choice](#libraries-choice)
      - [ES6+ over old](#es6--over-old)
      - [TS over JS](#ts-over-js)
      - [Tests](#tests-1)
  * [Javascript](#javascript)
      - [Never disable linting](#never-disable-linting)
  * [Frontend](#frontend)
      - [css over js](#css-over-js)
        * [External cdn or other links](#external-cdn-or-other-links)
      - [Images](#images)
  * [Frontend react](#frontend-react)
      - [One file per component](#one-file-per-component)
- [Efficiency](#efficiency)
      - [consistency](#consistency)
      - [reusable and modular code](#reusable-and-modular-code)
      - [CPP](#cpp)
- [Directory structure](#directory-structure)
    + [Frontend react based](#frontend-react-based)
    + [Backend nodejs](#backend-nodejs)
- [Configuring development environment](#configuring-development-environment)
      - [CORS restrictions](#cors-restrictions)
      - [Localhost nginx config](#localhost-nginx-config)
- [Tech notes](#tech-notes)
  * [Backend](#backend)
    + [Node.js](#nodejs)
      - [Knex transactions](#knex-transactions)
- [Online remote groups](#online-remote-groups)
      - [Noise due to group talk](#noise-due-to-group-talk)
      - [Stay connected all the time](#stay-connected-all-the-time)
      - [Personal info](#personal-info)
- [Daily routine](#daily-routine)
  * [What to do at day start](#what-to-do-at-day-start)
      - [Log in start time](#log-in-start-time)
      - [Message manager](#message-manager)
      - [Keep communication app onn](#keep-communication-app-onn)
      - [Refresh task list](#refresh-task-list)
      - [Plan or ask questions](#plan-or-ask-questions)
  * [What to do at day end](#what-to-do-at-day-end)
      - [Work and tickets complete](#work-and-tickets-complete)
      - [Plan or ask questions](#plan-or-ask-questions-1)
      - [Message manager](#message-manager-1)
      - [Log sign out time](#log-sign-out-time)
  * [Attendance](#attendance)
      - [Late sign-in](#late-sign-in)
- [Tutorials](#tutorials)
  * [Javascript Misc](#javascript-misc)
    + [Recommended authors](#recommended-authors)
  * [Backend Node.js](#backend-nodejs)
    + [Node core](#node-core)
    + [Testing / Jest](#testing---jest)
  * [Frontent React](#frontent-react)
    + [React core](#react-core)
  * [Git / github](#git---github)
    + [Git](#git-1)
    + [Github](#github)
  * [Project tool](#project-tool)
    + [Info gathering](#info-gathering)
  * [Basics](#basics)
    + [Javascript core](#javascript-core)
    + [Architecture for newbies](#architecture-for-newbies)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>




# Git
#### ssh keys
add ssh keys so you do not have to type password everytime and also you will need it for getting some of our private modules via npm. https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent


# Node, npm
#### nvm
Do not install node by any other means but only use nvm. Follow this link and use latest LTS version of node. https://github.com/nvm-sh/nvm and https://github.com/nvm-sh/nvm#usage  (go for the latest LTS node version)

For windows: https://github.com/coreybutler/nvm-windows



# IDE
#### Intellij idea
We encourage intellij idea **Ultimate edition** (very preferred). If you do not have the license, then **at least community edition**. If you do not have the **hardware resources**, you should get them to run intellij. If not, the last case (not preferred) is **vscode**.

Note that you should have **minimum of 4Gb ram**. Minimum **8Gb recommened** with most **unused plugins disabled** (else you it will consume a lot of cpu and memory)



# Operating system
#### *ubuntu LTS
(**ONLY LTS**) versions are preferred
1. **Kubuntu** (with k) If you have 16G plus ram and a quadcore and ok to invest system resources on beauty and features. LTS. https://kubuntu.com
2. **Xubuntu** (with X) LTS If you don't have enough resources or just want performance with ok to medium UI. https://xubuntu.org
#### Windows (NOT preferred)
If you use windows, you have to do the following in package.json (we have not made special windows commands yet as we mostly use and encourage Linux. This is the same setup we use on servers. So environment differences would be minimum).

exclude   `.`  (dot) and `/` slash at line starts

replace `/`  slashes with `\` blackslashes

replace   `;`  with `&`

You should try your **best** not to use windows but linux for develoment as it will be same with deployment/ production environment and save you from a lot of issues.

Expertise in Linux is also a key important skill in the developers life which he would face the need for any way.


# Pull requests / merge requests
## PR per feature
1. A feature should be divided into following **main parts/categories** and all PRs should be passed step by step. 
1. There can be more PRs than the below stated but these are the minimum and more sort of **broad categories**. 
1. Developer should write the `category number` in PR title. E.g `login page PR category #1`. Developer should **not work/extend code based on same/previous PR functionality, until the first PR is merged/approved**. This is because if there are issues in the intial PR, then the extended code based on that intial PR code will also have issues and consume more and more time. Same philosophy applies to PR categories. E.g do not go to category 2 unless 1 is approved.
1. You should work on some other feature/project during wait time.
#### PR part 1
1. First PR should have all the possible **flow/achitecture with directories, files and empty functions** with //TODO comments and pseudo code inside (and interfaces if Typescript is used). This will tell the approace of the the developer, will help the developer envision the big picture/process/strategy. It will also get the code flow review at a much earlier stage and will eliminate gaps in expectations far ahead of time.
1. There are many approaches in industry to make flow before coding e.g **UML** diagrams, test cases (where test cases are written before writing actual code (**TDD** test driven development)), or simply writing **empty functions/interfaces** etc.
1. Some people may say, "**what if the code is likely or will change in future? is PR 1 useless?**". Well, no. If its likely to change at a greater percentage, it means the plan and structure initally made needed improvement. Secondly, if some of it will change anyway, the effort to make initial design should have given more advantage over the minor con/disadvantage (to just remove/change an empty function/file).

##### Frontend example of PR 1
It will include and a react app for example:
1. All functions that ever would be needed (for example, but not limited to, routes, service, ajax call functions, alert, validation, on submit funnctions, util)
1. All components that ever would be needed
      1. Each component will have a body of sketchy html with no css styles. This is to have a viewable sketchy layout to be understood by the person that will do PR 2. This will be more like a wireframe. The app should run with working routes and sketchy structure of html/components viewable in browser.
      1. Each component will call child components as well.
1. Choice of libraries /frameworks and imports / configs of same

##### Backend example of PR 1
1. All functions tha ever would be needed but with no implementation code with all child components but no implementation.
1. Choice of libraries /frameworks and imports / configs of same

Notes: Example of child components hierarchy but with no implmentation is
```
doSomeParent(){doSomeChild1(); someOtheCode; someLibCalls;}
doSomeChild1(){doSomeChild2(); someOtherPseudoCodeMaybe;} // to make a flow for PR 2 person to understand and implement
doSomeChild2(){/* implementation in PR 2 only */}
```
#### PR part 2
Each function/part in PR #1 will be **implemented** (with unit tests if it is enforced in the project).

##### Frontend example of PR 2
1. All css styling
1. Implementation of everything. E.g but not limited to functions, components, ajax calls, alerts, etc. If PR 1 was made correctly, there should be no need to create any new functions/classes/items in PR 2. Just implementation would be needed.

##### Backend example of PR 2
1. Implementation of everything. If PR 1 was made correctly, there should be no need to create any new functions/classes/items in PR 2. Just implementation would be needed.

#### PR part 3
This would be **final PR** and will also make sure that other parts of **application work in harmony** with the current task. If integration tests and/or automation tests are enforced in the project, this PR should have those too).

#### Combined PR of multiple tickets
PR 1 and PR 3 for multiple tickets and stories can be combined in one PR but PR 2 for each story should be separate. As PR 3 usually at the end of multiple stories or full project and may cover multiple stories/tickets and PR 1 is simple and small structure and can also be made for multiple stories/tickets.

## prerequisits of PR
In order to get your code merged in daily-stable-master branch (for PR 1 and PR 2), you need to do the following. **Do not make a PR Pull request without the following first done**.
#### Create a fork and branch
Create a fork from original repository into your own company account, then clone your project git repository locally (by default the main default branch will be daily-stable-master). Create a new branch from it (the main default branch). Start coding in it.

It is to note that PR 3 is a separate process of merging daily-stable-master branch into master branch at major releases. Usually done by leads.

You may see tutorials at bottom about forking and PRs

#### Pull from branch and default branch
Before pushing code for PR, make sure you have done CPP (commit(in your branch), pull (from your branch if others are working on it too. If not, then simply from default branch), push (to your branch))
#### CI
We do **contineuous integration (CI)** on github. **Make sure all checks are passed** and its a green tick with your pull request and commits.
#### linting
One of the CI steps is linting. You can **autofix** with npm scripts in package.json and then manually test for any lint errors before making a Pull request. **Manually fix** if something is not autofixed. As a side note, observe autofixed syntax and learn from it.

#### Tests
If your project has unit test/ integration tests/ automation tests enforced, do not file PR without them. In most cases, integration tests are mandatory. Do not forget to ask from your manager.

Following are the default coverages if not overriden by manager.

##### Tools to use only
1. Jest
1. React-testing-library
1. ~~Enzyme~~-- (not permitted to use for now. Use React-testing-library)
1. ~~Cypress~~ (not testing e2e for now but later could be used after approval to use)
1. ~~Puppeteer~~ (not permitted to use for now. Use Cypress)
1. Mocking: No need for now as knex will have read test database. For endpoint and end to end testing, we are not making network calls however cypress/puppeteer will make real calls when used.

##### Backend
1. **Unit tests and integration tests**: Use Jest
      1. Controller functions should have **100% coverage**. These will be unit tests (not endpoint tests making ajax calls). For example, you will test loginCtr.js's function loginUser('/path/login',req,res,next); by constructing req.query or req.body params and calling these functions. No need for network call.
      1. Everything in base directory such as Base Daos or services should have **100% coverage**
      1. Everything in shared directories should have **100% coverage**
      1. Rest of the code should have at least **10% coverage** (for now). Most used/referred and most important functions should be tested in prioroty. Important thing to note here is that **if you test any function, you should test it 100%**. If not, leave that function.
1. **Endpoint tests** (type of integration test where network call is made)
      1. Endpoint tests will be making an ajax call to '/path/login' but will check status code only. **Currently not applicatble**.

###### Config to use for backend
jestconfig.js
```
{
  "jest": {
    "coverageThreshold": {
      "global": {
        "branches": 10,
        "functions": 10,
        "lines": 10,
        "statements": 10
      },
      "./dist/src/**/controller/*": {
        "branches": 100,
        "functions": 100,
        "lines": 100,
        "statements": 100
      },
      "./dist/src/base/**/*": {
        "branches": 100,
        "functions": 100,
        "lines": 100,
        "statements": 100
      },
      "./dist/src/**/shared/**": {
        "branches": 100,
        "functions": 100,
        "lines": 100,
        "statements": 100
      }
    }
  }
}
```

      
##### Frontend react
1. Non react component function unit test: Use Jest with at least **10% coverage**.
1. React components: Use Jest + React-testing-library should have **20% coverage** for all components
1. Anything in base or shared directories should have at least **50% coverage**.
1. E2e end to end: Use Cypress (**Currently not applicable**)
      1. Test coverage is at least **1 test per view screen**. Screen is a unique page content. E.g ignoring header, footer, nav bar (common things but also included in screen and needs test), login page is one screen, register is another, add user another, list user is another. This should test CRUD operation(s) of that screen but **only focus on UI** and some data visibility in it. e.g in a user creation page, test should fill form, hit submit, then view updated data, then edit it, then delete it, then add again, view it (wait for element and match with expected result). There is no need to redo and retest things that are already been tested in controller integration testing at backend.
      
###### Config to use for frontend react
jestconfig.js
```
{
  "jest": {
    "coverageThreshold": {
      "global": {
        "branches": 10,
        "functions": 10,
        "lines": 10,
        "statements": 10
      },
      "./**/*Comp.*": {
        "branches": 20,
        "functions": 20,
        "lines": 20,
        "statements": 20
      },
      "./**/base/": {
        "branches": 50,
        "functions": 50,
        "lines": 50,
        "statements": 50
      },
       },
      "./**/**shared**/": {
        "branches": 50,
        "functions": 50,
        "lines": 50,
        "statements": 50
      }
    }
  }
}
```
      

#### Self testing
All functionality should be tested before making a PR (self testing). Run and **test the functionality yourself first**.

#### Release notes
All PRs should have release notes about the functionality you made in that PR. It should briefly describe about the business flow, technical flow, any third party lib used and reason for its preference or at least what approach did you took to complete the task. This will have some **information that is not available in story points**. e.g any library used and why preferred, flow of code, technical precautions etc. This is very brief usually from **25 words to 100 words max**. Few example:
1. Had to convert .ai to .svg via 'outline conversion' ref https://somesite.com else text in svg gets distorted.
1. Preferring XYZ lib as ABC is deprecated (or has DEF issues) or GHI security concerns.
1. Using http v2 due to tons of advantages (list or provide link)
1. Pending things

#### Peer review
Next step is to have a peer review. (Peer should switch to branch, pull, check manually, then review code on github)

#### lead review
Next step is the have a final review by lead / manager

#### Issues in PR
If there are any issues in PR, they should be replied/typed in reply text box as fixed or replied to the question or a comment. Ultimately **all issues should be marked as resolved by the issue creater by clicking the resolve button**. The developer / PR creater should not press this button but only the issue creater should.

#### Close Old PR first
Always try best to close, finalize and **get old pull/merge requests first** before proceeding to new ones.
## Daily PRs routine

#### One PR per day
There should be one PR per day (which is consisting of all PR part 1 + PR part 2). The PR should have a complete functionality including test code. **This is mandatory**. If you fail to get it approved, you have not achieved the full success of the day. You should file a PR before few hours of the day so it defintily get approved (assuming that it might have some issues and it might take you some time before dayend to resolve those issues and get the PR finally approved).

See [getting-things-done](#getting-things-done) for more information

#### PR 2 after PR 1 approval only
Do not move to PR 2 or code anything for it if PR 1 is not approved. If you wait for the reviewer, you can do other tasks and PRs but do not move to PR 2 if PR 1 is not approved

#### Early review
We emphasis on early review rather than complete all and get it reviewed after that. e.g you make an app of 10 things / steps.

If you had made a mistake at step 2, then all steps from 2-10 might get influenced to be in the wrong direction. 

In thise case, if review is done at step 10 (completion of app), then it would be a "too late to find" senario and all/ most of 2-10 steps might need a refactor.

Whereas if the review on each step (2 in this case), only 2 will be corrected and later steps will be aligned to it.

The later is safer, more efficient, more time saving, needs lesser effort as a whole, gives more certainty and many other benefits.

#### How to solve PR issues
When an issue in PR is created, it should be fixed, code pushed, and a comment should be given in reply to the issue. A simplest comment can be 'Fixed'. Then the creater of the issue should resolve the issue by hiting  the resolve button. Not the developer. When all issues are resolved, PR can be merged.

# Pull request / merge request model B
This is an alternative and discretion of manager to adapt for projects. In model B
1. Developer will create PR on github but Github will not be used for issue creation. Instead, reviewer will type issues inside code with signature, commit and push e.g `// {ABC}:PRI text here`. And developer will respond below this line after changing code like this `// {CDE}: text here`. Commit and push. 
1. Once the code changes, conversation like this ends, the manager will cut and paste this conversation at the end of file. And approve PR after changing `// {ABC}:PRI` to `// {ABC}:PRRI`. Cuting and pasting at bottom like this means issue is accepted as resolved.
1. For commenting, you can use simple abbreviations like `// {ABC}: text here`
1. This will keep a record of all PR issues at end of each file.
1. Abbreviations to note here are
      1. {ABC} or {CDE} - Name abreviation. E.g John Corner is JOC. You should set one signature and be consistend on it.
      1. PRI - Pull request issue
      1. PRRI - Pull request resolved issue.
1. These issues can be referenced during and after the PR by searching `}:PRI` or `}:PRRI`
1. The `/* */` can be used instead of `//` for multi line comments if needed.

# QA Quality Assurance
#### No such thing
1. If you are a developer, in your world, there should be no such thing as "External dedicated QA" testing your work.
1. It is **not normal, implicit or casual to assume there there will be bugs and someone will find those and report back to you**. Actually the qualities of a **good developer** is that (s)he understands requirements and checks his code and functionality well enough before declaring those as complete.
1. The peer review mentioned above in git PRs is only for improvements. Do not ever rely on those or expect that someone will spoon feed you about your mistakes. Mistakes are deficiencies those should be minimized rather being casual about them.

# Naming conventions
This can be best informed by the following examples. If you are not following these, your PR may get rejected on just the naming conventions. Clear and self explanatory names are critical and save people from a lot of frustration.
#### Git commit message
1. add backend min char check on password - login page
#### Branch name
1. frontend-form-validation--login-page
#### PR title
1. slicing done - login page
1. frontend form validation - login page
#### Function names
1. isValidEmail(email)// returns true/false
#### Variable names
1. userArray
1. userMap
1. users | userList //list of objects
#### Css variable names
1. list-item
1. list-item-container
#### Directory names
1. directoryName
#### Notes for names
1. Function and variable names can be a big long e.g even to 20 characters but they should **smartly** and **clearly** explain the meaning and purpose. I.e be **self explanatory**.

# Comments
## Code comments
#### Commented code for later use
If unused commented code is present and developer needs it for future reference, move it to the bottom most of file.

# Docs
## API docs
To be continued
## Code docs
To be continued



# Project management
## Agile
#### story points
Each story / ticket is given points based on its complexity and time to complete. This is achieved when requirements are understood and best course of action suitable for the current business needs is concluded.
##### Why can't we just start coding. Why spend so much time in plan?
1. In short, it is to act and make an "informed decision". It is good for both business and developer though a developer may want to just code for practice or just due to interest or passion on something that attracts him/her. That thing, strategy, solution or way to doing the task may or may not even be the best way or decision for the business needs. Think like a developer and also think about the business needs. Keep yourself in the shoes of the product owner. If you have questions on how to think like one, ask questions.
1. At no point should a ticket be started for execution until the best plan of action, strategy, requirements are clear, defined and approved. E.g you want to go from city A to city B. If you search a bit and not just blindly hit the road in your car in garage, maybe a new bus services goes there in more comfort, shorter time, on a newly made highway you didn't knew about before. Or maybe a cost effective bullet train. Or maybe there is a curfew news you missed that can get you in jail or severe. Longer or critical journeys may include feul comparisons or going to a different city at all (changing course). All this cannot be decided without understanding requirments and creating best course of action.

#### stand up
#### sprints
Our typical schedule and sequence of doing things:
1. Do the 'estimates' ticket of each story to have an understanding of requirments, action plan andnestimated time to execute for each.
      1. Get estimationes for each story approved step by step, one by one.
1. Once (and only when) above is approved, create PR 1 for each story.
      1. Get PR 1 for each story approved step by step, one by one.
1. Once (and only when) above is approved, create PR 2 for each story.
      1. Get PR 2 for each story approved step by step, one by one.
1. Once (and only when) above is approved, create PR 3 (optional).
1. Finish the work accuretly as per needs, on time.
1. Attend retrospective meeting.

#### Ownership
Sprints are ownership of the team overall, success of a sprint is success of the full team (regardless of individual tasks). You can say you may hold at least 1% to 10% responsibility of overall team work. You own 100% of the taks specificily assigned to you. Responsibility includes, but not limited to, completing the task with at least minimum quality and absolutely agreed time mentioned in estimates.
#### Deviations
If you encounter any deviation in attainable preplaned timeline estimates, promptly inform the reasons and circumstances to your lead and project manager. Inform far ahead and as soon as possible when deviations are anticipated. NOT at the end or when time had elapsed.
#### Timelines
Once sprints and/or ticket estimats and plans are created and agreed upon, if there are delays in timeline without a reasonalbe cause, then the delay is the responsibility of the developer. (S)he should cover up the missed deadlines by any means possible to ensure reasonable efficiency. This may involve working for more time or any ways of being smarter and more productive to cover deadlines.

It is the professional responsibility of the candidate, at any level, to provide reasonable estimates and accomplish the tasks in that reasonable timeframe. In cases of otherwise, in absence of justified reasons, it is a negative mark on the repute of the candidate.

#### I got late due to problems
Someone might say "I got late because I encountered problems". Well, provided that you planned the project / task with due care and you are a proactive problem solver, the timeline should not be in deviation. 

Suppose you are going from city A to city B. Before journey, you would plan your journey, what to use as transport (train/bus/car), whats the journely time by each, time and money needed, schedule and see road blocks, make strategy before acting etc.

If a hazard comes like train out of order or delayed, or type puncture of a car. You should have a backup plan to resolve the situation. Get an alternative route/vehicle at the spot or plan it slightly before the journey even. e.g a taxi, or rent a bicycle, or simply try to fix the tyre (whatever is best suited and quickest).

**IF you are a proactive problem solver** (which is expected from a developer quite implicitly), **you will get the job done in almost same time** or very slight negligible deviations anyway. If you were not able to, then either planning needs improvement or problem solving needs improvement or there was a 100% natural unstoppable hazzard (e.g earth got destroyed and all died). There is NO third reason.

To explain, a soldier might say: if we had to go to a city from another city in a predetermined time, we will find a way; any way; and get the job done. There are only few corner cases in which you can't do it. E.g you get stuck by lightening and die on the way.

#### How can I improve estimate and execution
Ask few questions to your self
1. Are you spending more time on things those are not important compared to critical path and more important tasks? Or even slightest postion of your activity is not even needed but you do it pationately, striving hard? Think again. Analyse the day.
1. When you started working, did you proportioned total available time of the day into tasks or you kept stuck on 2nd task out of 10 tasks and the day passed and you found that task 3-10 for far more important than 2?
1. Think again, what other developers (who finish work on time) do, that you do not. Theres always something else than simple hardwork. Maybe smartwork? planned work? more intelligent work? more skillful work? Combination of all that defeats timeline issues.
1. Do this every day. It is 100% that all need improvement. Find out things that you can improve. Doing this daily and consistently is the key.

To be continued

### Change in requirements
#### I created something and it got changed. Why?
Change in any project is "normal". Change could be due to many reasons; for improvement or business needs or any other. Of course everytime a change happens, a new story is written. New design & strategy, new requirments and new estimates could be a normal thing to do again. Change -> new story -> new strategy === normal process of project

#### Ok but if it had to change, why did we do it like that in the first place?
Sometimes we don't know what the future will be. And sometimes we do know but despite that we do not do many things due to many reasons e.g but not limited to, priorities, business needs for the current time, not being fully sure of future features or even those will be needed in future.

## Project management tool
#### Task / issue types
1. Epic - For requirements and vision. This is the super main end of top most hierirachy. Its children may and usually are divided into multiple sprints
1. Story - For requirements and vision. 
1. Bug[SL/BK/JS/D] - A defect in delivery for slicing / backend / Javascript / Design.
1. Test[uFE/uBK/iFE/iBK/e2e] - Tests for unit test for frontend, unit test for backend, integration test for frontend, integration test for backend, end to end test.
1. Slice - HTML CSS slicing mostly
1. Back - Backend
1. Estimation - Requirement understanding and estimation time. This does not include development time. However if something is so unclear and very small amount of development is needed (usually less that 5%), it can be included in it. But 95 to 100 time is usually spend on research and requirement understanding.
1. Research - Only or mostly research (95% above)
1. JS	- Javascript		
1. Design - Graphic design (Adobe photoshop, Illustrator etc)

#### Task understanding
After reading the issue type, description and title of the task carefully, read the parent task (story or any other kind of ticket) and read all the way up to the top most ticket. Most of the times, major portion of requirements for your specific assigned ticket would be in the parent stories.

#### Execution
1. Observe due date, estimated hours and discuss if needed
1. Change status of task to "In progress" at the moment you start working on it. This is important to do as other stakeholders will know what is being started and being done.
1. During the work in progress, keep on changin the percentage done accordingly.
1. When finished, create PR (git pull request) and paste the link in the parent story of that ticket. Usually there should be an individual PR and branch for each story and its functionality. Code of other tickets and functionality should usually not be in it. 
1. After that, mark it as "Completed" and percentage done to 100%. A task should be marked complete if only PR 1 and PR 2 are created flawlessly.
1. The task will be reviewed, and status will be changed to "Approved" (in which you do not need to do anything further) or to "Rejected" (in this case you should make the task status to "In progress" and then "Completed" again after fixing the objections raised).

#### Do it yourself
1. Do what was written in description of task + parent tasks (when instructions in parent are in scope)
1. Please do the needful in order to declare the task as complete / change in progress via percentage or status etc.
1. Move to next task and change its status as well (and percentage when needed).
1. Do this automatically every time yourself so you do not have to be reminded for each ticket.

#### Priority
Of course, start a the tasks with most highest priority first.

#### How to see my tasks
1. You can click "my page" button at top left corner but it will show limited tasks. To see full task list of all projects, you should click "projects" at top and then "issues" menu. Or simply got to "/issues" url. If graphical gantt view is required, you can click "gantt" menu or simply go to "/issues/gantt".
1. You can play with filters above the tasklist displayed. For example, if you uncheck "assignee", you will see all tasks in all projects.
1. You can also use the shortcut links at the right side. E.g "custom queries" > "assigned to me" and ask manager to create more for you if needed

#### Your work time
1. Each day, the total estimated time of tickets done by you should be equal to the daily work time expected from you. The ticket estimated time is entered by project manager and is viewable in the field "Estimated time" in each ticket.

## Estimation
1. Estimation is the process of understanding the requirements first.
1. Then coming up with an action plan (tools, libraries, frameworks, process and so on with a long list of connected things).
1. The main purposes of estimations are only two. Understanding with action plan and time to complete.
1. Time spend on estimation (which means all the above), is usually 2% to 10% maximum of the total time to develop the application. 1. There is no limit on how deep someone can go in understanding, polishing a diamond, optimizing something. A developer can make a login page in 1 hour and in 100 hours as well (trying to keep on beautifying and optimizing and adding features).
1. Time to estimate, with smartness, should be of balance (not too low to not have unclarity and not too high to not waste time).
1. See [getting-things-done](#getting-things-done) for more information

### Sample estimation
Suppose you have to make a login page. How much time will it take? You answer might fall between 2 hours to 1 week. All depends on the joint mixture of requirements, your understandings, your skillset. Lets make a WBS and estimate
1. 1 hour : BK: Backend datababase design
1. 2 hours: BK: User authentacation (middleware and routes)
1. 0.5 hour: SL: Frontend slicing
1. 1 hour: JS: Javascript interactivity

Ok, good. you go 4.5 hours of work. But 
1. How will the frontend page look like? 
      1. Will we use bootstrap, matarial ui, foundation or custom code?
      1. Will we use sass? or plain css is fine?
      1. Will we use javascript for animation or css?
      1. Will we use html5 validation or Javascript based or react based validation?
      1. Any library we will use?
1. Which libs to use for JS
      1. Will we use captcha?
      1. Will we use 2 factor authentication
      1. Will we use redux?
1. What measures to take for backend
      1. Libs?
      1. Security precautions?
      1. So on.
      
#### Finalize understanding first
This is just an example, there will and must be many other questions (assuming that the requirements were not clear enough). We have to make them clear then and provide WBS based estimates. If anything is missing, explore and ask.

#### Nothing is missing but I don't know estimates.
If this is the case, there can be the folowing or more reasons
1. The task is not of your level and you need to learn before implmenting. In this case, the "specific" thing you have to learn and the time for that should also go in WBS. Once thats done, further WBS will continue (portions dependant on it).
1. You have not done enough effort to breakdown the WBS properly. If so, do it.
1. None of above but the task is a bit new to you or you have not done this before OR things are of unclear or unpredictable nature. In this case (which is rare), make a POC (proof of concept). e.g you are not confident on an api integration. In this case, quickly make POSTMAP calls and check it. If this is the case, the "specific" thing you will make POC "without which you cannot proceed", should also go in WBS. Once thats done, further WBS will continue (portions dependant on it).
      
#### Your duty to clear up requirments
Clients, product owners, project managers may try their best to clarify things but it is your duty to clear up requirements and make up your understandings in such a way that the product owner or project manager does not says "Why you did this? where is that feature? this should have been done differently or this is missing". So clear up scope of responsibility before giving estimates and far before performing any development.

#### Correct estimation - exaeplary
1. 1 {hours} : Estimation and understanding requirements
      1. 0.5 {hours} : Basic understandings of task
      1. 0.5 {hours} : Talk, Research on xyz // If unclear things/ POC needed. This should be done before any other execution or final estimation of xyz or related things
1. 1 hour : BK: Backend datababase design
      1. {hours} : {Item} // core thinking, designing
      1. {hours} : {Item} // creating schema in knex migration
      1. {hours} : {Item} // test cases // further sub divide into kinds of tests
1. 2 hours: BK: User authentacation (middleware and routes)
      1. {hours} : {Item} // setting basic routes
      1. {hours} : {Item} // writting middleware
            1. {hours} : {Item} // redis database implementation
            1. {hours} : {Item} // midleware finalization with redis + session + cookies
      1. {hours} : {Item} // test cases
            1. {hours} : {Item} // integration tests
            1. {hours} : {Item} // unit tests
1. 0.5 hour: SL: Frontend slicing
      1. {hours} : {Item} // html part
      1. {hours} : {Item} // css part OR sass part
1. 1 hour: JS: Javascript interactivity
      1. {hours} : {Item} // core
      1. {hours} : {Item} // Integration tests

#### What happenes if estimates do not match outcome
Your job performance score will be affected.

# You
## Who are our favourites? Top qualities?
Weighed according to numbers below
1. Number one quality we appreciate is not skills, appearance, experience etc. Number ONE qualities are combination of two.
  - Compliance / responsible behaviour : Not letting us repeat ever- Anything informed and instructed once, should never be needed to be repeated, should happen and complied in future with care. 
  - Dedication - You should work hard with your heart and motivation. A determination to become better. If you have these two qualities, you just got passed 50% acceptability already. Rest will follow (for us and for your career).
1. Your skills
1. Your experience
1. Your qualification

# Coding and development

## Getting things done

#### Do only whats required
1. **Only do whats needed**. Nothing less, nothing more. Your time is precious. You should be focussed on your **specific targets and goals**. Your time on job is company's **valuable asset** as your targeted efficiency in it is the efficiency of the company! We want to see you valued.
1. If you see something wrong or a room for improvement, **ask permission beforehand** for any deviations because if you think something is beneficial, that may not be the case with a different perspective, it may have **side effects** or simply it may be be very **good but not needed at the time** or at the cost of the current time. So simply **ask lead/manager and discuss first**.
#### Improvment
1. You might be thinking **then, how do we improve the code/funcitonality?** Of course, you do but **in steps**. **First target is to complete in a 'good way' and 'as instructed' but not in a 'perfect way'**. 
1. Perfection is a step by step process and the steps may reach infinity in some cases. We will not be able to afford time loss for completion at the cost of long perfection sessions. 
1. So in short, get first stage workable. Get it approved, move to next stage, get it approved and so on. Do not try to reach stage 10 by wanting to learn and experiment for 9 prior stages in one go. 
1. **If your code**, on the other hand, **is below standards**, you will ultimately get **PR issues anyway**... Remember them and do not repeat them. So you/your code improves any way by default. 
1. But keep a fine line between personal part of pure self learning (with self motive only) and self experimenting vs completing the task as priority and **learning through that** (which will be done any way during the process so everyone gets happy).
#### Smart done
Suppose you have 10 things in your todo list. **5 things 100% done is better than 10 things done 50% each**.
If you have multiple things, do one by one, but each fully complete.
If you have only one thing, divide it into parts. Do those parts one by one, each complete at a time.

#### Definition of done
Completion of a task with minimum acceptable qaulity (does whats needed, passes lint and code review etc).
## Coding practices
#### libraries choice
You should have very good reasons to choose a library. In most of the cases, you should **ask lead before choosing a library**.
#### ES6+ over old
**Always use ES6+ syntax over old. Take it as a mandatory rule**.
#### TS over JS
If your project is Typescript based, **use Typescript wherever possible**.
#### Tests
We use **Jest** as the testing library for unit tests and integration test and **Cypress** for automation e2e tests.

## Javascript
#### Never disable linting
Do not disable linting without permission.

## Frontend
#### css over js
**Only** use css/scss (scss preferred) for libraries like material ui etc that offer both Javascript based style configurations and css based style configurations. Put css/scss code in separate files for each component. There should be no inline styles as well. This strategy is important as it increases page performance a bit and also decouples development. A css coder can work (almost) independantly from a javascript developer on the same projects. Spliting css and js files also improves the said. Further more, it also decouples style (css) and interation (javascript) logic, giving better structure to code as well.
##### External cdn or other links
Never use (until informed by manager), any kind of external links of css, images, javascripts in html or js files like `<link src=.../>` or `<img src.../>`. It is agreed that resource loading via third party increases performance and decreases server/network load but specially in a SAAS app or single page app (SPA), we use our own optimized and/or bundled resources and/or if its PWA, this goes further strict as caching is involved. So do not use third party linked resources. Use `import`.
#### Images
Extending above point further, to use images or make them background etc, use image paths in css/scss files as css/scss syntax.

## Frontend react
#### One file per component
Create one js/jsx file and one .scss file for each component. Do not worry about more files and directories. Worry about more number of lines in one file. Create a separate scss/css file for each componenet .jsx file even if the component is small enough or the scss/css file have fewer lines of code.

# Efficiency
#### consistency
Be consistent in choosing, using, following architecture, libraries, patterns
#### reusable and modular code
Do not repeat your self
#### CPP 
commit, pull, push in **same sequence**. Do this as frequently as you can. Sequence is important. Commit first, then pull (from your branch AND from default branch at least), then push (to your branch). E.g For a **team of X number of people, you should do it X times a day**. Ie in a team of 3 people, you should do this at least 3 times a day. 



# Directory structure
### Frontend react based
```
src
    components (or modules)    
        base
            shared
                menus
                    xyzMenu
                        xyzMenu.jsx
                        .scss
                buttons
                    xyzButton
                    abcButton
                accordians
                    abc
            header
                headerComp.jsx
                headerComp.scss
                level
                    levelComp.jsx
                    levelComp.scss
                Balance
                    // 
                    //
                notifications
                    //
            navBar
            drawer
        tasks
            list
                taskListComp.jsx
                //.scss
                taskListItemComp.jsx
                //.scss
            task
                taskDetails
                    taskEdit
                        taskEditComp.jsx
                        //scss
                        taskRuleDetailComp.jsx
                        //scss
                    taskPreview
                        taskPreviewComp.jsx
                        //scss
                taskTabs
                    taskInfoTabComp.jsx
                    taskSampleTextTab.jsx
        dashboard
                //
                //
                //
        projects
                //
                //
                //

```
### Backend nodejs
The following is incomplete but gives an idea
```
src
      base  // having shared things or base core things
            controllers
                  // files or directories having files
            service
                  // files or directories having files
            middleware
                  // someSharedFunctionalityOrDirName
                        // someMW.js
                        // someOtherMW.js
            utils
                  // files or directories having files
            i18n  // contains language files for backend and frontend.
            // note: later this can be turned as module imported independantly
                  base
                        // base files to access / respond i18n for backend and frontend
                  public // bundle of auth + contact page + any other
                        fe    // language files used by frontend
                              en.js
                              tr.js
                              fr.js
                        bk    // language used by backend
                              // same structure as above
                  user (profile + dashboard + settings module) // same directory structure as of public module above
                  someOther   // same
      modules
            public      // includes things that can be used without login
                  auth  // auth module containing login, change password, register, etc
                        controller
                              loginCtr.js         // functions name: someCtr();
                        service
                              auth.js                    // functions name: some();
                              //some other
                        dao // database access object
                              loginDao.js                // functions name: someFuncDao();
                        utils
                              loginUtils.js              // // functions name: someUtil();
                  someOther
                        // same directory structure as above
            user     // access after login
                  userProfile 
                        // same directory structure as in auth module above
                  userDashboard 
                        // same as above
            someOther
                  // same as above                                               
```


# Configuring development environment
#### CORS restrictions
If you get CORS errors, you can install browser plugin (one called `allow cors` for chrome). You have to hit the big icon and make it colored to activate it.
#### Localhost nginx config 

Note: 
1. Replace `projectName` with real project name
1. You can use different ports for each project. e.g 4321 (backend) + 5321 (frontend) for one project and 2321,3321 for another. 6321,7321 for another, 8321,9321 for another.
1. Avoid port 3000.

Put entries in host files. 
`sudo nano /etc/hosts`

add
```
127.0.0.1       projectName.com 
127.0.0.1       api.projectName.com
```
hit ctrl + o or command + o
```
sudo apt install nginx Use homebrew for mac of course
sudo nano /etc/nginx/sites-available/projectName.local  (different location maybe for mac)
```

add

```
server {
    server_name projectName.com;
    root /tmp;
    location / {
        proxy_pass http://localhost:5321;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_http_version 1.1;
        proxy_set_header Host $host;
    }
}

server {
    server_name api.projectName.com;
    root /tmp;
    location / {
        proxy_pass http://localhost:4321;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_http_version 1.1;
        proxy_set_header Host $host;
    }
}

```
Change ports in above script if you have multiple projects.

```
sudo ln -s /etc/nginx/sites-available/projectName.local /etc/nginx/sites-enabled/
sudo nginx -t
sudo service nginx restart
```

# Tech notes
## Backend
### Node.js
#### Knex transactions
Any database access objects DAOs should not be declared or called without trx.
Sudo code:
```
try
  await knex.transaction(async (trx) => {
     other code
     const v = await someDao(trx, param, param)
     other code2
     const v2 = await some2Dao(trx, param, param)
  });
catch
```
Related code and DAOs can be grouped in knex.transaction block. If code is not related, you can have multiple separate knex.transaction blocks isolated.

# Online remote groups
#### Noise due to group talk
If you feel theres **too much voice conversations** in remote group, you can **mute the volume** but you should **be alert for any chat messages**. If some one wants to talk to you, (s)he should ping you on chat. You should do the same.
#### Stay connected all the time
You should stay connected to group collaboration software all the time
#### Personal info
1. Sharing of any personal information or discussing anything not related to work/current tasks is treated as a miss conduct.
1. Using any personal email, phone or contact in any platform, such as but limited to, github, collaboration, chat etc tools is treated as a miss conduct.

# Daily routine
## What to do at day start
Do the following in exact sequence
#### Log in start time
in attendance app if provided to you
#### Message manager
about your presence and check your emails/messanger/app for any messages that may need your attention.
#### Keep communication app onn
Whatever is your persistant communication medium, make sure it is always connected and available during sign in and sign off time
#### Refresh task list
assigned to you and observe any changes (specially priority and dates) and act accoringly.
#### Plan or ask questions
If anything is unclear for the day ahead, ask questions from manager. If all is clear, plan what to do next.

## What to do at day end
Do the followings in exact sequence
#### Work and tickets complete
Make sure the work assigned to you for the day is complete. Take good care to make sure that the git PR, PM tool ticket fields and all required things are complete and accurate.
#### Plan or ask questions
If anything is unclear for the next day, ask questions from manager. If all is clear, plan what to do next.
#### Message manager
at least 1 hour to 45 minutes before signing off so (s)he can discuss things or collaborate with you if needed.
#### Log sign out time
in attendance app if provided to you

## Attendance
#### Late sign-in
You should not come late in any and all cases unless you have explicit permission to come late from your manager or HR for that day. Few resources might want to or had worked late in the last working day. This does not except them from coming on time on the next day.

#### Early signout
Early signout is not allowed. If you do, you should spend that time in the next day in addition to the days time. If you think you have completed your tasks before dayend time, **a)** thinkg again and make sure they are fully completed **b)** if they are completed, ask for next tasks if project manager is available. If project manager is not available, start reading and understanding the next stories and tasks for future. 

# Penalties and rewards
Bright career of developer and quality and efficient work at company side demands discipline. Time of developer is precious and time of reviewers and managers is costly and cannot be used to keep on entertaining, informing, correcting and explaining same or similar things repeatedly. This is simply not viable nor affordable. Thus following penalties apply and will be modified from time to time.

However, rather being appreciative also on diciplined and well mannered, responsible employees, we also announce rewards!

Model type assigned (single or multiple) to you will be informed to you by your manager.

### Terms / definition
1. Time duration: Week: starts at 1 hour after office start time on Monday. Ends at the same time next Monday.
1. Rule/ Penalty point/ penalty: One point broken one time is one count per time duration. Multiple penalty count if same point broken multiple times per time duration. Penalty will be charged each time a rule is broken. This can be once or multiple times per day. E.g You made 2 PRs with lint errors in both, and third PR had console errors in browser. You will be changed 3 penalties. Next day you did the say. Again 3 penalties totalling 6. Then on same day he put his name in code. Not total penalties are 7.

#### Default reward (Model A)
If rule breakage count is less than 3 in a week, you will get 5% of your base salary as bonus reward per for that week. E.g your salary is 10,000, you will get weekly 500 bonus.

#### Default penalty (Model A)
If rule breakage count is more than or equal to 3 in a week, you will not get any kind of bonus in any plans or models, e.g but not limited to FIB.

#### Default penalty (Model B)
Penalty amount per penalty is 1% of your monthly salary. E.g if your salary is 10,000, penalty is 100.
This is default amount unless penalty amount is provided differently in any rule).

#### Note for managers.
If a manager knowingly does not reports (to management) a rule breakage by employee, he will pay 10 times of the penalty from his own pocket to the company.

#### Written approvals
Any exception permissions or written approvals should be kep saved by employee for future reference. E.g snapshot of chat, email etc. Else the approval is not valid.

## Code reviews

#### General
1. Use of any library or framework without written approval in non-PR-1 PRs or which is not in the approved list mentioned here. Managers should also create and publish a list off approved libs, framework for PR-2/3.
1. Use of any (unapproved in writing) library or framework or tool that creates/writes code for you. For example, but not limited to, create-react-app from create-react-app.dev website
1. Repeating a mistake (small or large) that was previously corrected by a lead/manager/reviewer (penalty is half of default penalty in this case)
1. Not being able to create a stable PR at least one and half hour before end of signoff time.
1. Not reviewing a PR (of someone else) within 2 hours of being informed.
1. Providing a PR title that is not the ticket name nor self explanatory.

#### General coding
1. Giving unclear variable/ function/ class names. E.g `maxSize` does not tells what it is and unit of measure. Instead it can be `maxUploadFileSizeInMB` or `upload.maxFileSizeInMB`. In short, when a person sees the name, he should exactly know what it is.
1. Not following the file, variable, function or class naming conventions stated in this doc e.g but not limited to having controller abreviation in controller files and functions.
1. Not following directory structure stated in this doc. E.g but not limited to controller, dao, service directories
1. Using console logs without a logger library or logger function.
1. Using strings or numbers that cannot be referred from configs, constants or cannot be auto completed while coding via Intellij Idea IDE. (exceptions of course are config files, constants, typescript types etc that actually provide the feature to be referred by other consumers)
1. Keeping unused code in middle of file. Put them at bottom of file.

#### Configs
1. Not using database name, user name, password same as project name (without hyphens). e.g `some-name-bk` can be `somename`
1. Using ports other than x321 port numbers where x can be from 1-9
1. Commiting your own configs that work for you but no need for other developers. E.g putting your own different database name or username and committing, pushing it.
1. Changing configs like eslint, babel, package.json scripts etc: Change of configs should not be done directly but via change in tpl projects or modules (whatever had been made and used for the project).

#### Linux compatibility
1. Creating PR that is missing code for or is incompatible or is not tested on ubuntu LTS operating system.
1. Not testing with nginx/apache with hosts file based local domain.

#### Personal info
1. Putting real names of anyone (instead of `user, user1, user2` in any part of code, image or any kind of asset/document or communication medium in any form.
1. Putting any kind of personal info that is not official. For example, but not limited to, personal email or phone in any part of code, image or any kind of asset/document or communication medium in any form.

#### All languages
1. Creating PR with console errors in browser, network tab errors in browser, application tab in browser or commandline erros of any kind. Or PWA service, application, cache errors.
1. Creating PR without minimum test coverage in each category (stated in this document). Test coverage should be provided by manager in project readme file or via email.
1. Creating a PR where app does not starts or tests do not run or run with errors.  
1. Not taking pull from master and daily-stable-master branch before making PR

#### Javascript, Typescript
1. Creating PR with lint errors, TSC errors, terminal/console errors, browser console errors. Lint and TSC errors are not just errors shown in IDE but also via command line and scripts for example, but not limited to, eslint commandline, TSC commandline, browser console errors (even if your project uses webpack or some other automation tool / script to compile).
1. Creating PR with compile or transpile errors e.g but not limited to, by babel, typescript compile (tsc), webpack, etc.
1. Changing, suppressing or disabling any project base configurations like eslint rules, tsconfig, esconfig, babel, package.json scripts
1. Using raw string based knex queries where proper knex syntax is possible. (one fourth of default panelty per query)

#### Typescript
1. Use of `any` or `unknown` without written approval
1. In typescript, using any non-javacript feature other than providing types (temporary rule for now).

#### Frontend / react
1. Coding inline (s)css styles or any kind of view code in any way inline. It should go in separate file.
1. Coding (s)css styles or any kind of view code in any way in react component file or file having html code. It should go in separate file. Even if the style is not a pure (s)css syntax but some object like of material ui parameter etc, anything to do with styles goes in a separate file with style name in file name or a .scss. If former, style object can be imported in the view component file and used.
1. If more than one components are using a child component and passing the same props every time (or it is anticipated in near future), then that called function (or wrapper of it if its a third party lib), should have default prop values that can be overriden when and if needed)

#### React
1. Referencing any third party css, javascipt resource other than including it in bundle.js as code. You should use `import` lib from `package` (Valid rule if bundling is used)

#### Java
1. Not using maven or gradle for dependancies but adding lib files directly
1. Not testing with .jar before PR

### Python
To be added soon

## Routine

#### Attendance
1. Not informing timely (at least 24hours) in writing before a non-emergency leave.
1. Not following "Daily routine" section on what to do at day start and day end. 
1. Not taking mandatory break from work for at least 30 minutes.

#### Behaviour
1. Not followin anything mentioned in appointment, policy, practices or any ammendmends in the said things. 
1. Asking for information that is already clearly present in appointment, policy or practices documents. This means employee had not carefully read the said and is irresponsibly consuming managemnt's time. However, if something is really missing, we welcome questions.

# List of libs/framework approved for PR 2/3
```
    All exact version number of libs mentioned in tpl project package.json
    any @types for typescript
    "@material-ui/*": "4.*",
    "clsx": "1.*",
    "material-table": "^1.68.0",
    "moment": "^2.27.0",
```

# Tutorials
## Javascript Misc

### Javascript core 
official first priority tutorials
1. https://developer.mozilla.org/en-US/docs/Web/JavaScript
1. https://tc39.es/ecma262/ || https://ecma-international.org/ecma-262/10.0/index.html || https://github.com/tc39/ecma262
1. Other references https://developer.mozilla.org/en-US/docs/Web/JavaScript/Language_Resources

### Recommended authors
1. Lynda/ Linkedin learning
1. Academind https://www.youtube.com/channel/UCSJbGtTlrDami-tDGPUV9-w/playlists


## Backend Node.js

### Node core
1. Lynda Node essential training by Alex banks

### Testing coverage
1. Statement coverage https://www.youtube.com/watch?v=9PSrhH2gtkU
1. Branch coverage https://www.youtube.com/watch?v=JkJFxPy08rk
1. Condition coverage https://www.youtube.com/watch?v=ZnPmJd5aqyw
1. Modified decision / condition coverage https://www.youtube.com/watch?v=DivaWCNohdw

### Testing libraries
1. React https://reactjs.org/docs/test-utils.html
1. Some good testing lib comparisons https://stackoverflow.com/a/54152893
1. Testing intro https://www.youtube.com/watch?v=r9HdJ8P6GQI
1. Cypress https://www.youtube.com/watch?v=LcGHiFnBh3Y
1. Enzyme vs React-testing-library https://youtu.be/SyAYO5w-nUI?t=1987
1. Enzyme shallow vs mount https://youtu.be/4_pZizupR7U?t=884
1. ~~Api testing https://youtu.be/7VNgjfmv_fE?t=381  to 5 mins (the later code for mongo is irrelevant). The same logic can be applied for Jest~~ Disregard this.

#### Enzyme 
1. Basic info and examples https://enzymejs.github.io/enzyme/
1. Setup https://enzymejs.github.io/enzyme/docs/guides/jest.html

### Mock testing
1. Mock libs and data https://www.youtube.com/watch?v=4Fl5GH4eYZ8&t=909s, https://youtu.be/Ngj2f1n9pUw?t=459

## Frontent React

### React core
1. Lynda React essential training by 

## Git / github

### Git
1. Pull request/ Merge request: https://youtu.be/uPt-bP_bKmQ
1. Forking at github https://www.youtube.com/watch?v=nT8KGYVurIU
1. Lynda Git Essential Training: The Basics with Kevin Skoglund

### Github
1. Lynda Github Essential Training

## Project tool
### Info gathering
1. Project tool - Info gathering https://youtu.be/vt4ymkGjco8
1. Project tool - why divide story into different tasks https://youtu.be/9e_hn905-tw

## Basics

### Algorithms
1. Big O notation https://www.youtube.com/watch?v=IR_S8BC8KI0

### Architecture for newbies
1. Basic app architecture and learning - https://youtu.be/OmZhSqgo6TQ
1. node backend newbie 1 - https://youtu.be/T7oYz2rICsc
1. react intro newbie 1 - https://youtu.be/CWNX5U_spmE
