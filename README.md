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

This document is an overview of the [Vimeo Mobile and TV Group's](#notes)<sup>1</sup> product development process (a process based on [scrum](https://en.wikipedia.org/wiki/Scrum_(software_development)) and [agile](https://en.wikipedia.org/wiki/Agile_software_development) methodologies). It describes [why process](#why-process) is important and outlines four aspects of our process: [team](#team), [workflow](#workflow), [sprints](#sprints), and the [exchange program](#exchange-program). This document focuses on high-level guidelines rather than specific implementation tactics in order to leave room for teams to apply them as they see fit. 

##Why Process?

Process helps us to:
 
1. Produce high quality work at a predictable [pace](#notes)<sup>2</sup>, 
3. Promote the development of an extraordinary team.
 
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

Velocity is a number that represents the amount of work completed by a team during a specific time period. Typically, we talk about “sprint velocity” and “average sprint velocity”. Sprint velocity describes the amount of work completed in a single sprint. Average sprint velocity is an average of the previous *n* sprints (where *n* is something like 2 - 4 sprints). 

> **sprint-velocity** = *total number of points completed* / *total person-hours*

> **average-sprint-velocity** = average **sprint-velocity** of previous *n* sprints


The latter is useful in planning the amount of work to commit to in an upcoming sprint. 

Before a sprint is started the team assigns a point value to each task. This point value represents the estimated amount of effort that it will take to complete the task. At the end of the sprint the team uses these point values to calculate the sprint velocity. First, the team sums the point values of the completed tasks to get the *total number of points completed* (Footnote: Only include the point values of tasks that are 100% “done”). Next, the team sums how many hours each team member was able to contribute to the sprint to get *total person-hours*. Finally, the team divides the *total number of points completed* by the number of *total person-hours* in the sprint. The resulting value is the **sprint-velocity**. Dividing the total points by the total hours results in the smallest possible unit of one point, per one person, per one hour. Since **sprint-velocity** is broken down to the smallest unit, it can scale well with any number of team members as well as any number of days in a sprint.

When planning a sprint, the team determines how many total points they should commit to by multiplying their **average-sprint-velocity** by the *total person-hours* available in the sprint they are planning. The result is the total number of points the team should commit to. If every member of the team will be present for the entire sprint, the total points are divided evenly to each member; every individual’s contribution is considered equal. If a team member will only be able to contribute to half of a sprint, their **individual-velocity** will be 50% of the total number of hours in the sprint multiplied by the **average-sprint-velocity**. The individual velocity factors in the specific team member’s available hours and always relies on the average velocity for the team; it is never reliant on the individual’s previous velocities and individual velocity is never recorded at the end of a sprint.

> **individual-velocity** = *hours the team member can contribute to the sprint* * **average-sprint-velocity**

Velocity tracking has several benefits - it increases predictability, leads to more detailed tasks, and ensures all members of the team have an amount of work they feel comfortable with. Since **average-sprint-velocity** is the average of previous sprints, commitment should end with no member having too much to complete or too little to complete as it is based on how much work the team was able to finish in the past. The average also increases predictability by greatly improving the likelihood that the team will finish what they said they would finish. This prevents blockers because all dependencies of a task will have been resolved in a previous sprint.

Velocity tracking improves task definition because well defined tasks are a prerequisite to estimation. When estimating a task, the point value assigned is based on time, complexity, and unknowns. Reducing the number of unknowns makes the point value more accurate because it removes ambiguity and allows the team to point solely on the task’s time and complexity. The point values the team chooses from should get progressively larger because as a task gets bigger, the number of unknowns increases. A good scale to use for point values is the fibonacci sequence (1, 2, 3, 5, 8, 13). In the example of the fibonacci sequence, task estimates should remain below a 13. If a task gets larger than an 8, that means that it is too vague and should broken down into several more specific tasks with their own point values. Team members should estimate each task as a group and converge on a point value that every member agrees with. This ensures that each task is pointed consistently and flushes out any additional unknowns. It doesn’t matter if two separate teams use a different scale, as long as they are consistent within their own team.

Task estimation is a difficult process but it naturally improves from sprint to sprint as the team retrospects how they estimated. By measuring each sprint against a previous one, it is easier for the team to identify which areas need improvement (estimation, overcommitment, excessive blockers, etc). Within just a few sprints of velocity tracking, each team will see a considerable improvement in comfort, predictability, and consistency.

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

