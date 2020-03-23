- [Git](#git)
      - [ssh keys](#ssh-keys)
- [Node, npm](#node--npm)
      - [nvm](#nvm)
- [IDE](#ide)
      - [Intellij idea](#intellij-idea)
- [Operating system](#operating-system)
      - [Kubuntu](#kubuntu)
      - [Windows](#windows)
- [Pull requests / merge requests](#pull-requests---merge-requests)
  * [PR per feature](#pr-per-feature)
      - [PR part 1](#pr-part-1)
      - [PR part 2](#pr-part-2)
      - [PR part 3](#pr-part-3)
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
- [Docs](#docs)
  * [API docs](#api-docs)
  * [Code docs](#code-docs)
- [Project management](#project-management)
  * [Agile](#agile)
      - [story points](#story-points)
      - [stand up](#stand-up)
      - [sprints](#sprints)
      - [Ownership](#ownership)
      - [Deviations](#deviations)
  * [Project management tool](#project-management-tool)
      - [Task / issue types](#task---issue-types)
      - [Task understanding](#task-understanding)
      - [Execution](#execution)
      - [Priority](#priority)
      - [How to see my tasks](#how-to-see-my-tasks)
  * [Estimation](#estimation)
- [Coding and development](#coding-and-development)
  * ["Getting things done"](#-getting-things-done-)
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
      - [Localhost nginx config (not needed unless asked)](#localhost-nginx-config--not-needed-unless-asked-)
- [Online remote groups](#online-remote-groups)
      - [Noise due to group talk](#noise-due-to-group-talk)
      - [Stay connected all the time](#stay-connected-all-the-time)
      - [Personal info](#personal-info)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>


# Git
#### ssh keys
add ssh keys so you do not have to type password everytime and also you will need it for getting some of our private modules via npm. https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent


# Node, npm
#### nvm
Do not install node by any other means but only use nvm. Follow this link and use latest LTS version of node. https://github.com/nvm-sh/nvm and https://github.com/nvm-sh/nvm#usage  (go for the latest LTS node version)



# IDE
#### Intellij idea
We encourage intellij idea **Ultimate edition** (very preferred). If you do not have the license, then **at least community edition**. If you do not have the **hardware resources**, you should get them to run intellij. If not, the last case (not preferred) is **vscode**.

Note that you should have **minimum of 4Gb ram**. Minimum **8Gb recommened** with most **unused plugins disabled** (else you it will consume a lot of cpu and memory)



# Operating system
#### Kubuntu
**Kubuntu** (with k) LTS (**ONLY LTS**) versions are preferred. https://kubuntu.com
#### Windows
If you use windows, you have to do the following in package.json (we have not made special windows commands yet as we mostly use and encourage Linux. This is the same setup we use on servers. So environment differences would be minimum).

exclude   `.`  (dot) and `/` slash at line starts

replace `/`  slashes with `\` blackslashes

replace   `;`  with `&`



# Pull requests / merge requests
## PR per feature
1. A feature should be divided into following **main parts/categories** and all PRs should be passed step by step. 
1. There can be more PRs than the below stated but these are the minimum and more sort of **broad categories**. 
1. Developer should write the `category number` in PR title. E.g `login page PR category #1`. Developer should **not work/extend code based on same/previous PR functionality, until the first PR is merged/approved**. This is because if there are issues in the intial PR, then the extended code based on that intial PR code will also have issues and consume more and more time. Same philosophy applies to PR categories. E.g do not go to category 2 unless 1 is approved.
1. You should work on some other feature/project during wait time.
#### PR part 1
1. First PR should have all the possible **flow/achitecture with directories, files and empty functions** with //TODO comments inside (and interfaces if Typescript is used). This will tell the approace of the the developer, will help the developer envision the big picture/process/strategy. It will also get the code flow review at a much earlier stage and will eliminate gaps in expectations far ahead of time.
1. There are many approaches in industry to make flow before coding e.g **UML** diagrams, test cases (where test cases are written before writing actual code (**TDD** test driven development)), or simply writing **empty functions/interfaces** etc.
1. Some people may say, "**what if the code is likely or will change in future? is PR 1 useless?**". Well, no. If its likely to change at a greater percentage, it means the plan and structure initally made needed improvement. Secondly, if some of it will change anyway, the effort to make initial design should have given more advantage over the minor con/disadvantage (to just remove/change an empty function/file).
#### PR part 2
Each function/part in PR #1 will be **implemented** (with unit tests if it is enforced in the project)
#### PR part 3
This would be **final PR** and will also make sure that other parts of **application work in harmony** with the current task. If integration tests and/or automation tests are enforced in the project, this PR should have those too).

## prerequisits of PR
In order to get your code merged in master branch, you need to do the following. **Do not make a PR Pull request without the following first done**.
#### Create branch
Create a new branch by first cloning your project git repository, then creating a new branch from master. Start coding in it.
#### Pull from branch and master
Before pushing code for PR, make sure you have done CPP (commit(in your branch), pull (from your branch if others are working on it too. If not, then simply from master), push (to your branch))
#### CI
We do **contineuous integration (CI)** on github. **Make sure all checks are passed** and its a green tick with your pull request and commits.
#### linting
One of the CI steps is linting. You can **autofix** with npm scripts in package.json and then manually test for any lint errors before making a Pull request. **Manually fix** if something is not autofixed. As a side note, observe autofixed syntax and learn from it.
#### Tests
If your project has unit test/ integration tests/ automation tests enforced, do not file PR without them.
#### Self testing
All functionality should be tested before making a PR (self testing). Run and **test the functionality yourself first**.
#### Release notes
All PRs should have release notes about the functionality you made in that PR. It should briefly describe about the business flow, technical flow, any third party lib used and reason for its preference. This will have some **information that is not available in story points**. e.g any library used and why preferred, flow of code, technical precautions etc. This is very brief usually from **25 words to 100 words max**. 
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
**There should be one PR per day** (which is consisting of all PR part 1 + PR part 2 + PR part 3). **This is mandatory**. If you fail to get it approved, you have not achieved the full success of the day. You should file a PR before few hours of the day so it defintily get approved (assuming that it might have some issues and it might take you some time before dayend to resolve those issues and get the PR finally approved).

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
1. loginServices
#### Notes for names
1. Function and variable names can be a big long e.g even to 20 characters but they should **smartly** and **clearly** explain the meaning and purpose. I.e be **self explanatory**.



# Docs
## API docs
To be continued
## Code docs
To be continued



# Project management
## Agile
#### story points
#### stand up
#### sprints
#### Ownership
Sprints are ownership of the team overall, success of a sprint is success of the full team (regardless of individual tasks). You can say you may hold at least 1% to 10% responsibility of overall team work. You own 100% of the taks specificily assigned to you. Responsibility includes, but not limited to, completing the task with at least minimum quality and absolutely agreed time mentioned in estimates.
#### Deviations
If you encounter any deviation in attainable preplaned timeline estimates, promptly inform the reasons and circumstances to your lead and project manager. Inform far ahead and as soon as possible when deviations are anticipated. NOT at the end or when time had elapsed.

## Project management tool
#### Task / issue types
1. Epic - For requirements and vision. This is the super main end of top most hierirachy. Its children may and usually are divided into multiple sprints
1. Story - For requirements and vision. 
1. Bug[SL/BK/JS/D] - A defect in delivery for slicing / backend / Javascript / Design.
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
1. When finished, create PR (git pull request) and paste the link in that ticket.
1. After that, mark it as "Completed" and percentage done to 100%.
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
1. Time to estimate, with smartness, should be of balance (not too low to not be unclarity and not too high to not waste time).
1. See [getting-things-done](#getting-things-done) for more information


# Coding and development

## "Getting things done"

#### Do only whats required
1. **Only do whats needed**. Nothing less, nothing more. Your time is precious. You should be focussed on your **specific targets and goals**. Your time on job is company's **valuable asset** as your targeted efficiency in it is the efficiency of the company! We want to see you valued.
1. If you see something wrong or a room for improvement, **ask permission beforehand** for any deviations because if you think something is beneficial, that may not be the case with a different perspective, it may have **side effects** or simply it may be be very **good but not needed at the time** or at the cost of the current time. So simply **ask lead/manager and discuss first**.
#### Improvment
1. You might be thinking **then, how do we improve the code/funcitonality?** Of course, you do but **in steps**. **First target is to complete in a 'good way' and not in a 'perfect way'**. 
1. Perfection is a step by step process and the steps may reach infinity in some cases. We will not be able to afford time loss for completion at the cost of long perfection sessions. 
1. So in short, get first stage workable. Get it approved, move to next stage, get it approved and so on. Do not try to reach stage 10 by wanting to learn and experiment for 9 prior stages in one go. 
1. **If your code**, on the other hand, **is below standards**, you will ultimately get **PR issues anyway**... Remember them and do not repeat them. So you/your code improves any way by default. 
1. But keep a fine line between personal part of pure self learning (with self motive only) and self experimenting vs completing the task as priority and **learning through that** (which will be done any way during the process so everyone gets happy).
#### Smart done
Suppose you have 10 things in your todo list. **5 things 100% done is better than 10 things done 50% each**.
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
We use **Jest** as the testing library for unit tests and integration test. For automation test, the choice is of project manager.

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
commit, pull, push in **same sequence**. Do this as frequently as you can. Sequence is important. Commit first, then pull (from your branch AND from master at least), then push (to your branch). E.g For a **team of X number of people, you should do it X times a day**. Ie in a team of 3 people, you should do this at least 3 times a day. 



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
      modules
            login
                  controller
                        loginController.js
                  service
                        authService.js
                        //some other
                  dao // database access object
                        loginDao.js
                  utils
                        loginUtils.js
      shared
            services
            utils                                                 
```


# Configuring development environment
#### CORS restrictions
If you get CORS errors, you can install browser plugin (one called `allow cors` for chrome). You have to hit the big icon and make it colored to activate it.
#### Localhost nginx config (not needed unless asked)
To be continued



# Online remote groups
#### Noise due to group talk
If you feel theres **too much voice conversations** in remote group, you can **mute the volume** but you should **be alert for any chat messages**. If some one wants to talk to you, (s)he should ping you on chat. You should do the same.
#### Stay connected all the time
You should stay connected to group collaboration software all the time
#### Personal info
1. Sharing of any personal information or discussing anything not related to work/current tasks is treated as a miss conduct.
1. Using any personal email, phone or contact in any platform, such as but limited to, github, collaboration, chat etc tools is treated as a miss conduct.
