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

## Velocity Tracking

### What is Velocity Tracking?

Let's say your team has broken user stories into tasks that are each ticketed, pointed, and assigned to team members. Now it's time to decide, how much should your team commit to as a whole for the next sprint? How does that translate to the total number of points that each team member should be assigned for the next sprint? Velocity tracking can help you do that by using a team's average historical output to inform how much work (measured in total number of points) to commit to in the upcoming sprint. As such, velocity tracking is both used to help us (1) plan upcoming sprints and (2) reflect on how much work was accomplished during retrospective.

Velocity is a number that represents the amount of work completed by a team during a specific time period. Typically, we talk about “sprint velocity” and “average sprint velocity”. `sprint-velocity` describes the amount of work completed in a single sprint. `average-sprint-velocity` is an average of the previous *n* sprints (where *n* is something like 2 - 4 sprints). We use `average-sprint-velocity` during sprint planning to determine how much work to commit to in the sprint being planned.

### How Do We Track Velocity?

If the sprint you're planning is the first sprint where you'll be incorporating anything related to velocity then use a seed value of 0.5 for `average-sprint-velocity` to get your estimations started.

If all tickets in the previous sprint are pointed there's no need for a seed value and you can calcualte the `sprint-velocity` of the previous sprint and then the `average-sprint-velocity`. You do this like so:

> *total person-hours* = The sum of the hours each team member contributed to the sprint

> *total number of points completed* = The sum of the point values of tasks that are 100% “done”

> **sprint-velocity** = *total number of points completed* / *total person-hours*

> **average-sprint-velocity** = average **sprint-velocity** of previous *n* sprints

How to calcualte `total person-hours`? If your sprint is 2 weeks of 5 8-hour days then each person has a max of 80 available hours. But you might reduce this number if a company holiday falls within the sprint, if a team member is taking time off, or generally if someone's capacity is reduced for any other reason.

Once you have a real or seeded `average-sprint-velocity` you're ready to determine how many points each team member should commit to in the sprint you're planning. You do this by multiplying `average-sprint-velocity` by the `total person-hours` available in the sprint you are planning. The result is the total number of points the team should commit to. If every member of the team will be present for the entire sprint, the total points are divided evenly to each member (every individual’s contribution is considered equal). 

If a team member will only be able to contribute to half of a sprint, their `individual-velocity` will be 50% of the total number of hours in the sprint multiplied by the `average-sprint-velocity`. The individual velocity factors in the specific team member’s available hours and always relies on the average velocity for the team; it is never reliant on the individual’s previous velocities and individual velocity is never recorded at the end of a sprint (this is a team effort, the emphasis is on team performance).

> **individual-velocity** = *hours the team member can contribute to the sprint* * **average-sprint-velocity**

*Note: Dividing the total points by the total hours results in the smallest possible unit of one point, per one person, per one hour aka `sprint-velocity`. Since `sprint-velocity` is broken down to the smallest unit, it can scale well with any number of team members as well as any number of days in a sprint.*

### Why Do We Track Velocity?

Velocity tracking has several benefits ranging from better scoping and more accurate estimation to more reasonable workloads and increased team predictability.

Velocity tracking improves task definition because well defined tasks are a prerequisite to accurate estimation. When estimating a task, the point value assigned is based on time, complexity, and unknowns. Reducing the number of unknowns makes the point value more accurate because it removes ambiguity and allows the team to point solely on the task’s time and complexity. The point values the team chooses from should get progressively larger because as a task gets bigger, the number of unknowns increases. A good scale to use for point values is the fibonacci sequence (1, 2, 3, 5, 8, 13). In the example of the fibonacci sequence, task estimates should remain below a 13. If a task gets larger than an 8, that means that it is too vague and should broken down into several more specific tasks with their own point values. Team members should estimate each task as a group and converge on a point value that every member agrees with. This ensures that each task is pointed consistently and flushes out any additional unknowns. It doesn’t matter if two separate teams use a different scale, as long as they are consistent within their own team.

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

