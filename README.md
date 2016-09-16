# Blueprint

aka **How We Collaborate** :zap:

##Contents

[Overview](#overview)  
[Why Process?](#why-process)  
[Team](#team)  
[Workflow](#workflow)  
[Sprints](#sprints)  
[Velocity Tracking](#velocity-tracking)  
[Exchange Program](#exchange-program)  
[Notes](#notes)  
[Contributors](#contributors)  

##Overview

This document is an overview of the [Vimeo Mobile and TV Group's](#notes)<sup>1</sup> product development process (a process based on [scrum](https://en.wikipedia.org/wiki/Scrum_(software_development)) and [agile](https://en.wikipedia.org/wiki/Agile_software_development) methodologies). It describes [why process](#why-process) is important and outlines five aspects of our process: [team](#team), [workflow](#workflow), [sprints](#sprints), [velocity tracking](#velocity-tracking) and the [exchange program](#exchange-program). This document focuses on high-level guidelines rather than specific implementation tactics in order to leave room for teams to apply them as they see fit. 

##Why Process?

Process helps us to:
 
1. Produce high quality work at a predictable [pace](#notes)<sup>2</sup>, 
2. Promote the development of an extraordinary team.
 
##Team
 
A product team is a co-located, cross-functional group of roughly 4-7 people who collaborate to bring ideas to life. Proximity builds relationships. Cross-functionality fosters autonomy and self-sufficiency. Limiting team size promotes ownership.
 
![Team composition](/assets/team-composition.png)    
<sup>*Team composition*</sup>

Teams are externally trusted, transparent, and accountable. Teams are internally creative, balanced, and practical. 

##Workflow
 
Workflow is a structured approach to how a team evolves an idea from inception to production. Teams evolve each idea one function at a time, with each function’s output being the next function’s input. 

![Workflow and deliverables](/assets/workflow.png)    
<sup>*Workflow and deliverables*</sup>

Consider an example where the idea we're working on is captured by this user story: *"As a user, I'd like to be able to upload videos to Vimeo from within the Vimeo iOS app."* The team's product manager creates a feature spec. The team's designer uses this spec to generate visuals. The team's developer uses the product and design documentation to build the upload feature. And the team's QA representative tests the resulting build and documents any bugs that surface. Based on QA's test results we determine whether the build is shippable. 

Each function's output must be reviewed and approved by the other functions before it can advance to the next stage (e.g. design and engineering review a product spec before it advances, product and engineering review design documentation before it advances, etc.). This helps us make decisions when we have enough info to make them (not before, not after). It also ensures cross-functional ownership at each stage.

This is our ideal workflow. In practice the boundaries are softer and the communication more fluid. No matter how the workflow is applied the emphasis is on discussion across functions and platforms early and often (e.g. product specs out a feature, design identifies potential conceptual inconsistencies, engineering identifies technical limitations, revisions are made, and so on). 

These checks and balances help us define problems more accurately. This makes us less likely to encounter issues mid-development, and therefore increases our chances of success and predictability. However, problems are not always avoidable and this is where a willingness to engage in iterative product development is important.

We solicit feedback early, ask questions often, and [document and share what we learn](#notes)<sup>3</sup> along the way. 

##Sprints
 
Sprints are structured 2-week intervals at which a team executes the above workflow to evolve ideas. Sprints help teams establish [pace](#notes)<sup>2</sup>. Pace is valuable because it allows us to predict how long projects will take in the short and long term. 
 
![Sprint workflow](/assets/workflow-with-sprints.png)    
<sup>*Sprint workflow*</sup>

Before beginning a sprint:
 
1. We assemble a rough list of stories to be included in the sprint (a mix of product, design, dev, and qa stories),
2. We determine who will work on each story (via self-selection rather than top-down assignment), 
3. Assignees break each of their stories into small, actionable chunks (defined in, for example, Jira tickets or Github issues),
4. We estimate the amount of effort required to complete each chunk (via [planning poker](https://en.wikipedia.org/wiki/Planning_poker)), and
5. We commit to a specific subset of chunks by using our historical team [velocity](https://en.wikipedia.org/wiki/Velocity_(software_development)) and the [Pace apps](#notes)<sup>2</sup> to calculate how much each person should take on.

![Sprint planning](/assets/sprint-planning.png)    
<sup>*Sprint planning*</sup>

During a sprint we track progress using a [scrum or kanban-like board](#notes)<sup>4</sup> with status columns for To Do, In Progress, Blocked, Ready for Review, Ready for QA, and Done. 

After finishing a sprint we hold a retrospective to discuss what went well, what didn't go so well, and what we decide to do differently next sprint. Part of retrospective involves examining our [burndown chart](https://en.wikipedia.org/wiki/Burn_down_chart) to gauge the accuracy of our estimates and inform how we estimate and commit to the next sprint's tasks. Retrospective is also the perfect time to adjust the process to better suit our needs.

The following sections provide more detail on specific phases of sprint planning mentioned above. 

##Task Estimation 

Each task that a team member takes on requires an estimated point value. When estimating a task, the point value assigned is based on time, complexity, and unknowns. Ensuring tickets are broken down into sensible, actionable chunks can reduce unknowns and allow the team to point a ticket based on the task’s time and complexity. 

A good scale to use for point values is the fibonacci sequence (1, 2, 3, 5, 8, 13) because, as the size of a task grows, [so does the associated amount of uncertainty in executing it](http://www.scrum-institute.org/Effort_Estimations_Planning_Poker.php). 

A team should point each ticket as if any member were to execute it. Team members should therefore estimate each task as a group, and converge on a point value on which every member agrees.    

It doesn’t matter if two separate teams use a different type of scale or other practices specific to their pointing process, as long as they are consistent within their own team. For example, a team might decide to always revisit tickets that were assigned a point value of 13, because that suggests they reflect a task that has not been understood and broken down sufficiently. 

## Velocity Tracking

Let's say your team has finished pointing tickets and assigned them to team members. Now it's time to decide, how much should your team commit to as a whole for the next sprint? How does that translate into the total number of points that each team member should be assigned? 

Velocity tracking uses a team's average historical output to inform how much work (measured in total number of points) to commit to in the next sprint. Velocity tracking can also help a team reflect on how much work was accomplished during retrospective by comparing their *target* sprint velocity to their *actual* sprint velocity, [usually manifested as a burn-down chart](https://en.wikipedia.org/wiki/Burn_down_chart).

### What is Sprint Velocity?

`Sprint-velocity` describes the amount of work completed in a single sprint. `Average-sprint-velocity` is an average of the previous *n* sprints (where *n* might be 2 - 4). We use the `average-sprint-velocity` during sprint planning to determine how much work to commit to in the next sprint because it gives an overall sense of the how much work the team can reasonably accomplish. 

### How Do We Track Velocity?

If a team is planning their first sprint and has not tracked velocity before, they should use an initial value of 0.5 points per person-hour to get started. If a sprint is 2 weeks x 5, 8-hour days, then each person has a max of 80 available hours. For a team of 4 members, if the velocity is 0.5, that means each person is assigned 0.5 * 80 = 40 points worth of tickets. Thus the team as a whole has committed to 4 * 40 = 160 points to be completed over the duration of a sprint. 

Now let's say two weeks have passed, and the sprint is done: the team as a whole completed 128 points of the estimated 160 points they committed to. While their *projected* velocity was 0.5, their *actual* velocity is 128/320 = 0.4 point per person-hour. 

The team now has a velocity value based on their **actual** performance to plan the next sprint. Now the team knows to assign 0.4 * 80 available work hours = 32 points to each team member. Now, the team's estimated velocity for the next sprint is 0.4, and they might complete work at an actual velocity that hits above or below that value. The can then average this with the previous value to get a new velocity. 

Here are the calculations broken out:

> *total person-hours* = The sum of the hours each team member contributed to the sprint

> *total number of points completed* = The sum of the point values of tasks that are 100% “done”

> **sprint-velocity** = *total number of points completed* / *total person-hours*

> **average-sprint-velocity** = average **sprint-velocity** of previous *n* sprints

If a team member will only be able to contribute to half of a sprint, their `individual-velocity` will be 50% of the total number of hours in the sprint multiplied by the `average-sprint-velocity`. The individual velocity factors in the specific team member’s available hours and always relies on the average velocity for the team; it is never reliant on the individual’s previous velocities and individual velocity is never recorded at the end of a sprint (this is a team effort, the emphasis is on team performance).

> **individual-velocity** = *hours the team member can contribute to the sprint* * **average-sprint-velocity**

*Note: Dividing the total points by the total hours results in the smallest possible unit of one point, per one person, per one hour aka `sprint-velocity`. Since `sprint-velocity` is broken down to the smallest unit, it can scale well with any number of team members as well as any number of days in a sprint.*

### Why Do We Track Velocity?

Velocity tracking has several benefits ranging from better scoping and more accurate estimation to more reasonable workloads and increased team predictability. Velocity tracking improves task definition because well defined tasks are a prerequisite to accurate estimation. 

Task estimation is a difficult process but it naturally improves from sprint to sprint as the team retrospects how they estimated. By measuring each sprint against a previous one, it is easier for the team to identify which areas need improvement (estimation, overcommitment, excessive blockers, etc). After tracking velocity for a few sprints a team should see a considerable improvement in comfort (i.e. committing to just the right amount of work), predictability, and consistency.

##Exchange Program

In order to promote personal growth and inter-team knowledge transfer we offer an engineering exchange program. An exchange is a single or multi-sprint-long period where an engineer from another group can contribute to one of our projects in a structured way. This is an opportunity for exchange participants to learn new platforms, languages, and team processes.

When someone participates in an exchange they are paired up with a member of the team that's working on the project that they'll be contributing to. This point-person helps them get set up and provides guidance and mentorship during the exchange. Exchange participants attend all sprint planning meetings, daily scrum, and sprint retrospective.

##Notes

1. At the time of writing, the Vimeo Mobile & TV Group is comprised of roughly 20 people. 
2. To track velocity, we use [Pace-iOS](https://github.com/vimeo/Pace-iOS) and [Pace-Android](https://github.com/vimeo/Pace-Android) (both coming soon).
3. We use Confluence for most documentation, but any wiki-like tool will do.
4. We use Jira for task management, but tools like Trello, Zenhub, or a simple whiteboard or post-it note wall will work.

##Contributors

Ryan Casey    
Brian Cooper   
Alfie Hanssen    
Jason Hawkins  
Aaron Hedges  
Julie Ho    
Rob Huebner  
Will Hutson  
Gavin King    
Nicole Lehrer    
Stephen Levinson    
Toan Pham    
Anthony Restaino    
Howard Rigberg    
Jon Sheldrick    
Dina Solovey   
Kenya Stewart   
Andy Thompson    
Will True    
Mike Westendorf    
Kyle Venn    
Kevin Zetterstrom    

