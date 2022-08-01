% Last modified: 2022-07-29 19:52:58

Practice doc overview https://youtu.be/4q4eNV-Rczg

# Table of contents

- [Terminologies](#terminologies)
- [Work Flow](#workflow)
- [Development Env Setup](#development-env-setup)
  - [Git](#git)
  - [Node, npm](#node-npm)
  - [IDE](#ide)
  - [Operating system](#operating-system)
  - [Database Redis](#database-redis)
  - [Database postgres](#database-postgres)
- [Development process](#development-process) 
  - [Tests](#tests)
  - [Documentation](#documentation)
  - [API docs](#api-docs)
  - [Code docs](#code-docs)
- [Post development](#post-development)
  - [Release notes](#release-notes)
  - [Peer review](#peer-review)
  - [lead review](#lead-review)
  - [Pull requests / merge requests](#pull-requests--merge-requests)
  - [Daily PRs routine](#daily-prs-routine)
  - [Pull request / merge request model B](#pull-request--merge-request-model-b)
- [QA Quality Assurance](#qa-quality-assurance)
- [Development process](#development-process)
  - [CPP - commit, pull, push](#cpp---commit-pull-push)
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
  - [Code comments](#code-comments)
- [Project management](#project-management)
  - [Agile](#agile)
- [Work and self management](#work-and-self-management)
  - [Ownership](#ownership)
  - [Deviations](#deviations)
  - [Timelines](#timelines)
  - [I got late due to problems](#i-got-late-due-to-problems)
  - [Change in requirements](#change-in-requirements)
  - [Getting things done](#getting-things-done)
  - [Do only whats required](#do-only-whats-required)
  - [Improvment in steps](#improvment-in-steps)
  - [Smart done](#smart-done)
  - [Definition of done](#definition-of-done)
- [You](#you)
  - [Who are our favourites? Top qualities?](#who-are-our-favourites-top-qualities)
- [Project management tool](#project-management-tool)
  - [Task / issue types](#task--issue-types)
  - [Task understanding](#task-understanding)
  - [Execution in PM tool](#execution-in-pm-tool)
  - [Do it yourself](#do-it-yourself)
  - [Priority](#priority)
  - [How to see my tasks](#how-to-see-my-tasks)
  - [Your work time](#your-work-time)
- [Estimations and requirement gathering](#estimations-and-requirement-gathering)
  - [How can I improve estimate and execution](#how-can-i-improve-estimate-and-execution)
  - [What is estimation](#what-is-estimation)
  - [Sample estimation](#sample-estimation)
  - [Finalize understanding first](#finalize-understanding-first)
  - [Nothing is missing but I don't know estimates.](#nothing-is-missing-but-i-dont-know-estimates)
  - [Your duty to clear up requirments](#your-duty-to-clear-up-requirments)
  - [Correct estimation - examplary](#correct-estimation---examplary)
  - [What happenes if estimates do not match outcome](#what-happenes-if-estimates-do-not-match-outcome)
- [Coding practices](#coding-practices)
  - [libraries choice](#libraries-choice)
  - [TS over JS](#ts-over-js)
  - [Javascript](#javascript)
  - [Frontend](#frontend)
  - [Frontend react](#frontend-react)
  - [Code Efficiency](#code-efficiency)
  - [Directory structure](#directory-structure)
  - [```](#)
- [Configuring development environment](#configuring-development-environment)
  - [CORS restrictions](#cors-restrictions)
  - [Localhost nginx config](#localhost-nginx-config)
- [Tech notes](#tech-notes)
  - [Node.js Knex transactions](#nodejs-knex-transactions)
- [Online remote groups](#online-remote-groups)
  - [Noise due to group talk](#noise-due-to-group-talk)
  - [Stay connected all the time](#stay-connected-all-the-time)
  - [Personal info](#personal-info)
- [Daily routine](#daily-routine)
  - [What to do at day start](#what-to-do-at-day-start)
  - [What to do at day end](#what-to-do-at-day-end)
  - [Work and tickets complete](#work-and-tickets-complete)
  - [Plan or ask questions](#plan-or-ask-questions)
  - [Message manager](#message-manager)
  - [Log sign out time](#log-sign-out-time)
- [Attendance](#attendance)
  - [Late sign-in](#late-sign-in)
  - [Early signout](#early-signout)
- [Penalties and rewards](#penalties-and-rewards)
  - [Code reviews](#code-reviews)
  - [Routine](#routine)
- [List of libs/framework approved for PR 2/3](#list-of-libsframework-approved-for-pr-23)
- [Tutorials](#tutorials)
  - [Javascript Misc](#javascript-misc)
  - [Backend Node.js](#backend-nodejs)
  - [Frontent React](#frontent-react)
  - [Git / github](#git--github)
  - [Project tool](#project-tool)
  - [Basics](#basics)

https://luciopaiva.com/markdown-toc/
<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table 
of contents generated with markdown-toc</a></i></small>

# Terminologies:

1. **SM**: Scheduled meeting.
2. **PR**: github based pull request
3. **MR**: Mini online room (room dedicated for meetings where few (but 
   not all) are participants).
4. **Main Room**: Main online room where all should be present all the 
   time.
5. **Inform manager**: via whatsapp text message, discord.
6. **Inform team**: via zoom group text chat, google chat and voice.
7. **PM tool**: Project management tool that has tasks/ tickets in it.
8. **CPP**: commit, pull, push. Commit locally, pull from SO, push to your own origin in exactly this sequence.
9. **Own origin/your origin/** `OO`: When you make a fork of project from 
   SO, it will create a project in your own github account. That is your origin.
10. **Super origin** / `SO`: master repositories with preceeding `ab159ab
    ` in github git url. The repository where you should make PRs and get your work merged.

# Workflow

## Workflow cheatsheet
The following is a synopsis of quick access of workflow. You should still see details ahead of it.
1. Day start
    1. Message manager
    1. Update task statuses
    1. Check assigned tasks
    1. Do not do new tasks without fully finishing old tasks first. See 
       `General priorities and preferences` section below for more details.
    1. Start/resume tasks as per priority field in PM tool
1. At each SM
    1. Message in group, for SM; and participate
    1. Review PRs, get your PR reviewed and merged
    1. Sync up with team members (doer, pair, sto)
    1. Do CPP, resume tasks
1. At dayend
    1. Regardless of quantity of work, make sure your work is stable for public/client use.
    1. Delta reviewer reviews all PRs of the day in all projects (merged 
       or open) at last SM (within 15 minutes). Yes, all PRs be re-reviewed 
       within 15 mins. This will be a quick review. Not all can be reviewed
       . So things can be glanced or inspected in detail at ad hoc basis. However doing this every day is important.
    3. Message manager (that you are leaving) 10-15 minutes before leaving .
    4. Also message manager if you were not able to get at all the work done to be merged via PRs.
    5. (Temporary: make a very short list of mistakes/issues/inefficiencies 
       + brilliant work done by others + anything you like to improve and 
         send it to manager. So 2 headings: "Good things", "To be improved 
       + things" for things that whatever you have noticed in the day)
  
## Follow workflow religiously 
Please read this and follow consistently. All are adults here and need 
not to be reminded every time. These things are important and thus written 
with effort. Nothing further needs to be written any further to insist more.

## The most important thing
1. The most important thing to do here is be responsible and avoiding mistakes
   . This is the first and one of the most important trait that you should build. 
2. This does not requires a lot of time. It just requires a changed, improved attitude and behavior.
3. When one makes a mistake or is less careful (in any way regarding anything
   ), the effects are comparable to ripple effect. More people and their 
   time is often also involved. Even if not the case, the later tasks (
   which is based on initial work) is also affected. So its best to be careful in start. 
5. Sometimes its also not wise to overdo and cost of being 1000% perfect 
   is higher than the profit. Sometimes done is better than perfect. But 
   lets not go in that debate. 
   [definition-of-mistake](#definition-of-mistake) is quite clear in this article.

Links: 
[definition-of-mistake](#definition-of-mistake), 
[no-such-thing-as-qa](#no-such-thing-as-qa), 
[qa-quality-assurance](#qa-quality-assurance), 
[work-and-self-management](#work-and-self-management), 
[you](#you)

Videos: [#self-review](#self-review), 

## Unavailability
1. Inform manager about at least 5 minutes before taking any kind of long/short/lunch break 
2. Inform again on your return (to manager)
3. Do not be absent at the scheduled meeting times unless special permission is given

## Lunch / rest break
1. It is **mandatory** to take at least **30 mins break** during a day 
   and it should not be during the first 2 hours or last 2 hours of work day time or during SMs (Scheduled meetings).
1. Normal time is 1 hour break. 1 hour 30 mins on Fridays for Muslims.
1. You can take break anytime during the day except the above mentioned times. Just inform manager 10 minutes before taking break and inform when you return via his personal chat tool (discord etc).

## Blockers
1. If you ever get into blockers (e.g PM tool not running, system crash 
   for more than 5 minutes, or any other disability for more than 5 minutes
   ), Anything that limits you to work, you should message your manager 
   at your earliest (and call if no timely reply/he is busy).
3. If you do not inform AND get an acknowledgment from manager (that he 
   knows about it), it will be considered that you were not working that time. 
   I.e work hours will not be considered.

Links: 
[online-remote-groups](#online-remote-groups), 
[remote-collaboration](#remote-collaboration) 

[estimations-and-requirement-gathering](#estimations-and-requirement-gathering)
[#coding-and-execution](#coding-and-execution)

[cpp---commit-pull-push](#cpp---commit-pull-push),
[#project-execution-workflow](#project-execution-workflow)
[#coding-and-execution](#coding-and-execution)  
[no-such-thing-as-qa](#no-such-thing-as-qa) 
[daily-prs-routine](#daily-prs-routine)

## General priorities and preferences
**Top ones to be done first**. This is a list on what to do things first 
if you have multiple things:
1. **Delegation** - any tasks on which others' work is dependent. It can be, but not limited to
    1. PRs reviews (you doing PR review of others)
    2. assigning tasks to others
    3. explaining tasks to others while you delegate
    4. actually planning on how to delegate (maybe at start of the day/sprint etc)
1. Your **old work**. 
    1. Your old unmerged PRs.
    2. Anything pending, unfinished things (before you move to new things
       ). Do not do new things unless old things are concluded.
1. **Clarity of vision** and strategy for new things.
1. **Normal tasks** - See pm tool or task sheet for priorities and start
   your tasks as per highest priority first.
3. Notice that your normal/new tasks are at the end of priority. 

Video: 
[#project-tool](#project-tool), 
Link: 
[#project-management-tool](#project-management-tool) 
[#activity-sheet](#activity-sheet)
[initial-strategy-making](#initial-strategy-making)
[do-only-whats-required](#do-only-whats-required)
[#project-execution-workflow](#project-execution-workflow)


# Task allocation between members
## Kind of team members
No one should do a task fully alone. There will be at least 3 roles (usually 
each role belongs to a different person but sometimes 1 person may have 2 roles and other may have 1 role). 

One himself, One **pair** and one **strategic owner (sto)**. For example 
for a task or sub task, one person will may do coding, the other may do 
api tests. Or one may do frontend, other may do backend. This can go vice 
versa in the next task but the sequence of work flow described above should not change. 

## STO
The sto is responsible to be aware and to review the high level strategy 
of each task. But that does not excludes strategy responsibility from the 
other two executors by any means. STO can simply overrule and review strategy
. But if doer/pair doubts this, they should talk to the manager.

# Important rule of task execution
The following are the litmus paper tests, important rules the will determine 
if the task is executed correctly or not. At all points in time, for any sprint, any task, any person, any team member
## Team coordination
1. Task should have at above 3 roles (2 pairs and a sto).
2. Task should be executed in such a away that suppose, if one of the 3 
   members  vanishes/disappears in thin air, the others will not be confused
3. . Because each of the others will know exactly what and how the vanished person was doing. 
4. Ones a "one single smallest identifiable" task is completed, and reviewed  
   by manager, there should be brief technical flow notes in `-info` repository 
5. and a video on the strategy used to do the task. E.g you created a login 
   feature. You should explain the auth mechanism, steps, flow, syntax 
6. code and all the 3 roled persons mentioned above should acknowedge a 100% understanding of it in writing/via tool.
7. If one of the 3 team members ever need to ask a question from one of 
   the other 2, (after the task was done and some time  passed), it means the above steps were not completed correctly.
8. If one of the 3 team members are questioned by manager or asked to continue 
   the task and they are not aware on what and how something and anything 
9. at any level is happening, that is alarming as well.

## PR coordination
1. PRs will be reviewed in depth and full responsibility by pairs and STOs 
   of that team/feature/project. There might be a final review by manager 
2. or teamlead or some third person but this would be a quick review. Lets 
   say in 15 minutes of whatever work was done by all the group members 
3. (of the online group) in a day. Lets call it `Delta review`.


# Project management tool
## Task type FAQs
1. Which is the most important step or task? - Answer: Writing,covering all
   possible and correct scenarios after understanding the requirements.
1. Example of scenarios:
    1. `action_expectedResult` <--- valid scenario and test case pseudo 
    1. loginWithIncorrectCred_401ErrorSent
    1. register with existing email _ reroute to forgot password page with message
    1. any and everything thinkable, doable, actionable, reactionable by 
       user, system, naturally.
       
## Task flow and steps
1. Each task should be performed from top to bottom. I.e the tasks / ticket types mentioned 
at top should be done first. The sequence is exactly as per the list below.
1. Not more than 2 tasks should be given to new joiners at a single time.
1. This is for all but even more emphasised for new joiners is that for each 
task, (s)he should share understandings and strategy plan with pair first, 
then share brief summary of understanding and strategy/steps with STO. 
The task should be started only after all are synchronized and on the same page. 
1. Review process, when the task is done, is also with same sequence. 
Pair first, then STO
1. Consider it as a **sin, a software crime, a blunder** to declare a task as 
complete and move to a new task while the old task is actually not complete 
or with flaws or with bugs or not production ready or not ready for public 
facing or not as per requirements.

## Task / issue types
1. **Epic** - For requirements and vision. This is the super main end of 
   top most hierarchy. Its children may and usually are divided into multiple sprints
1. **Story** - For requirements and vision. We have moved to github based 
   story documentation now though. After reading the issue type, description 
   and title of the task carefully, read the parent task (story or any 
   other kind of ticket) and read all the way up to the top most ticket
   . Most of the times, major portion of requirements for your specific assigned ticket 
   would be in the parent stories.
1. Level 0 - Estimates (ballpark) - time investment 2% of total project time
   . Lets say the full project execution and completion might be guessed 
   at this stage to be 100 hours. Then at this stage of estimation, 
   we should spend about 2% (which is 2 hours).
    1. **0 understanding** - Understand requirements - Clients, product owners, 
       project managers may try their best to clarify things but it is your duty 
       to clear up requirements and make up your understandings 
       in such a way that the product owner or project manager does not says "
       Why you did this? Where is that feature? This should have been done differently 
       or this is missing". So clear up scope of responsibility before giving 
       estimates and far before performing any development.
    1. **0 pairUnderstanding** - same for pair
    1. **0 stoUnderstanding** - same for sto
    1. **0 sketch/wrf** - very quick creating sketch with digital pencil or wireframing tool
    1. **0 scenarios** - scenarios, cases e.g `z` happens if `x` is done in a `y` way.
       The `x`, `y` & `z` will be written in `-test` projects as .md file and later 
       iBK will be done via this .md file by renaming it to .ts executable test file. 
    1. **0 wbs** - work break down structure having tasks, sub tasks and 
       their estimates of next level. E.g level 1 in this case (listed bellow). 
       Here, the estimated proposed time will be added to all the 
       tickets for the next level (which is level 1 in this case as current level is 0)
    3. **0 pairReview** - review all what is done in this level here.
    4. **0 stoReview** - review all what is done in this level here and specially the execution
          strategy of assignees. STO should ask verbally on how the assignees will accomplish
          the tasks. 
5. Level 1 - Estimates - extended (enough to start execution). 20% of total time. 
   This phase should consume 10% of total project time investment.
    1. **1 deepUnderstanding** 
    1. **1 pairDeepUnderstanding**
    1. **1 stoDeepUnderstanding**
    1. **1 wireframe**
    1. **1 dbDesign** - in `.dot` language and file. Be approved via PR
    1. **1 flowDiagram** - in `.dot` language and file. Be approved via PR
    1. **1 scenarios** - No scenarios should be left here. Cover all extensively. 
       Definition and litmus test of complete scenario set: Whatever action/reaction/step is
       executable by end user/system/by natural factors is a scenario.
    3. **1 finalWbs** - Same as described above but extensive and final for the next level.
    4. **1 stoReview** - similar to `0 stoReview` but for this level. 
6. Level 2 - Base - 20% of total time.
    1. **2 html** - (html only)
    1. **2 style** - (css/scss styling and layout only)
    1. **2 req/resp model** - Just the minimalist model. Not the actual code.
    1. **2 iBK** - integration test = backend controller tests = Full tests without writing 
       code that is to be tested. E.g you don't write login functionality but you do write test code that checks `/login` route and its expected functionality. It ( the test) will of course fail as there would be not login code written. Scenarios + req/resp model will be the basis of iBK here.
    1. **2 stoFuncReview** - review all what is done in this level here.
7. Level 3 - Execute - 50% +/- of total time.
    1. **3 js** - All frontend (JS, react etc)
    1. **3 uBK** - unit tests for backend. **If this is required by manager** and we use 
       TDD, then `uBK` will be completed before or with `bk` task.
    1. **3 bk** - All backend (db, controllers, code etc)
    1. **3 e2eV** - end to end testing if needed. ui/view part only 
       (via cypress if informed by manager and applicable) 
    1. **3 e2eF** - end to end testing if needed. Functionality part only 
       (via cypress if informed by manager and applicable)
    1. **3 stoFuncReview** - final functionality review.
1. Level 4 - Post Execution - 2% of total time.
    1. **Release notes** - In -info project, make PR that describes about the business flow, 
        technical flow, any third party lib used and reason for its preference or at least what 
        approach did you took to complete the task. This will have some **information 
        that is not available in story points**. E.g any library used and why preferred
        , flow of code, technical precautions etc. This is very brief usually from 
        **25 words to 100 words max**. Few example:
        1. Had to convert .ai to .svg via 'outline conversion' ref https://somesite.com else text in svg gets distorted.
        1. Preferring XYZ lib as ABC is deprecated (or has DEF issues) or GHI security concerns.
        1. Using http v2 due to tons of advantages (list or provide link)
        1. Pending things
    1. **Video elaboration** - A video recording should be made by the assigner of task.
       (s)he should explain the flow, strategy (code, architecture, user experience etc)
       in such a way so that a totally blank/new person would understand it.
       A litmus test of it would be that suppose you are handing over the project.
       Create the video in such a way that the viewer will **never** have to ask a question
       from you. No need to explain a lot of what is already in user stories though.
8. Other types of tasks
    1. **BugBundle** - Just a wrapper ticket to hold bugs in it.
    1. **Bug[SL/BK/JS/D]** - A defect in delivery for slicing / backend / Javascript / Design.
    1. **Test[uFE/uBK/iFE/iBK/e2e]** - Tests for unit test for frontend
       , unit test for backend, integration test for frontend, integration test for backend, end to end test.		
    1. **Design** - Graphic design (Adobe photoshop, Illustrator etc)

## Task statuses

1. **new** - default status of each task when it is created
1. **in progress** - assignee should promptly set this status when (s)he 
   starts working on it. If a task was somehow marked completed at any 
   stage mentioned below and then it was rejected at any stage mentioned 
   below; if assignee starts working on it again (obviously (s)he will 
   to complete it), the during that time, the status of that task should 
   again be marked as `in progress` by the assignee.
   Do not start more than 1 or 2 tasks in parallel.
   [#smart-done](#smart-done), 
   [#getting-things-done](#getting-things-done)
5. **completed on localhost** - when something is working on your machine.
6. PR & functionality - phase 1 - We emphasis on early review rather than 
    complete all and get it reviewed after that. E.g you make an app of 10 things / steps.
    If you had made a mistake at step 2, then all steps from 2-10 might get influenced to 
    be in the wrong direction. 
    In these case, if review is done at step 10 (completion of app), then it 
    would be a "too late to find" scenario and all/ most of 2-10 steps might need a refactor.
    Whereas if the review on each step (2 in this case), only 2 will be corrected and later 
    steps will be aligned to it.
    The later is safer, more efficient, more time saving, needs lesser effort 
    as a whole, gives more certainty and many other benefits.
    1. **PR created** - when pr is created after all careful checks of 
       quality and functionality. Things maybe more or less but they should 
       be "complete" flawlessly. PR creater should attach a video of functionality so reviewer can review it. 
    3. **PR & func rejected** - if issues in code/ functionality.
    4. **PR & func approved after rejections** - If PR or functionality 
       was approved but there were repetitive or major/big issues created 
       in PR or functionality and fixed (by assignee) before approval. 
       While setting this status, setter should add a max 100 character note. 
    6. **PR & func approved flawlessly** - Reviewer should run the functionality 
       on localhost as well and take responsibility that the app is working.
7. PR & functionality - phase 2 - same as above for the same PR but second review by someone second person.
    1. **2PR & func rejected**
    1. **2PR & func approved after rejections** 
    1. **2PR & func approved flawlessly** 
8. Overall status - review by STO
    1. **Task rejected**
    1. **Task approved flawlessly**
    1. **Task approved after rejections**
9. Finalization 
    1. **closed** - Only manager should set it.
10. Other
    1. **deferred** - deferred due to some reason. This should not be set by assignee of the task.

## Task fields
1. **status** & **% done** - Current status of task. Keep changing the 
   status regularly. This is critical to avoid others asking you for updates 
   that they can simply see from the PM tool if its updated.
3. **priority** - A higher number will show higher priority.
4. **start date** - date at which task is expected to start.
5. **end date** - date at which task is expected to be fully completed.
6. **proposed est time** - After studying the requirements and making an 
   action plan and wbs, assignee or wbs creater should provide and agree to a proposed est time of accomplishment.
7. **est time** - Estimated time determined by manager/lead after or without 
   taking into `proposed est time`. This will be the final expectations.

## Time logging
1. Whatever the task assigned to assignee and performed, the time spent 
   on it should be logged via tool. In the same ticket, there is an option to log time. 
1. At the end or during the sprint, the spent time, results, proposed time
   , estimated time may be tallied to measure and improve results.
1. Each day, the total estimated time of tickets done by you should be 
   equal to the daily work time expected from you. The ticket estimated 
   time is entered by project manager and is viewable in the field "Estimated time" in each ticket.

## How to see my tasks
1. You can click "my page" button at top left corner but it will show limited 
   tasks. To see full task list of all projects, you should click "projects
   " at top and then "issues" menu. Or simply got to "/issues" url. If 
   graphical gantt view is required, you can click "gantt" menu or simply go to "/issues/gantt".
3. You can play with filters above the tasklist displayed. For example, 
   if you uncheck "assignee", you will see all tasks in all projects.
4. You can also use the shortcut links at the right side. E.g "custom queries
   " > "assigned to me" and ask manager to create more for you if needed

# Estimations and requirement gathering

## How can I improve estimate and execution
Ask few questions to your self
1. Are you spending more time on things those are not important compared 
   to critical path and more important tasks? Or even slightest postion 
   of your activity is not even needed but you do it pationately, striving hard? Think again. Analyse the day.
3. When you started working, did you proportioned total available time 
   of the day into tasks or you kept stuck on 2nd task out of 10 tasks 
   and the day passed and you found that task 3-10 for far more important than 2?
5. Think again, what other developers (who finish work on time) do, that 
   you do not. Theres always something else than simple hardwork. Maybe 
   smartwork? Planned work? More intelligent work? More skillful work? Combination of all that defeats timeline issues.
7. Do this every day. It is 100% that all need improvement. Find out things 
   that you can improve. Doing this daily and consistently is the key.

To be continued

## What is estimation
1. Estimation is the process of understanding the requirements first.
1. Then coming up with an action plan (tools, libraries, frameworks, process 
   and so on with a long list of connected things).
1. The main purposes of estimations are only two. Understanding with action plan and time to complete.
1. Time spend on estimation (which means all the above), is usually 2% 
   to 10% maximum of the total time to develop the application. 1. There 
2. is no limit on how deep someone can go in understanding, polishing a 
   diamond, optimizing something. A developer can make a login page in 
3. 1 hour and in 100 hours as well (trying to keep on beautifying and optimizing and adding features).
4. Time to estimate, with smartness, should be of balance (not too low 
   to not have unclarity and not too high to not waste time).
5. See [getting-things-done](#getting-things-done) for more information

## Sample estimation
Suppose you have to make a login page. How much time will it take? You 
answer might fall between 2 hours to 1 week. All depends on the joint mixture 
of requirements, your understandings, your skillset. Lets make a WBS and estimate
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
      
## Finalize understanding first
This is just an example, there will and must be many other questions (assuming 
that the requirements were not clear enough). We have to make them clear 
then and provide WBS based estimates. If anything is missing, explore and ask.

## Nothing is missing but I don't know estimates.
If this is the case, there can be the folowing or more reasons
1. The task is not of your level and you need to learn before implmenting
   . In this case, the "specific" thing you have to learn and the time 
   for that should also go in WBS. Once thats done, further WBS will continue (portions dependant on it).
3. You have not done enough effort to breakdown the WBS properly. If so, do it.
4. None of above but the task is a bit new to you or you have not done 
   this before OR things are of unclear or unpredictable nature. In this 
   case (which is rare), make a POC (proof of concept). e.g you are not 
   confident on an api integration. In this case, quickly make POSTMAP 
6. calls and check it. If this is the case, the "specific" thing you will 
   make POC "without which you cannot proceed", should also go in WBS. 
7. Once thats done, further WBS will continue (portions dependant on it).
      
## Correct estimation - examplary
1. 1 {hours} : Estimation and understanding requirements
      1. 0.5 {hours} : Basic understandings of task
      1. 0.5 {hours} : Talk, Research on xyz // If unclear things/ POC 
         needed. This should be done before any other execution or final estimation of xyz or related things
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

## What happens if estimates do not match outcome
Your job performance score will be affected.

## Estimation for unknown bugs
1. It is comparatively hard to estimate time for bugs. This is why the 
   first day / few hours of sprint is for understanding. Once you understand task or bug, its easy to estimate.
1. Note, it's estimation first. When execution /fixing/development start: that is the sprint start time. 
1. Still bug resolution estimate is tougher as compared to normal task 
   estimate. But the point is "try your best to estimate" and all will be ok.
1. One of the main reasons to estimate is so that we can compare between 
   "what we thought" vs "what we had to do". And improve on it later or keep good things in future.

# Meetings

### Meeting schedule
1. Scheduled meeting times:  10pm-10:15pm (scrum), 3pm, 7pm. 
    1. Please create alarms on mobile for meeting times
    1. Start speaking yourself with the sequence of people that would be 
       informed to you by your manager (sequence of your turn to speak).
1. See video(s) below (search `scrum` word) about what scrum master does.    
    
### Meeting process before meeting start
1. First of all, type 'ready' in group chat, when you are ready.
    1. Ready means that you have your work done so far open in from of 
       you to show on screen, have PR made, and updated your status in pm tool / sheet.
1. Then send your PR in group chat and past link in sheet for others to 
   review and you can review PR of others as well (whatever the methodology of your group and team is).

### During meeting
1. Per person you, should take 1 minute (unless prolonged by Manager). 
   So arrange your speech, screen, application etc accordingly beforehand.
1. Speak one by one as per given sequence by your manager / lead, about your 
    1. **status**, what you did already (most probably with **showing** your **screen**) 
    1. what are you **doing now** and 
    1. your **future plan**, 
    1. any **problems**? 
    1. or request for **separate meeting** due to problems or any other reason, 
    1. Your work **PR status** (approved, not approved, issues found etc). 
    1. Please do this in a systematic and well organized way with less 
       hand holding and asking/informing same questions/ instructions.
    1. Above said should be carried out like this. Each point has a purpose
       . E.g few things might also be written in task sheet and one might 
    2. say **"I am doing as per my sheet. That's the status and no issues
       "** but on the contrary, showing screen, verbally telling status 
    3. of each item above in few seconds allows quick review of lead/manager 
       and every team member/stakeholder listens without digging through the work sheet (in few seconds).
    4. No need to say "yes/hello" on your turn. **Simply start** the above stated. 
    5. **Listen to what others speak**. This is advantageous in team collaboration. 

### After meeting
1. STO should sync up with team members to make sure everything is on track
   . If everything is on track (ideally), then there will be less need 
2. for any detail discussion. Few verbal sentences and screen share would suffice.

### PR per meeting
1. Ideally your PR should have no or less issues and as a result, it should 
   be approved within few minutes (very quickly).
1. PR should be **`lintAutoFix`ed** and have no lint errors (at least of your code)
1. **present PRs** of whatever **stable work** you have done so far. Develop 
   in such a way that on each meeting you have something (small or big) 
2. flawless to get merged. So make PR(s) ready on each meeting time.
3. Whatever you have done, should be in an accurate and stable form in terms of functionality and code. 
4. Small reviews are good to have. It is **your responsibility** to get 
   it merged. Watch out github emails for @mentions or when issues are 
5. made. If it has no or minor mistakes, it will get merged in 2-10 minutes
   . If this is not the case, then most likely it means you did not completed it flawlessly.    
6. In SM, **review PRs of peers**. ask manager to whose work you should 
   review daily or see task field of 'reviewer' or short cut link on right panel of pm tool

### PR Deviations
1. If you are not able to get your PRs merged on each SM, it means something 
   needs to be optimized. Please discuss with your manaager. 

# Misc topics

## Asking for help by new joiners
1. Seniors should give hints, directions and practice doc links to new comers. 
New joiners should be able to setup, understand workflow and configure things themselves. 
2. If they can't carefully read and follow already written instructions in practice doc, 
seniors should not spent a lot time spoonfeeding them. Many many devs have confgured things themselves, including even inexperienced  computer science graduates. Everyone and anyone 
who is a new comer is expected to do this himself. 
3. The basic issue here is not experience. Its the apptitude + problem solving skills +
 responsibility + ownership potion that the person should drink a couple of times daily.
4. I would like to add an opinionated movie clip here https://youtu.be/Uk280jVuH1w?t=99

## Asking for help in general
You should not ask anyone in an unscheduled way. People might be working 
and concentrating on their own work. You can message (anyone) in group 
chat at each clock hour. E.g 10am, 11am, 12pm, 1pm .. so on. A clock hour 
is when its a full hour (hour needle is at the digit exactly).

Other examples maybe, if your PR is not approved in schedule meeting and 
you think any delay will affect the timeline, then you can request reviewer to review it at a clock hour.

The last resort for super urgent things where you or more people are blocked 
and also have no other alternative task is to raise red flags and ask for 
help from your pair, strategy owner, lead or manager (sequencially).


## Setup and for new commers

Links: [#development-env-setup](#development-env-setup)

Videos: [#project-tool](#project-tool), [#directory-structure-1](#directory
-structure-1), [#typescript, Daos, frontend overview](#typescript-2), [#
react-core](#react-core), [#sass-scss and themeing](#sass-scss), [#knex
](#knex), [#codding-discussions](#codding-discussions), [#i18n](#i18n), [#git-1](#git-1), 

# Development Env Setup
## Git

#### ssh keys
add ssh keys so you do not have to type password everytime and also you 
will need it for getting some of our private modules via npm. https://help
.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

Note: do not set passphrase during ssh key creation.
Also do not enter real email during key creation.

### If you install on windows
It is **important** that you choose this option `Checkout as is, commit unix style line endings`
![image](https://user-images.githubusercontent.com/6178423/120978305-0134a980-c77d-11eb-9e2d-0e2bbf5c18ca.png)

Then do `npm config set script-shell "C:\\Program Files\\git\\bin\\bash.exe"`


### superOrigin

If you are using forks, then you should add superOrigin of main repository by `git remote add superOrigin urlOfab159abRepository_thatYouUsedToForkInTheFirstPlace`

e.g: `git remote add superOrigin git@github.com:ab159ab/<project-name>.git` <-- note: you can get this by going to main project in ab159ab at github, then click "code" dropdown, copy url in `ssh` tab.

Then you should pull from there instead. e.g `git pull superOrigin master`

### Remove name, email 
For both local and on github.com settings

For local, use global email setting config git config --global user.email 
"MY_NAME@HIDDEN.com". // replace MY_NAME with your nickname.
For github.com, visit https://github.com/settings/emails and check the 
checkbox that says "Keep my email addresses private"

### Other git settings
git config --system core.longpaths true  (run as bash admin)

## Node, npm
#### nvm
Do not install node by any other means but only use nvm. Follow this link 
and use latest LTS version of node. https://github.com/nvm-sh/nvm (download 
by wget command, don't forget to copy/paste the export options in terminal 
and then install the latest **LTS** version of nodejs via https://github
.com/nvm-sh/nvm#usage  e.g `nvm i 16.15.1` <--- **important**


For windows: https://github.com/coreybutler/nvm-windows

##### node version
As of date we are using 16.15.1 for most projects. Please use this or ask 
manager. Otherwise most likely you might have challenges in setting up project.


## IDE
#### Intellij idea, vim, vscode
We encourage **vim** or intellij idea **Ultimate edition**. If you do not 
have the license, then **at least community edition**. If you do not have 
the **hardware resources**, you should get them to run intellij. If not, the last case (not preferred) is **vscode**.

Note that you should have **minimum of 4Gb ram**. Minimum **8Gb recommened
** with most **unused plugins disabled** (else you it will consume a lot of cpu and memory)


## Operating system
#### ubuntu LTS
(**ONLY LTS**) versions are allowed <--- take good care while choosing.
1. **Kubuntu** (with k) If you have 16G plus ram and a quad core and ok 
   to invest system resources on beauty and features. LTS. https://kubuntu.com
2. **Xubuntu** (with X) LTS If you don't have enough resources or just 
   want performance with ok to medium UI. https://xubuntu.org

```
sudo snap install code --classic; 
sudo apt install git chromium-browser firefox xubuntu-restricted-addons vlc redis postgresql;
```


#### Windows (NOT allowed)
~~Try using virtualbox based ubuntu server with `bridged network` option 
in network tab so you get an ip for the machine to which you can access to (via browser or IDE in wondws for coding)~~

~~If you use windows, you have to do the following in package.json (we 
have not made special windows commands yet as we mostly use and encourage 
Linux. This is the same setup we use on servers. So environment differences would be minimum)~~

~~exclude   `.`  (dot) and `/` slash at line starts~~

~~replace `/`  slashes with `\` blackslashes~~

~~replace   `;`  with `&`~~

You should try your **best** not to use windows but linux for develoment 
as it will be same with deployment/ production environment and save you from a lot of issues.

Expertise in Linux is also a key important skill in the developers life which he would face the need for any way.

## Fork projects from github
1. First of all, fork the project before following any of the steps below

You will see this on the main repository(ies) of the projects.
Main repository link will look like this: 
`https://github.com/ab159ab/<project-name>`
Project name may end with `bk`,`fe`,or `info`. These are backend, frontend
, information repositories respectively, of the same project.

![App Screenshot](https://www.cloudsavvyit.com/p/uploads/2021/11/8f84e8a9.png?trim=1,1&bg-color=000&pad=1,1)

2. The fork process will ask you that on which account you want to fork the project. Choose your account.
Once fork is made, it will be seen as in `https://github.com/<your-account>/<project-name>.
Note here that this fork will not contain `ab159ab`. The main repository and this fork repository are different.

3. Use this forked repository to clone. Do NOT clone from the main `ab159ab` repository.

```bash
  git clone git@github.com:<you-id>/<project-name>.git
```

4. Go to the project directory

```bash
  cd <project-name>
```

5. Install dependencies

```bash
  npm install
```
At this pont, you also need to install databases like postgresql and redis 
most probably for most projects (not all though). Configs of databases 
are in `bk` (backend projects). Search for `config` files and follow the 
instructions written in the database sections below. 

6. Once databases are setup, now you most probably would want to run these in the backend 
    `npm run dbMigrations` 
    `npm run dbSeeds` 
    There maybe some spelling variaions in old projects. Please see package.json for exact script names
    
7. Start the servers of both frontend and backend.

```bash
  npm start
```

## Database Redis
On Ubuntu its simple to do `sudo apt install redis-server`. **On windows
** its hard to find a clean setup. Ask you manager for download file if 
you are unable to find one in 5-10 minutes. As of November 2020, `https
://redis.io/download` does not have redis for windows available.

(for **windows** go to program files, locate redis folder, then go to bin 
folder. In windows explorer location bar, type cmd. Then type `redis-cli
`. If you get a command prompt `theip>`. If this happens, it means redis 
is running.) If not, you need to start redis within bin folder. (to be continued).

### Redis on windows
https://github.com/microsoftarchive/redis/releases/download/win-3.2.100/Redis-x64-3.2.100.msi

## Database postgres
On ubuntu and windows, use the following commands
```
sudo apt install postgresql
sudo -u postgres psql;    (for windows go to program files, locate postgres folder, then go to bin folder. 
In windows explorer location bar, type cmd. Then type `psql -U postgres`. 
You will be prompted for password that you setup during installation. Rest is same for linux and windows.
You can also use pgadmin application. Please youtube as its versions change.)
create database mydb;
\c mydb;
create user myuser with encrypted password 'mypass';
grant all privileges on database mydb to myuser; // some times for some 
hibernate apps, this is needed: GRANT ALL PRIVILEGES ON ALL TABLES IN SCHEMA public TO myuser; 
CREATE EXTENSION "uuid-ossp";

```
**Important**:
`mydb,myuser,mypass` etc should be replaced with the credentials and details 
given in your project config file. For example, your project name is `abc
-nbk`. Then your `dbname, username, password` all should be `abc`. Mostly 
this would be already coded in the config files. So see those first. See 
your config file to create matching datbase and user/pass. Configs must 
be in `src/config` or at root of project directory of `..-bk..` project.

For windows, visit https://www.postgresql.org/download/ and download pgadmin as well.
You should search youtube on how to create database, user, set password in pgadmin/postgres.

# Development process


## Tests
If your project has unit test/ integration tests/ automation tests enforced
, do not file PR without them. In most cases, integration tests are mandatory. Do not forget to ask from your manager.

Following are the default coverage if not overridden by manager.

### TDD test notes
A typical types flow:

1. insert data in database via another controller (recommended) or directly 
   in database (less recommended). Further testing will be based on this
2. . At this stage, you should fully know what input will result in what output later.
3. Make different and several cases for input and output. E.g table search, sort, group, total, etc.
4. Hit controller/ api with different params etc for things mentioned above.
5. Compare output of #3 with expected output. If development is not completed
   , tests will fail and that is fine. This will help the developer also to do development and test it seamlessly.

### Notes while writing tests

* no need to know db query or internal logic of code of developer. It's not the business of tester.
* no need to know actual/real data in db, tester can insert things himself for testing, during test.
* controller/api route should exist though. Dummy route can be made. 
* controller/api route is required to be 100% working before test is coded/
  started. However tester and developer, both should be 100% sure about input/expected output and requirements.

#### Tools to use only for tests
1. Jest
1. ~~React-testing-library~~
1. ~~Enzyme~~-- (not permitted to use for now. Use React-testing-library)
1. Cypress (not testing e2e for now but later could be used after approval to use)
1. ~~Puppeteer~~ (not permitted to use for now. Use Cypress)
1. Mocking: No need for now as knex will have read test database. For endpoint 
   and end to end testing, we are not making network calls however cypress/puppeteer will make real calls when used.

##### Backend
1. **Unit tests and integration tests**: Use Jest
      1. Controller functions should have **100% coverage**. These will 
         be unit tests (not endpoint tests making ajax calls). For example
         , you will test loginCtr.js's function loginUser('/path/login',
         req,res,next); by constructing req.query or req.body params and 
         calling these functions. No need for network call.
      4. Everything in base directory such as Base Daos or services should have **100% coverage**
      5. Everything in shared directories should have **100% coverage**
      6. Rest of the code should have at least **10% coverage** (for now
         ). Most used/referred and most important functions should be tested 
         in prioroty. Important thing to note here is that **if you test 
         any function, you should test it 100%**. If not, leave that function.
1. **Endpoint tests** (type of integration test where network call is made)
      1. Endpoint tests will be making an ajax call to '/path/login' but 
         will check status code only. **Currently not applicatble**.

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
      1. Test coverage is at least **1 test per view screen**. Screen is 
         a unique page content. E.g ignoring header, footer, nav bar (common 
         things but also included in screen and needs test), login page 
         is one screen, register is another, add user another, list user 
         is another. 
      1. This should test CRUD operation(s) of that screen 
         but **only focus on UI** and some data visibility in it. e.g in 
         a user creation page, test should fill form, hit submit, then 
         view updated data, then edit it, then delete it, then add again
         , view it (wait for element and match with expected result). There 
         is no need to redo and retest things that are already been tested 
         in controller integration testing at backend.
        
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
All functionality should be tested before making a PR (self testing). Run 
and **test the functionality yourself first**.


## Documentation

### Process flow 
Process flow should be in text form as DOT files ( https://en.wikipedia
.org/wiki/DOT_(graph_description_language) ) and part of git. One of the 
reason is that git can show diffs and changes better than changes in diagrams.

#### Process flow diagrame Sample:
```
                abc <----
                |       |
               / \      |
             yes  no ---
             |
           some thing ---> some case(note 1)
           more here
```
an other example
```
                login 
                |       
          Registered?   
               / \      
             yes  no 
             |
        credentials
        correct?
         / \      
        yes  no 
        |      |
       login  show error
```
sample dot file (can be viewed in https://edotor.net/ , for drawing connectors 
with must, use right click to start and left to stop in http://magjac.com
/graphviz-visual-editor/ , repository https://github.com/magjac/graphviz-visual-editor)

Dot syntax https://graphviz.org/documentation/

listen to conversation about layout https://youtu.be/M00Mh43NQvE

### Mini UML
```
digraph {
    node [
        style="solid" 
        shape="box"  
    ]
    subgraph cluster_auth_ctr { label= "controller/authCtr.ts"
        loginController;
    }

    subgraph cluster_auth { label= "service/login.ts"
        "login(id, pass)";
        "functionCalledByLogin()";
        "other()";
    }

    subgraph cluster_auth_dao { label= "dao/authDao.ts"
        "getUserByLoginId(id)";
    }

    loginController -> "login(id, pass)" -> "getUserByLoginId(id)";
    "login(id, pass)" -> "functionCalledByLogin()" [label = "< can be anything"]

}
```
### Process flow
```
digraph {
    node [shape="box"]
    graph [splines="splines"]
    

    login -> password_matched -> 
             route_to_dashboard;
    subgraph cluster_logs {label="loging"; logFailedAttempt}
    login -> password_not_matched -> count_failed_retry_in_memory;
             password_not_matched -> logFailedAttempt;
             password_not_matched -> login [label="Show error message and threshhold"];
}

```
### ERD
```
digraph G {
    graph [
        center=true,
        nodesep=0.5,
        ranksep="1.2 equally",
        sep=6.2,
        splines="ortho",   
        forcelabels="true",
        overlap="false",
        bgcolor="white"   
        style="dashed"
        color="gray"
        fontsize="41"
        
    ];
    node [
        width="2" 
        style="solid" 
        shape="box"  
        fontname="Arial"  
        fontsize="14"  
        fontcolor="black" 
        
    ];
    # user
    subgraph cluster0 {
        label = "user";  node [style=filled];
        user__id [label="id"];
        user__first_name[label="first_name"];
        user__last_name[label="last_name"]; 
        user__title[label="title"]; 
        user__status [label="status"];
        user__email[label="email"];
        user__phone[label="phone"];
        user__nic[label="nic"];
        user__tax_no[label="tax_no"];
        
        user__id -> 
        user__first_name ->
        user__last_name -> 
        user__title -> 
        user__status ->
        user__email ->
        user__phone ->
        user__nic ->
        user__tax_no
        [style=invis];
    }
    
    subgraph cluster1 {
        label = "user_details"; color=blue; node [style=filled];
        user_details__id -> 
        user_details__userId ->
        user_details__firstname -> 
        user_details__lastname
        [style=invis];
    }

    user_details__userId -> user__id;
}
```

## API docs
To be continued
## Code docs
To be continued

# Post development

## Pull requests / merge requests
#### PR part 1
1. Some people may say, "**what if the code is likely or will change in 
   future? is PR 1 useless?**". Well, no. If its likely to change at a 
   greater percentage, it means the plan and structure initally made needed 
   improvement. Secondly, if some of it will change anyway, the effort 
   to make initial design should have given more advantage over the minor 
   con/disadvantage (to just remove/change an empty function/file).

#### Depricated PR 1 concepts (ignore for now)
Notes: Example of child components hierarchy but with no implmentation is
```
doSomeParent(){doSomeChild1(); someOtheCode; someLibCalls;}
doSomeChild1(){doSomeChild2(); someOtherPseudoCodeMaybe;} // to make a flow for PR 2 person to understand and implement
doSomeChild2(){/* implementation in PR 2 only */}
```

#### Create a fork and branch
Create a fork from original repository into your own company account, then 
clone your project git repository locally (by default the main default 
branch will be daily-stable-master). Create a new branch from it (the main default branch). Start coding in it.


### Issues in PR
If there are any issues in PR, they should be replied/typed in reply text 
box as fixed or replied to the question or a comment. Ultimately **all 
issues should be marked as resolved by the issue creater by clicking the 
resolve button**. The developer / PR creater should not press this button but only the issue creater should.

### Close Old PR first
Always try best to close, finalize and **get old pull/merge requests first** before proceeding to new ones.
## Daily PRs routine

### One PR per day
There should be one PR per day (which is consisting of all PR part 1 + 
PR part 2). The PR should have a complete functionality including test 
code. **This is mandatory**. If you fail to get it approved, you have not 
achieved the full success of the day. It does not matter how big or small 
the code and functionality is, but it should be a **stable and complete
** functionality presented in a PR everyday at least 1 hour before day 
end time. You should file a PR before few hours of the day so it defintily 
get approved (assuming that it might have some issues and it might take 
you some time before dayend to resolve those issues and get the PR finally approved).

See [getting-things-done](#getting-things-done) for more information

### Early review

### How to solve PR issues
When an issue in PR is created, it should be fixed, code pushed, and a 
comment should be given in reply to the issue. A simplest comment can be 
'Fixed'. Then the creater of the issue should resolve the issue by hiting  
the resolve button. Not the developer. When all issues are resolved, PR can be merged.

## Pull request / merge request model B (ignore for now)
This is an alternative and discretion of manager to adapt for projects. In model B
1. Developer will create PR on github but Github will not be used for issue 
   creation. Instead, reviewer will type issues inside code with signature
2. , commit and push e.g `// {ABC}:PRI text here`. And developer will respond 
   below this line after changing code like this `// {CDE}: text here`. Commit and push. 
3. Once the code changes, conversation like this ends, the manager will 
   cut and paste this conversation at the end of file. And approve PR after 
4. changing `// {ABC}:PRI` to `// {ABC}:PRRI`. Cuting and pasting at bottom 
   like this means issue is accepted as resolved.
5. For commenting, you can use simple abbreviations like `// {ABC}: text here`
6. This will keep a record of all PR issues at end of each file.
7. Abbreviations to note here are
      1. {ABC} or {CDE} - Name abreviation. E.g John Corner is JOC. You 
         should set one signature and be consistend on it.
      1. PRI - Pull request issue
      1. PRRI - Pull request resolved issue.
8. These issues can be referenced during and after the PR by searching `}:PRI` or `}:PRRI`
9. The `/* */` can be used instead of `//` for multi line comments if needed.


# Development process
## CPP - commit, pull, push 
commit, pull, push in **same sequence**. Do this as frequently as you can
. Sequence is important. Commit first, then pull (from your branch AND 
from default branch at least), then push (to your branch). E.g For a **
team of X number of people, you should do it X times a day**. Ie in a team 
of 3 people, you should do this at least 3 times a day. 

If you are using forks, then you should add `superorigin` of main repository 
by `git remote add superorigin urlOfab159abRepository_thatYouUsedToForkInTheFirstPlace`

Then you should pull from there instead. e.g `git pull superorigin master`

## Naming conventions
This can be best informed by the following examples. If you are not following 
these, your PR may get rejected on just the naming conventions. Clear and 
self explanatory names are critical and save people from a lot of frustration.
## Git commit message
1. add backend min char check on password - login page
## Branch name
1. frontend-form-validation--login-page
## PR title
1. slicing done - login page
1. frontend form validation - login page
## Function names
1. sIsValidEmail(email)// returns true/false
## Variable names
1. userArray
1. userMap
1. users | userList //list of objects
## Directory names
1. directoryName
## Notes for names
1. Function and variable names can be a big long e.g even to 20 characters 
   but they should **smartly** and **clearly** explain the meaning and purpose. I.e be **self explanatory**.

## Mixure of names of files and functions for backend and frontend
Note that react component file will always have C capital at start but 
for other files, if it has a class, the first char will be capital. If 
it does not have a file, the first char will be small case. So file name can be pascal or camel case.
```
file, func,     desc
prefix prefix
                examples
["ct", ct,   "controller", 
                ctUser.ts//controller //or CtUser.ts if class
                ctUser()//controller  //or CtUser() if class
["Cp", Cp,   "component", 
                CpUser.tsx //comp
                CpUser()//comp
["hk", use,   "hook", // only exception for function name. Latter has 'use'
                hkUser.tsx
                useUser()
["ctx", ctx, "context",
                ctxUser.tsx
                ctxUser()
["ap", ap,     "api",
                apUser.ts/tsx
                apUser()
["do", do,     "dao",
                doUser.ts
                doUser()
["md", md,     "model",
                mdUser.ts
                mdUser()
["sr", sr,     "service"],
                srUser.ts
                srUser()
["ut", ut,     "util"],
                utUser.ts
                utUser()
["cfg", cfg, "config"],
                cfgUser.ts
                cfgUser()
["rt", rt,     "route"],
                rtUser.ts
                rtUser()
["st", st,   "style/css"],
                stUser.ts
                st-user {}
["tp", tp,     "types"],
                tpUser.ts
                tpUser = {} //types and interfaces
["dt", dt,   "data"],
                dtUser.ts
                dtUser()
["mw", mw,   "middleware"],
                mwUser.ts
                mwUser()
```

## Css variable names
1. list-item
1. list-item-container

The component should have a unique class name applied only on root element of that component, 
The class name should be named after that component name.

**Example:**
```javascript
  const CpMyTest = () => {
    return (
      <div className="cp-my-test-root"> {/* Notice the className consists of component name */}
        <CpOtherSub />
        <div className="wrapper">
          <CpMore />
          { /* so on... */ }
        </div>
      </div>
    )
}
```

Each component will have own style `.scss` file.
all the component styles should be wrapped inside a single unique parent class name.

```scss
  // As u can see, the classname .wrapper scoped now, Now if we have the 
  same classname applied anywhere else in app that won't be affected
  .cp-my-test-root { ✔️
    .wrapper { ✔️
      
    }
  }
```
```scss 
  .cp-my-test-root { ❌️
    
  }
  .wrapper { ❌
  
  }
```
## React components

### Component PropTypes naming convention:
Just name the component props type as `PropTypes`

**Example:**
```typescript
  type PropTypes = {}; ✔️

  const CpMyTest = (props: PropTypes) => { /**/ }
```

```typescript
  type MyCustomNamedType = {}; ❌

  const CpMyTest = (props: MyCustomNamedType) => { /**/ }
```

### Page Components naming convention:

Components that compose the entire UI using smaller components should be suffixed with the **Page** word.

Or just think whatever component is declared in routes file should have this name criteria.
**Example:**
```javascript
  // folder and filename: loginPage/CpLoginPage.tsx
  const CpLoginPage = () => { ✔️
    return (
      <div className="cp-login-page-root"> {/* Notice the className consists of component name */}
        <CpOther />
        <CpWrapper>
          {/* so on... */}
        </CpWrapper>
      </div>
    )
}
```

### Available Wrapper Components:
___

### Form Controls

These are the few default form control components available in the project.

You can find all the form components at this path ``src/components/form``

**Example:**
The components use **react-hook-form** for managing form state and validation.

- ```<CpFormTextFieldInput />```
- ```<CpFormCheckboxInput />```
- ```<CpFormRadioInput />```
- ```<CpFormSwitchInput />```
- ```<CpFormSelectionInput />```
- ```<CpForm />```

See Below, for examples usage of each control.

### Usage/Examples

```javascript
const CpTestComponent = () => {
  const methods = useForm({
    defaultValues: {},
  });

  return (
    <CpForm methods={methods} onSubmit={methods.handleSubmit(console.log)}>
      <CpFormTextFieldInput name="fn" label="First Name" required />
      <br />
      <CpFormCheckboxInput name="cb" label="Agree terms & conditions" required />
      <br />
      <CpFormRadioInput
        name="radio"
        label="Allow or not ?"
        required
        data={[
          { label: "Male", value: "male" },
          { label: "Female", value: "female" },
        ]}
      />
      <br />
      <CpFormSelectionInput
        name="select"
        required
        label="Select Me"
        data={[
          { label: "User 1", value: "user1" },
          { label: "User 2", value: "user2" },
          { label: "User 3", value: "user3" },
        ]}
      />
      <br />
      <CpFormSwitchInput label="Switch Me" name="switch" required />
      <br />
      <button onClick={() => methods.reset()}>Clear</button>
      <button type="submit">Submit</button>
    </CpForm>
  );
};
```

### Dialog Components

These are the variations of dialog components. 

- ```<CpDialog1 />```  => sweetAlert dialog
- ```<CpDialog2 />```  => material dialog v1
- ```<CpDialog3 />```  => material dialog v2

(✨ optional) There is a handy hook which you can use to display the dialog 
without having to set up everything manually. See example below.

````javascript
  const [dialog, close] = useDialog({ title: "Simple Dialog" });

  return (
    <button onClick={
      () => dialog({
        onConfirm: close,
        onClose: close,
        children: <p>Lorem ipsum dolor sit amet, consectetur...</p>,
        type: "info",   // if using dialog1 then you can specify type
      }, "dialog3") // you can switch between different dialogs
    }>
      Show dialog
    </button>
  )
````

### Importing modules 

- do not import anything from any UI library directly, instead import via 
  `moduleImports.ts` file (think `moduleImports.ts` as a middle man which import and export)
  ```javascript
    import { TextField } from "@mui/material"; ❌ ️
    // instead
    import { CpTextField } from "moduleImports"; ✔️
  ```
You can find the `moduleImports.ts` file in `src/shared/moduleImports/moduleImports.ts`

- icons should be imported from `iconImports.ts` file


## Comments
## Code comments
#### Commented code for later use
If unused commented code is present and developer needs it for future reference, move it to another notes file.


# Project management
## Agile
##### Why can't we just start coding. Why spend so much time in plan?
1. In short, it is to act and make an "informed decision". It is good for 
   both business and developer though a developer may want to just code 
   for practice or just due to interest or passion on something that attracts 
   him/her. That thing, strategy, solution or way to doing the task may 
   or may not even be the best way or decision for the business needs. 
   Think like a developer and also think about the business needs. Keep 
   yourself in the shoes of the product owner. If you have questions on how to think like one, ask questions.
5. At no point should a ticket be started for execution until the best 
   plan of action, strategy, requirements are clear, defined and approved
   . E.g you want to go from city A to city B. If you search a bit and 
   not just blindly hit the road in your car in garage, maybe a new bus 
   services goes there in more comfort, shorter time, on a newly made highway 
   you didn't knew about before. Or maybe a cost effective bullet train
   . Or maybe there is a curfew news you missed that can get you in jail 
   or severe. Longer or critical journeys may include feul comparisons 
   or going to a different city at all (changing course). All this cannot 
   be decided without understanding requirments and creating best course of action.

# Work and self management

## Most important things to take care
1. **No Mistakes**  <- this is a point, not comment. This is the most important 
   thing to do. You might be surpried to know but these are the most costly 
2. things in coding, a war / battle, a race, a mission, almost all kinds 
   of work. The following are most damaging kinds of mistakes.
        1. **Requirement understanding** - Do exactly whats required, not 
           less, not more. If any doubhts/suggestions, ask lead/manager.
        1. **Mistakes in code, functionality**, specially mistakes those 
           are repeated/similar in previous tasks. Every mistake (or group 
           of mistakes) causes a review cycle, an issue, a new pull/push
           , multiplied time of engagement (developer, reviewer(s)).
        **Remedy**: PR 1 with verbal but brief explaination of strategy to lead/manager before starting to code.
3. Async (non-blocking) collaboration - 
        1. Engage a peer / lead / manager only when blocked / unsure of 
           outcome or if the outcome is desired or not. If you are **not 
        2. blocked**, you should not ask before **scheduled meeting** time.
        3. If a problem conversation does not makes a **positive progress 
           towards a solution in 5-10 minutes** of a verbal meeting, 
              1. it should be either dealt by helper person via anydesk 
                 (less preferred as help seeking and helper, both will be blocked/engaged at same time) 
              1. or entirly at his own computer by taking pull from branch 
                 of help seeker developer. In this case, both developers 
              2. are not blocked by each other in same task. One can do 
                 another task meanwhile the other solves it. For learnign 
              3. purpose, the helper can then explain it breifly after its done. This is less time consuming overall.
        
## QA Quality Assurance
#### No such thing as QA
1. If you are a developer, in your world, there should be no such thing as "External dedicated QA" testing your work.
1. It is **not normal, implicit or casual to assume there there will be 
   bugs and someone will find those and report back to you**. Actually 
2. the qualities of a **good developer** is that (s)he understands requirements 
   and checks his code and functionality well enough before declaring those as complete.
3. The peer review mentioned above in git PRs is only for improvements. 
   Do not ever rely on those or expect that someone will spoon feed you 
4. about your mistakes. Mistakes are deficiencies those should be minimized rather being casual about them.

#### Test before delivery
1. Please note that you "always" have to test "EvErYtHiNg" if its working, before you declare it complete and deliver it.
1. Let me repeat again. "NEVER" declare something as complete, without testing it if it is ready for public / production use and quality.
1. Contrary can cost "HuGe" problems with time, cost, production/server discrepancies, issues, data corruption, loss of business and customers. 
1. The point is not to be a robot and 1000% "the perfect human ever" but the point is "do what should have been done by you in the first place"

## Ownership
Sprints are ownership of the team overall, success of a sprint is success 
of the full team (regardless of individual tasks). You can say you may 
hold at least 1% to 10% responsibility of overall team work. You own 100% 
of the takes specifically assigned to you. Responsibility includes, but 
not limited to, completing the task with at least minimum quality and absolutely agreed time mentioned in estimates.

## Deviations
If you encounter any deviation in attainable preplaned timeline estimates
, promptly inform the reasons and circumstances to your lead and project 
manager. Inform far ahead and as soon as possible when deviations are anticipated
. NOT at the end or when time had elapsed.

## Timelines
Once sprints and/or ticket estimats and plans are created and agreed upon
, if there are delays in timeline without a reasonalbe cause, then the 
delay is the responsibility of the developer. (S)he should cover up the 
missed deadlines by any means possible to ensure reasonable efficiency. 
This may involve working for more time or any ways of being smarter and more productive to cover deadlines.

It is the professional responsibility of the candidate, at any level, to 
provide reasonable estimates and accomplish the tasks in that reasonable 
timeframe. In cases of otherwise, in absence of justified reasons, it is 
a negative mark on the repute of the candidate.

## I got late due to problems
Someone might say "I got late because I encountered problems". Well, provided 
that you planned the project / task with due care and you are a proactive 
problem solver, the timeline should not be in deviation. 

Suppose you are going from city A to city B. Before journey, you would 
plan your journey, what to use as transport (train/bus/car), whats the 
journey time by each, time and money needed, schedule and see road blocks, make strategy before acting etc.

If a hazard comes like train out of order or delayed, or type puncture 
of a car. You should have a backup plan to resolve the situation. Get an 
alternative route/vehicle at the spot or plan it slightly before the journey 
even. E.g a taxi, or rent a bicycle, or simply try to fix the tyre (whatever is best suited and quickest).

**IF you are a proactive problem solver** (which is expected from a developer 
quite implicitly), **you will get the job done in almost same time** or 
very slight negligible deviations anyway. If you were not able to, then 
either planning needs improvement or problem solving needs improvement 
or there was a 100% natural unstoppable hazzard (e.g earth got destroyed and all died). There is NO third reason.

To explain, a soldier might say: if we had to go to a city from another 
city in a predetermined time, we will find a way; any way; and get the 
job done. There are only few corner cases in which you can't do it. E.g 
you get stuck by lightening and die on the way.  

## Change in requirements
#### I created something and it got changed. Why?
Change in any project is "normal". Change could be due to many reasons; 
for improvement or business needs or any other. Of course everytime a change 
happens, a new story is written. New design & strategy, new requirments 
and new estimates could be a normal thing to do again. Change -> new story 
-> new strategy === normal process of project

#### Ok but if it had to change, why did we do it like that in the first place?
Sometimes we don't know what the future will be. And sometimes we do know 
but despite that we do not do many things due to many reasons e.g but not 
limited to, priorities, business needs for the current time, not being 
fully sure of future features or even those will be needed in future.

## Getting things done
## Do only whats required
1. **Only do whats needed**. Nothing less, nothing more. Your time is precious
   . You should be focussed on your **specific targets and goals**. Your 
   time on job is company's **valuable asset** as your targeted efficiency 
   in it is the efficiency of the company! We want to see you valued.
3. If you see something wrong or a room for improvement, **ask permission 
   beforehand** for any deviations because if you think something is beneficial
   , that may not be the case with a different perspective, it may have 
   **side effects** or simply it may be be very **good but not needed at 
   the time** or at the cost of the current time. So simply **ask lead/manager and discuss first**.

## Improvement in steps
1. You might be thinking **then, how do we improve the code/funcitonality
   ?** Of course, you do but **in steps**. **First target is to complete 
   in a 'good way' and 'as instructed' but not in a 'perfect way'**. 
3. Perfection is a step by step process and the steps may reach infinity 
   in some cases. We will not be able to afford time loss for completion at the cost of long perfection sessions. 
4. So in short, get first stage workable. Get it approved, move to next 
   stage, get it approved and so on. Do not try to reach stage 10 by wanting 
   to learn and experiment for 9 prior stages in one go. 
6. **If your code**, on the other hand, **is below standards**, you will 
   ultimately get **PR issues anyway**... Remember them and do not repeat 
   them. So you/your code improves any way by default. 
8. But keep a fine line between personal part of pure self learning (with 
   self motive only) and self experimenting vs completing the task as priority 
   and **learning through that** (which will be done any way during the process so everyone gets happy).

## Smart done
Suppose you have 10 things in your todo list. **5 things 100% done is better than 10 things done 50% each**.
If you have multiple things, do one by one, but each fully complete.
If you have only one thing, divide it into parts. Do those parts one by one, each complete at a time.

## Definition of done
Complete in such a way that no one has to talk about it ever again until requirements change or get added.

## Definition of mistake
1. ANY thing that is done outside explicit rules of company policy and this practices doc. e.g but NOT limited to 
    2. not following **code** rules, 
    3. causing **PR issues** to be filed which are not just a difference 
       of opinion but technical / business mistake or carelessness. 
    4. missing prominent / critical issues while **reviewing a PR** (someone else's code)
1. ANY thing that shows absence of due care, ownership and responsible behaviour. e.g but NOT limited to
    1. for something you might have to say "Oh I/you forgot to do this", 
       "I/you missed this", "I/you should have done this", "this is not stable and for production / public / clients"
    2. not taking enough measures to understand **requirements** of a task
       . It is your responsibility to clear up things if not clear already.
    3. forgetting** or implementing requirements **incorrectly**
    4. **asking** the same thing **more than once** (you should take notes 
       if you fear to forget) or not following anything said by lead / manager thus (s)he had to remind more than once.
1. Proposing, researching, concluding or implementing ANY thing that is 
   least expected from one's level e.g but NOT limited to 
    1. **missing** some important aspect of documentation while research or study
    2. **making a PR issue**, suggesting something without proper knowledge and **certainity**
To be continued..

# You
## Who are our favorites? Top qualities?
Weighed according to numbers below
1. Number one quality we appreciate is not skills, appearance, experience etc. Number ONE quality is:
  - Responsible behavior : If you have this **one** trait, you will have these for example:
    1. No repetitive mistakes, 
    2. no carelessness, 
    3. not letting us repeat ever
    4. Anything informed and instructed once, would never be needed to 
       be repeated, should happen and complied in future with care. 
    5. Dedication - You should work hard with your heart and motivation. 
    6. A determination to become better. 
         If you have this one quality, you just got passed 50% acceptability already
         . Rest will follow (for us and for your career). Later comes
1. Your skills
1. Your experience
1. Your qualification


# Coding practices
## libraries choice
You should have very good reasons to choose a library. In most of the cases
, you should **ask lead before choosing a library**.

#### ES6+ over old
**Always use ES6+ syntax over old. Take it as a mandatory rule**.

## TS over JS
If your project is Typescript based, **use Typescript wherever possible**.

#### Tests
We use **Jest** as the testing library for unit tests and integration test and **Cypress** for automation e2e tests.

## Javascript
#### Never disable linting or change git, tsconfig rules
Do not disable linting without permission.

## Frontend
#### css over js
**Only** use css/scss (scss preferred) for libraries like material ui etc 
that offer both Javascript based style configurations and css based style 
configurations. Put css/scss code in separate files for each component. 
There should be no inline styles as well. This strategy is important as 
it increases page performance a bit and also decouples development. A css 
coder can work (almost) independantly from a javascript developer on the 
same projects. Spliting css and js files also improves the said. Further 
more, it also decouples style (css) and interation (javascript) logic, giving better structure to code as well.

##### External cdn or other links
Never use (until informed by manager), any kind of external links of css
, images, javascripts in html or js files like `<link src=.../>` or `<img 
src.../>`. It is agreed that resource loading via third party increases 
performance and decreases server/network load but specially in a SAAS app 
or single page app (SPA), we use our own optimized and/or bundled resources 
and/or if its PWA, this goes further strict as caching is involved. So 
do not use third party linked resources. Use `import`.

#### Images
Extending above point further, to use images or make them background etc
, use image paths in css/scss files as css/scss syntax.

## Frontend react
#### One file per component
Create one js/jsx file and one .scss file for each component. Do not worry 
about more files and directories. Worry about more number of lines in one 
file. Create a separate scss/css file for each componenet .jsx file even 
if the component is small enough or the scss/css file have fewer lines of code.

## Code Efficiency
#### consistency
Be consistent in choosing, using, following architecture, libraries, patterns
#### reusable and modular code
Do not repeat your self


## Directory structure
### Frontend react based

NOTE, naming conventions are incorrect here. Refer naming convention section
. The following is just to show you structure. This will also be updated 
soon. Refer to real/model projects that will be given to you by manager.
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
                
test

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
                        i18n
                              en.js
                              tr.js
                  someOther
                        // same directory structure as above
            user     // access after login
                  userProfile 
                        // same directory structure as in auth module above
                  userDashboard 
                        // same as above
            someOther
                  // same as above     
            shared
                  user
                        same directors like above modules controller, dao, utils, i18n
                  email
                        same
                  someOther
                        same
                        
tests
```

# Coding rules
Currently experimental but 100% enfored.

## Basic coding rules
1. If a function / code block can be logically divided into sub parts, 
   then it MUST be. e.g `login(){if(getUserByLoginId(){ checkPassword(); 
   authenticateUser();}}`  < a little invalid pseudo code but tells the purpose.
1. A function / class MUST only do ONE thing. Not more than one.
1. Any code you write MUST be close for modification and open for extension
   . In other words, you should never edit old code. It should be written 
   in such a way that editing won't be needed (even a new feature or change 
   in feature is required). When you write code, ask yourself a question 
   that will this code be needed to change/be edited if more features are 
2. required to be added OR the code you are writing can be `extended` by 
   `adding` more code to it? Edit is bad, extend is good.
3. Arrange functions/class in relevant folders and files. Do not worry 
   if your functions are too small or you have created too many tiny functions or too many files.
4. Inheritence not allowed unless you really think its needed and you get 
   a permission from project manager. For everything else, use composition instead.
5. No switch statments or if/else acting like switch statements. Use functions in objects.
6. No function parameters more than 3. If needed, make an object and pass that instead.
7. DRY. Do not repeat yourself. Take this religiously. 
8. Mostly comments mostly means deficiency in code to explain itself. But 
   few times, those are needed. Decide with care.
9. No lint errors or warnings.


## Choosing a library or framework
Ask yourself before chossing a library
1. Total time needed to understand, implement and then change or maintain 
   the library is less than the same time to create your own code?
1. Whats the downloads count, date of release, bugs, users, comunity support
   , etc of the libray / framework and other alternative options to it? 
1. Does it just does the job OR the overall benefits are less than the harms?


## Typescript
1. Use types or objects as return types and params like `PersonModel` or 
   `Type personName Pick<person, fname|lname>` or `Type personName Exclude
   <person, email`. Do not pass individual params/return types like `name, email`




-------------------------------------------------------


# Configuring development environment
## CORS restrictions
If you get CORS errors, you can install browser plugin (one called `allow 
cors` for chrome). You have to hit the big icon and make it colored to activate it.

## Localhost nginx config 

Note: 
1. Replace `projectName` with real project name
1. You can use different ports for each project. e.g 4321 (backend) + 5321 
   (frontend) for one project and 2321,3321 for another. 6321,7321 for another, 8321,9321 for another.
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

## Node.js Knex transactions
Any database access objects DAOs should not be declared or called without trx.
Sudo code:
```
try
  await knex.transaction(async (trx) => {
     other code
     const v = await someDao(trx, param, param)
     other code2
     const v2 = await someOtherDao(trx, param, param)
  });
catch
```
Related code and DAOs can be grouped in knex.transaction block. If code 
is not related, you can have multiple separate knex.transaction blocks isolated.

# Online remote groups
## Noise due to group talk
If you feel theres **too much voice conversations** in remote group, you 
can **mute the volume** but you should **be alert for any chat messages
**. If some one wants to talk to you, (s)he should ping you on chat. You should do the same.

## Stay connected all the time
You should stay connected to group collaboration software all the time

## Personal info
1. Sharing of any personal information or discussing anything not related 
   to work/current tasks is treated as a miss conduct.
1. Using any personal email, phone or contact in any platform, such as 
   but limited to, github, collaboration, chat etc tools is treated as a miss conduct.

# Daily routine

## What to do at day start
Do the following in exact sequence

#### Log in start time
in attendance app if provided to you

#### Message manager
about your presence and check your emails/messanger/app for any messages that may need your attention.

#### Keep communication app onn
Whatever is your persistant communication medium, make sure it is always 
connected and available during sign in and sign off time (currently zoom
, whatsapp, discoard (all three should be connected))

#### Refresh / review task list
assigned to you and observe any changes (specially priority and dates) 
and act accoringly. Do this in the first few minutes of the day. This should 
be the first actual activity you should do.

#### Plan or ask questions
If anything is unclear for the day ahead, ask questions from manager. If all is clear, plan what to do next.

#### Put proposed estimated hours 
in your task fields and observe estimated hours and due dates if manager has already filled those.

#### Start your tasks
according to the priority number in tickets and change ticket status from 
`new` to `in-progress` with some percentage (wherever applicable).

#### Update status of tasks
during the day at lease 2-3 times so the stakeholders do not have to ask you individually.

## What to do at day end
Do the followings in exact sequence

#### Work and tickets complete
Make sure the work assigned to you for the day is complete. Take good care 
to make sure that the git PR, PM tool ticket fields and all required things are complete and accurate.

#### Make PRs
And push code. This should be done daily and stable code should be daily 
pushed. If you have not completed something, push the stable part. By the 
way, the ratio of your work should have more than 90% stable part. You 
should not assume or say that you didn't pushed because things were not 
stable. In a full day, you should work considerable stable part. Its better 
to do 5 things 100% complete rather than 10 things 50% complete.

#### Update ticket statuses

#### Plan or ask questions
If anything is unclear for the next day, ask questions from manager. If all is clear, plan what to do next.

#### Message manager
at least 15 minutes before signing off so (s)he can discuss things or collaborate with you if needed.

#### Log sign out time
in attendance app if provided to you

# Attendance
## Late sign-in
You should not come late in any and all cases unless you have explicit 
permission to come late from your manager or HR for that day. Few resources 
might want to or had worked late in the last working day. This does not 
except them from coming on time on the next day.

## Early signout
Early signout is not allowed. If you do, you should spend that time in 
the next day in addition to the days time. If you think you have completed 
your tasks before dayend time, **a)** thinkg again and make sure they are 
fully completed **b)** if they are completed, ask for next tasks if project 
manager is available. If project manager is not available, start reading 
and understanding the next stories and tasks for future. 

## Normal routine
Just follow the normal routine. We do not encourage late sittings. If you 
do late sittings on your own (without explicit instructions from manager
), then the late sitting is on you (your choice) and this cannot be compensated 
/ swapped with normal working hours. For example, you signed out 10 minutes 
late on 1st Jan. You cannot come late by 10 minutes on 2nd Jan or 5th Jan
. If you have concerns, then simply do not sit late. But normal routine 
should be same. However in few cases, the manager or adminstration may 
provide you benefits. As a side note, it is mostly observed that new commers 
often try to learn and try to accomplish their tasks with help of extra 
late sittings (at their own choice) or normal developers to complete their 'due' tasks.

# Penalties and rewards
Bright career of developer and quality and efficient work at company side 
demands discipline. Time of developer is precious and time of reviewers 
and managers is costly and cannot be used to keep on entertaining, informing
, correcting and explaining same or similar things repeatedly. This is 
simply not viable nor affordable. Thus following penalties apply and will be modified from time to time.

However, rather being appreciative also on diciplined and well mannered
, responsible employees, we also announce rewards!

Model type assigned (single or multiple) to you will be informed to you by your manager.

# Frequent mistakes we observed
## Code reviews
#### General
1. Use of any library or framework without written approval in non-PR-1 
   PRs or which is not in the approved list mentioned here. Managers should 
2. also create and publish a list off approved libs, framework for PR-2/3.
3. Use of any (unapproved in writing) library or framework or tool that 
   creates/writes code for you. For example, but not limited to, create-react-app from create-react-app.dev website
4. Repeating a mistake (small or large) that was previously corrected by 
   a lead/manager/reviewer (penalty is half of default penalty in this case)
5. Not being able to create a stable PR at least one and half hour before end of signoff time.
6. Not reviewing a PR (of someone else) within 2 hours of being informed.
7. Providing a PR title that is not the ticket name nor self explanatory.

#### General coding
1. Giving unclear variable/ function/ class names. E.g `maxSize` does not 
   tells what it is and unit of measure. Instead it can be `maxUploadFileSizeInMB
2. ` or `upload.maxFileSizeInMB`. In short, when a person sees the name, he should exactly know what it is.
3. Not following the file, variable, function or class naming conventions 
   stated in this doc e.g but not limited to having controller abreviation in controller files and functions.
4. Not following directory structure stated in this doc. E.g but not limited to controller, dao, service directories
5. Using console logs without a logger library or logger function.
6. Using strings or numbers that cannot be referred from configs, constants 
   or cannot be auto completed while coding via Intellij Idea IDE. (exceptions 
7. of course are config files, constants, typescript types etc that actually 
   provide the feature to be referred by other consumers)
8. Keeping unused code in middle of file. Put them at bottom of file.

#### Configs
1. Not using database name, user name, password same as project name (without 
   hyphens). e.g `some-name-bk` can be `somename`
1. Using ports other than x321 port numbers where x can be from 1-9
1. Commiting your own configs that work for you but no need for other developers
   . E.g putting your own different database name or username and committing, pushing it.
1. Changing configs like eslint, babel, package.json scripts etc: Change 
   of configs should not be done directly but via change in tpl projects 
2. or modules (whatever had been made and used for the project).

#### Linux compatibility
1. Creating PR that is missing code for or is incompatible or is not tested on ubuntu LTS operating system.
1. Not testing with nginx/apache with hosts file based local domain.

#### Personal info
1. Putting real names of anyone (instead of `user, user1, user2` in any 
   part of code, image or any kind of asset/document or communication medium in any form.
1. Putting any kind of personal info that is not official. For example, 
   but not limited to, personal email or phone in any part of code, image 
2. or any kind of asset/document or communication medium in any form.

#### All languages
1. Creating PR with console errors in browser, network tab errors in browser
   , application tab in browser or commandline erros of any kind. Or PWA service, application, cache errors.
1. Creating PR without minimum test coverage in each category (stated in 
   this document). Test coverage should be provided by manager in project readme file or via email.
1. Creating a PR where app does not starts or tests do not run or run with errors.  
1. Not taking pull from master and daily-stable-master branch before making PR

#### Javascript, Typescript
1. Creating PR with lint errors, TSC errors, terminal/console errors, browser 
   console errors. Lint and TSC errors are not just errors shown in IDE 
2. but also via command line and scripts for example, but not limited to
   , eslint commandline, TSC commandline, browser console errors (even 
3. if your project uses webpack or some other automation tool / script to compile).
4. Creating PR with compile or transpile errors e.g but not limited to, 
   by babel, typescript compile (tsc), webpack, etc.
5. Changing, suppressing or disabling any project base configurations like 
   eslint rules, tsconfig, esconfig, babel, package.json scripts
6. Using raw string based knex queries where proper knex syntax is possible. (one fourth of default panelty per query)

#### Typescript
1. Use of `any` or `unknown` without written approval
1. In typescript, using any non-javacript feature other than providing types (temporary rule for now).

#### Frontend / react
1. Coding inline (s)css styles or any kind of view code in any way inline. It should go in separate file.
1. Coding (s)css styles or any kind of view code in any way in react component 
   file or file having html code. It should go in separate file. Even if 
2. the style is not a pure (s)css syntax but some object like of material 
   ui parameter etc, anything to do with styles goes in a separate file 
3. with style name in file name or a .scss. If former, style object can 
   be imported in the view component file and used.
4. If more than one components are using a child component and passing 
   the same props every time (or it is anticipated in near future), then 
5. that called function (or wrapper of it if its a third party lib), should 
   have default prop values that can be overriden when and if needed)

#### React
1. Referencing any third party css, javascipt resource other than including 
   it in bundle.js as code. You should use `import` lib from `package` (Valid rule if bundling is used)

#### Java
1. Not using maven or gradle for dependancies but adding lib files directly
1. Not testing with .jar before PR

### Python
To be added soon

## Routine

#### Attendance
Avoid
1. Not informing timely (at least 24hours) in writing before a non-emergency leave.
1. Not following "Daily routine" section on what to do at day start and day end. 
1. Not taking mandatory break from work for at least 30 minutes in the 
   middle of day (and 1 hour in total during all day (prayer, lunch, rest etc).

#### Behavior
Avoid
1. Not following anything mentioned in appointment, policy, practices or any ammendmends in the said things. 
1. Asking for information that is already clearly present in appointment
   , policy or practices documents. This means employee had not carefully 
2. read the said and is irresponsibly consuming managemnt's time. However
   , if something is really missing, we welcome questions.

# List of libs/framework approved for PR 2/3
## Third party libs/frameworks

```
    All exact version number of libs mentioned in tpl project package.json
    any @types for typescript
```
## Inhouse made libs
All modules shoulds be found and listed with details by developers here: https://github.com/ab159ab/module-info

# Tutorials

## Workflow, PR 1 pseudo etc

1. Workflow https://www.youtube.com/watch?v=AY_ox3Zp9Y8
1. Code PR 1, 2 (Pull request) with peer https://youtu.be/BJuwXc10bow
1. Pseudo api tests https://youtu.be/4ki3WWWbVUg
1. Test dependency on other tests and data  https://youtu.be/fMw4jKLUdGk
1. Req response model https://youtu.be/B7WlwGw4_Bc
1. Segregation of tasks PR 1 and PR 2 https://youtu.be/7tOMTbo0NF8
1. What does scrum master do? https://www.youtube.com/watch?v=1CxWF42WQFo  https://www.youtube.com/watch?v=QbPkcfzi2HI

## Initial Strategy making
1. Internal make sure strategy is followed correctly by others and pr 1 https://youtu.be/EhgLR4alv1I
2. What is strategy making https://youtu.be/FLLW9Dl_pDE
3. Sample strategy making  (can be extended where needed but this is a 
   must have in all cases) https://youtu.be/_cLq9KfIHWY
4. Sample strategy sagp social urls https://youtu.be/2OSSVKB6ZDM
5. Strategy making optimization https://youtu.be/aCaWohyRhxM

## Codding discussions
5. Open / close and if / else / switch statements https://www.youtube.com/watch?v=-ptMtJAdj40

## Self review
1. How to self review https://youtu.be/nxhpVWcvHjI
1. Self review attitude 2021 08 24  https://youtu.be/wAsnZs-MSOU
1. Bug vs improvement self qa flawless delivery 2021 08 19 https://youtu.be/L7_k6vRkMIg
1. Bugs vs preference https://youtu.be/rP7cDLhMPzA

## Personality
1. Responsible behaviour https://youtu.be/W2hWQFA7tgA
1. Resourcefullnes problem solver https://youtu.be/nKRXiuug59k
1. Resourcefullnes problem solver part 2 https://youtu.be/f_MgVusUJdQ 
1. Inner and outer world https://youtu.be/3RtPd_wWAfk
1. Mistakes, carelessness https://youtu.be/nMVhlYyrJ-E
1. Pull request review delegation https://youtu.be/4ekRhisqzhQ 

## Asking for help
1. How to get help from others https://youtu.be/lfCE_jf0RaY

## Javascript Misc

### Javascript core 
official first priority tutorials
1. https://developer.mozilla.org/en-US/docs/Web/JavaScript
1. https://tc39.es/ecma262/ || https://ecma-international.org/ecma-262/
   10.0/index.html || https://github.com/tc39/ecma262
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
1. ~~Api testing https://youtu.be/7VNgjfmv_fE?t=381  to 5 mins (the later 
   code for mongo is irrelevant). The same logic can be applied for Jest~~ Disregard this.

#### Enzyme 
1. Basic info and examples https://enzymejs.github.io/enzyme/
1. Setup https://enzymejs.github.io/enzyme/docs/guides/jest.html

### Mock testing
1. Mock libs and data https://www.youtube.com/watch?v=4Fl5GH4eYZ8&t=909s, https://youtu.be/Ngj2f1n9pUw?t=459

## i18n

1. i18n basics https://youtu.be/LrVxEM_7GzE
1. i18n example https://youtu.be/FLJBguJRxFA
2. i18n details https://youtu.be/O0ZzMII3hV8

## Frontent

### Mix
1. How to bypass frontend form validation https://youtu.be/lXttrBti82E
1. Forgot password strategy https://youtu.be/GeqkAcshjoA

### Coding practices
1. React code reusability https://youtu.be/VgRyPndPNlI

### Typescript
1. Typescript models and DAOs https://youtu.be/AXyJHMksgXM
2. frontend and typescript overview https://youtu.be/oIYYWdYcnb8 
1. Tutorials 1 Traversy Media https://www.youtube.com/watch?v=BCg4U1FzODs&t=1011s
1. Tutorials 2 Academind https://www.youtube.com/watch?v=BwuLxPH8IDs

### React core
1. React in 5 minutes https://www.youtube.com/watch?v=MRIMT0xPXFI
1. React in 30 mins with a todo list app https://youtu.be/hQAHSlTtcmY?t=171
1. react components https://www.youtube.com/watch?v=Y2hgEGPzTZY&list=PLC3y8-rFHvwgg3vaYJgHGnModB54rxOk3&index=4
1. react props https://www.youtube.com/watch?v=m7OWXtbiXX8&list=PLC3y8-rFHvwgg3vaYJgHGnModB54rxOk3&index=9
1. react state https://www.youtube.com/watch?v=4ORZ1GmjaMc&list=PLC3y8-rFHvwgg3vaYJgHGnModB54rxOk3&index=10    
1. routing https://www.youtube.com/watch?v=yQf1KbGiwiI
1. component usage, data binding, retrive and display data in table/UI/form from object
    1. conditional rendering https://www.youtube.com/watch?v=7o5FPaVA9m0
    1. list rendering https://www.youtube.com/watch?v=5s8Ol9uw-yM
    1. array rendering with unique id https://www.youtube.com/watch?v=ke1pkMV44iU
    1. form handling https://www.youtube.com/watch?v=7Vo_VCcWupQ&list=PLC3y8-rFHvwgg3vaYJgHGnModB54rxOk3&index=21
    1. useState https://www.youtube.com/watch?v=O6P86uwfdR0
1. Ajax calls, custom hooks https://www.youtube.com/watch?v=lvQgZqvIY6M&feature=youtu.be
1. Lynda React essential training 

### Angular
1. Angular 8 urdu https://www.youtube.com/watch?v=wGPZJDw3Ee4&ab_channel=LearnInUrdu
1. Angular https://www.youtube.com/watch?v=k5E2AVpwsko&t=5606s

### Sass scss css
1. Sass tutorials - inheritence and more https://www.youtube.com/watch?v=nu5mdN2JIwM&t=406s 
1. Sass tutorials - variables and more https://www.youtube.com/watch?v=nu5mdN2JIwM&t=191s
1. Sass tutorials - sass in 20 mins 2019 https://www.youtube.com/watch?v=Zz6eOVaaelI  
2. Css grid layout - https://youtu.be/jV8B24rSN5o?t=230 
3. Kendo sass scss styling theming https://youtu.be/yUjkD7hHi3Y

### Knex 
1. updating    https://www.youtube.com/watch?v=aWLlh_Gn_oA
1. select https://www.youtube.com/watch?v=GbVP4Ac2QAo
1. migrations https://www.youtube.com/watch?v=YEh7yPr8oGE

### SQL
1. DB schema decision with entity involvment https://www.youtube.com/watch?v=P4AUdfHS9Bc

### Java
1. Is java difficult? Few things in this video might be incorrect but just 
   listen to it https://www.youtube.com/watch?v=mCOSgYilwNs
### Spring
1. spring intro in 10 mns https://www.youtube.com/watch?v=gq4S-ovWVlM
1. spring boot https://www.youtube.com/watch?v=msXL2oDexqw&list=PLqq-6Pq4lTTbx8p2oCgcAQGQyqN8XeA1x
1. spring https://www.youtube.com/watch?v=GB8k2-Egfv0&list=PLC97BDEFDCDD169D7

### Hibernate
1. hibernate https://www.youtube.com/watch?v=Yv2xctJxE-w&list=PL4AFF701184976B25

### Maven
maven https://www.youtube.com/watch?v=al7bRZzz4oU&list=PL92E89440B7BFD0F6

### Java Mix
1. For detailed javaee related concepts (caustion, few are a bit old so 
   you should make sure if anything is depricated), https://innovalog.atlassian
2. .net/wiki/spaces/JMCF/pages/141892372/Calculated+scripted+Text+Html+custom+field+type
3. spring boot, jpa, hibernate in 1 hour https://www.youtube.com/watch?v=MaI0_XdpdP8

## Diagraming and tools
### Dot graphviz
1. How to create process flow diagrames https://youtu.be/KPblF9LfTp0

## Git / github

### Git
1. Pull request/ Merge request: https://youtu.be/uPt-bP_bKmQ
1. Forking at github https://www.youtube.com/watch?v=nT8KGYVurIU
1. SuperOrigin and forks https://youtu.be/sys5PMunerc
1. Pull, push, commit with Forks https://youtu.be/J5xli-BmDzM
1. Github git branch repo pull request code exchange explained https://youtu.be/ZW5gLj687qw
1. Git multi branch made simple https://youtu.be/zVfK-Rxt1Iw 
1. Multi branch, multi pr, multi functionality https://youtu.be/t-fNSEgqe4I
1. Git rebase https://www.youtube.com/watch?v=kMvLn8WcAII
1. Git rebase https://www.youtube.com/watch?v=CRlGDDprdOQ
1. Git rebase https://www.youtube.com/watch?v=f1wnYdLEpgI
1. Lynda Git Essential Training: The Basics with Kevin Skoglund

### Github
1. Lynda Github Essential Training

## Project tool
### Info gathering
1. Project tool - Info gathering https://youtu.be/vt4ymkGjco8
1. Project tool - why divide story into different tasks https://youtu.be/9e_hn905-tw
1. Project tool - gantt and stories https://youtu.be/wiq8lbz2RhE
1. Project tool - task life cycle https://youtu.be/-0EH_lFeYBk
1. create multiple tasks part 1 https://youtu.be/fPq67N1Pjaw 
1. create multiple tasks part 2 https://youtu.be/JSe7VW0I6AU  

### Activity sheet 
1. How to update status on sheet https://youtu.be/mLMNsMp5Wx8

## Basic way of working
### Directory structure
1. Node, react https://youtu.be/grnmgw9vqDk
2. Basic ajax controller database flow https://youtu.be/ik-D4-ngJPw

## Basics

### Algorithms
1. Big O notation https://www.youtube.com/watch?v=IR_S8BC8KI0
1. Live testing https://edotor.net/
1. (do not use) ERD exampmles https://mamchenkov.net/wordpress/2015/08/20/graphviz-dot-erds-network-diagrams/
1. (do not use) ERD example https://stackoverflow.com/questions/56832652
   /erd-diagram-with-graphviz-how-to-improve-the-rendering-layout

### Dot files and graphviz
1. Dot files https://www.youtube.com/watch?v=QjUaNXNuNMs
1. Dot file Docs https://www.graphviz.org/pdf/dotguide.pdf
1. Some examples https://renenyffenegger.ch/notes/tools/Graphviz/examples
   /index https://www.graphviz.org/Gallery/directed/cluster.html

### Architecture for newbies
1. Basic app architecture and learning - https://youtu.be/OmZhSqgo6TQ
1. node backend newbie 1 - https://youtu.be/T7oYz2rICsc
1. react intro newbie 1 - https://youtu.be/CWNX5U_spmE

## Vanila javascript possibilities
1. Vanila javascript based component https://www.youtube.com/watch?v=vLkPBj9ZaU0

## SSR server side rendering
1. Getspeed https://youtu.be/Kg0Q_YaQ3Gk?t=421

## Wordpress

1. Custom wordpress theme https://youtu.be/ZJKAwJq9_xM?t=416
2. Custom wordpress theme https://www.youtube.com/watch?v=-h7gOJbIpmo
3. Custom wordpress theme https://www.youtube.com/watch?v=pFMgAWkrk8o

## Vim

## Pros of vim
1. Vim as a competitive advantage https://www.youtube.com/watch?v=4WTV6ZCY4qo
1. How vim saves time https://www.youtube.com/watch?v=bshMXXX40_4

## Vim core
1. Do most without vim plugins https://www.youtube.com/watch?v=XA2WjJbmmoM&t=3846s

## Who uses Vim

1. Microsoft manager, auther of typescript language server https://www.youtube.com/watch?v=lbkjXWeWY-o

## Misc
1. Presentation in vim https://www.youtube.com/watch?v=GDa7hrbcCB8


# Queue
### How to delete branches and start fresh fetch

backup (manual copy paste your project; in case you loose code)
```
git branch -d <yourBranchName>
git push -d <yourForkOrigin <yourBranchName>

git fetch superOrigin -a
git checkout -b <yourBranch> superOrigin/<branchNameAtSuperOrigin>

git log  < check all commits tally with github page of superOrigin branch)
```

### Maven and spring commands

```
sudo apt install default-jdk
sudo apt install maven
```
In project directory:
```
mvn -U clean install
mvn dependency:purge-local-repository
mvn spring-boot:run
```

### Remote collaboration
1. Let the world, your friends, neighbours and your family know that you are *on duty* while  in office timings.
2. Let all know that this is your career and this career will be with you for life time.
3. Let them know that this is remote work but not less professional and 
   formal than any on-premises office work or duty.
4. Create 'do not disturb' or 'silence please' signs all over the walls 
   at your work area, lock the room, repartition the room, do whatever it takes to have a healthy working environment.
5. You are not expected to be absent/ unreacheable for more than 5 minutes
   , without informing your manager and then informing again on your return
   . Its ok to just inform and leave for a 5 minute walk, posture change
6. , water, tea, washroom break etc 1-2 times a day.
7. Keep zoom/ discord/ any chat platform used to be connected and respond to 'unmute requests'.
8. Hardware / internet issues and other issues. Internet issues, computer 
   issues, etc. These are not even meant to be discussed here as you all are adults. 
    1. If primary pc or internet makes problems, install zoom and discord 
       on mobile as backup (always) and have a cheap data package for mobile 
       sim card (always). Make a hotspot. In short, do whats needed as its your responsibility. 
    2. If you have a mic / speaker issue, connect with your mobile phone 
       based zoom / discord and share screen in desktop with another user (instance of ) zoom / discord.
9. Failure to not make measures or repeated absence may result in cards 
   being issued. https://github.com/thesircle/cq-policy#disciplinary-procedure


### Effective delegation
1. If you ever have to repeat yourself exactly or mostly same on the same 
   topic, it means delegation is not efficient. If you think similar 
2. tbc

### NPM package issues
If any issues in packages, do this:
```
delete node_modules
make sure you have node LTS version (latest). Using nvm for this is easier
(optional but recommended). See how to use nvm at link in this doc.
do:
npm cache clean --force
npm cache verify
npm i
```

### Mysql backup/restore
```
mysqldump -u<userName> -p<Password> -h<Host> <dbName>   >  <path/to/file.sql>     //backup

mysql -u<userName> -p<Password> -h<Host> <dbName>   <  <path/to/file.sql>            //restore

```
### Mysql misc
1. display tables in cmd  `pager less -SFX;`
2. `show databases; use xyzDatabaseName; show tables;`
3. `create database <name>;`
4. Create user: `CREATE USER 'nativeuser'@'localhost'IDENTIFIED WITH mysql_native_password BY 'password';`
5. If you already have created user with some other way and facing issues 
   with connecting via an application, you can do:  `ALTER USER 'user'@'
   localhost' IDENTIFIED WITH mysql_native_password BY 'your_new_password
6. ';  FLUSH PRIVILEGES;` `GRANT ALL PRIVILEGES ON database.* TO 'user'@'host'`
7. see relations FKs in workbench https://youtu.be/E0krzfu2jxc?t=60
queue

```
sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf

```


### Postgres backup/restore

```
pg_dump -U <user>  -h <host> -p <port-LeaveThisIfDefaultPort>  <dbName> -Fc > <fileName>   // dump

pg_restore -U <user> -d <dbname> -Fc --no-privileges --no-owner < <filenameToRestore>  // restore
```

### Postgres connect
```
psql -U devuser -d devdb -h localhost
```
### Postgres misc

uuid generator. Use v4. https://www.uuidgenerator.net

### HTML connector and charts

1. https://anseki.github.io/leader-line/
2. https://anseki.github.io/plain-draggable/
3. https://gojs.net/beta/samples/pageFlow.html
4. https://js.cytoscape.org/demos/architecture/
5. http://bl.ocks.org/Neilos/584b9a5d44d5fe00f779
6. https://bost.ocks.org/mike/fisheye/
7. https://bost.ocks.org/mike/hive/
8. https://observablehq.com/@d3/hierarchical-edge-bundling
9. https://observablehq.com/@d3/tidy-tree
10. https://dmitrybaranovskiy.github.io/raphael/graffle.html

### Git
1. `git push origin local-name:remote-name`


### Translation

1. PDF https://www.onlinedoctranslator.com/en/translationform
1. PDF https://www.protranslate.net/en/order/

### Helper utilities for collaboration

1. Google meet mute tab https://chrome.google.com/webstore/detail/mute-
   tab/blljobffcekcbopmkgfhpcjmbfnelkfg  Use this plugin to mute multiple 
2. meeting rooms/tabs and unmute only the one you want to listen to.
3. Show notifications for google meet and also can download chats as text 
   file https://chrome.google.com/webstore/detail/notifs-for-meet/iinecemgdedknjoenecmgjlghnkmbofc

### Helper configs 
1. Node file watcher for linux 
```
# insert the new value into the system config
echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p

# check that the new value was applied
cat /proc/sys/fs/inotify/max_user_watches

# config variable name (not runnable)
fs.inotify.max_user_watches=524288
```

## Few preferences

### choosing tools for docs, development and management
In the PM tool app, drawing app, we use should
* be configurable, changeable e.g PM tool database in our own hands, git 
  based docs in our control, spreadsheet in our full control if downloaded, its spreadsheet.
* can gave local backup
* the backup should be run independent of the application service (paid or free) online
* mostly text based, text oriented 

These are few of the core values.

* Beauty is not in the primary core values
* Easy to use is ok but we do not use things just because its easy to get started
* or its sparky and shiny
