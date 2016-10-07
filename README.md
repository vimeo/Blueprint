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

Teams are externally trusted, transparent, and accountable. Teams are internally creative, balanced, and practical. Teams typically include a product manager, designer(s), engineer(s), and a QA representative. Read more about the product manager's core responsibilities [here](/PRODUCT.md).

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
4. We [estimate the amount of effort required to complete each chunk](#task-estimation), and
5. We commit to a specific subset of chunks by using our historical team [velocity](https://en.wikipedia.org/wiki/Velocity_(software_development)) and the [Pace apps](#notes)<sup>2</sup> to calculate how much each person should take on.

![Sprint planning](/assets/sprint-planning.png)    
<sup>*Sprint planning*</sup>

During a sprint we track progress using a [scrum or kanban-like board](#notes)<sup>4</sup> with status columns for To Do, In Progress, Blocked, Ready for Review, Ready for QA, and Done. 

After finishing a sprint we hold a retrospective to discuss what went well, what didn't go so well, and what we decide to do differently next sprint. Part of retrospective involves examining our [burndown chart](https://en.wikipedia.org/wiki/Burn_down_chart) to gauge the accuracy of our estimates and inform how we estimate and commit to the next sprint's tasks. Retrospective is also the perfect time to adjust the process to better suit our needs.

The following sections provide more detail on specific phases of sprint planning mentioned above. 

##Task Estimation 

Each task requires an estimated point value based on time, complexity, and unknowns. Ensuring tickets are broken down into sensible, actionable chunks can reduce unknowns and allow the team to point a ticket based on the task’s time and complexity. A good scale to use for point values is the fibonacci sequence (1, 2, 3, 5, 8, 13) [because it reflects that uncertainty on how to execute a task increases with task size](http://www.scrum-institute.org/Effort_Estimations_Planning_Poker.php).

A team should point each ticket as if any member were to take it on. This increases team flexibility and improves the quality of task estimation. Team members should therefore estimate each task as a group, and converge on a point value on which every member agrees. One method is planning poker, in which each team member reveals their individual point estimation of a task at the same time before the team collectively decides on the appropriate point value. 

In practice, estimating point value based on time alone without considering the complexity or associated unknowns of a task can lead to poor estimation. However, a variable like complexity does not have inherent upper and lower bounds, whereas the maximum amount of time available can easily be determined.

It can be helpful to consider brackets of time when pointing to set some common ground among team members amidst discussion of a task's complexity and unknowns. In the example table below, a low complexity 3-point task might take closer to 4 hours for the average team member to complete, while a high complexity 3-point task might take closer to 8 hours.  

Points | Time range
:----:|:----------:
1 | A few minutes
2 | A few hours
3 | Half a day
5 | 1 day
8 | 2 - 3 days
13 | 1 week

<sup>*Example of how a team maps ranges of time to point value to facilitate task estimation*</sup>

The table above (and best practices in pointing in general) is by no means prescriptive. A team should determine in practice the guidelines that work for their needs. 

It does not matter if two teams use different pointing scales or rules of thumb, as long as they are consistent within their own team. For example, a team might decide to break any tasks assigned a point value of 13 into multiple, smaller tickets because a 13 suggests the task is too vague or has too many unknowns. 

## Velocity Tracking

Velocity tracking uses a team's average historical output to inform how much work (measured in total number of points) to commit to in the next sprint. Velocity tracking can also help a team reflect during retrospective on how much work was accomplished by comparing their *estimated* sprint velocity to their *actual* sprint velocity, often [visualized with a burn-down chart](https://en.wikipedia.org/wiki/Burn_down_chart).

### What is Sprint-Velocity?

`Sprint-velocity` describes the rate at which work is completed over the duration of a sprint. In other words, sprint-velocity reflects the number of points completed by the average team member in one hour (or points per person-hour).

When using sprint-velocity to plan a sprint, a team typically wants to know its average velocity across fairly recent sprints to get an overall sense of a comfortable pace. We will refer to this later as the `average-sprint-velocity`.

### How Do We Measure Sprint-Velocity?

1. Determine the number of total available hours for the next 2-week sprint. If a team has 4 members, and each can contribute 40 hrs per week, there is a total of 320 person-hours. 

 > ***total person-hours*** = The sum of the hours each team member can contribute to the sprint
 
2. If a team is planning their first sprint and has never tracked velocity before, they should choose a "seed" sprint-velocity value, such as 0.5 points per person-hour, to get started. 

 > ***seed-sprint-velocity*** = number of points per person-hour
 
3. Multiply the seed-sprint-velocity by total person-hours to get the total number of points the team should commit to in the next sprint. Continuing our example, 0.5 points per person-hour x 320 person-hours = 160 points. 

 > ***total number of points committed to*** = *sprint-velocity* x *total person-hours*

4. Now let's say the sprint is done. The team as a whole completed most, but not all of the points committed to. While their *estimated* velocity was 0.5, their *actual* velocity is different. They completed 128 points / 320 hours,  so their team velocity based on the last sprint is 0.4 points per person-hour. 

 > ***sprint-velocity*** = total number of points completed / *total person-hours*

5. The team now has a velocity value based on their **actual** performance to plan the next sprint. Given the total person-hours available for that sprint, the team knows to assign a total number of points that reflects a velocity of 0.4. At the end of each subsequent sprint, the team will have another sprint-velocity sample they can use to calculate their **average-sprint-velocity** to plan future sprints. 

 > ***average-sprint-velocity*** = the average velocity across the previous *n* sprints (where *n* might be 2 - 4)

![Velocity tracking](/assets/velocityTracking.png)
<sup>*Snapshot of a team planning their first 4 sprints using velocity tracking*</sup>

Because sprint-velocity is measured in points / person-hour, it can be used with any number of team members, as well as any number of days, in a sprint. Note that Sprint 4 in the table above has 32 hours less than the previous because of a company holiday. The average-sprint-velocity can still be used to determine how many points to assign the team because it scales points based on the number of hours available. 

### How Many Points are Assigned to an Individual Team Member?

Typically the total points a team takes on is the result of each team member contributing equal person-hours to a sprint. But sometimes a team member needs to take time off or otherwise work at a lower capacity. This is accounted for by decreasing their available hours. 

If a team member will only be able to contribute to part of a sprint, their `individual-commitment` will be the number of hours they can commit times the `average-sprint-velocity`. 

> ***individual-commitment (points)*** = *hours the team member can contribute* x *average-sprint-velocity*

Total available person-hours is also adjusted to reflect the individual's decreased availability during the sprint. 

The velocity of an individual team member is never tracked. This emphasizes focus on the collective effort of the team, not the performance of an individual team member. 

### Why Do We Track Velocity?

Velocity tracking can over time increase the predictability of a team's output, which helps set more accurate expectations within a team. For example, the product manager can better estimate the timing of a release for a team of developers and designers with a predictable pace. 

Velocity tracking can highlight the need to improve task scoping, because well-defined tasks are a prerequisite to accurate estimation. 
Task estimation is a difficult process but it naturally improves across sprints as the team retrospects how they estimated. By measuring each sprint against the previous, it is easier for the team to identify which areas need improvement (estimation, overcommitment, excessive blockers, etc). 

Velocity tracking helps keep workloads at a reasonable amount. After tracking velocity for a few sprints a team should see a considerable improvement in comfort (i.e. committing to just the right amount of work), predictability, and consistency.

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

