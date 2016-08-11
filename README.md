# Blueprint

aka **How We Collaborate** :zap:

##Contents

[Overview](#overview)  
[Why Process?](#why-process)  
[Team](#team)  
[Workflow](#workflow)  
[Sprints](#sprints)  
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

These checks and balances increase our chances of success and predictability by helping us define problems more accurately and therefore making us less likely to encounter issues down the line. However, problems are not always avoidable and this is where a willingness to engage in iterative product development is important.

We solicit feedback early, ask questions often, and [document and share what we learn](#notes)<sup>3</sup> along the way. 

##Sprints
 
Sprints are structured 2-week intervals at which a team executes the above workflow to evolve ideas. Sprints help teams establish [pace](#notes)<sup>2</sup>. Pace is valuable because it allows us to predict how long things will take in the short and long term. 
 
![Sprint workflow](/assets/workflow-with-sprints.png)    
<sup>*Sprint workflow*</sup>

Before beginning a sprint:
 
1. We assemble a rough list of stories to be included in the sprint (a mix of product, design, dev, and qa stories),
2. We determine who will work on each story (via self-selection rather than top-down assignment), 
3. Assignees break each of their stories into small, actionable chunks (defined in, for example, Jira tickets or Github issues),
4. We estimate the amount of effort required to complete each chunk (via [planning poker](https://en.wikipedia.org/wiki/Planning_poker)), and
5. We commit to a specific subset of chunks by using our historical team [velocity](https://en.wikipedia.org/wiki/Velocity_(software_development) and the [Pace apps](#notes)<sup>2</sup> to calculate how much each person should take on.

![Sprint planning](/assets/sprint-planning.png)    
<sup>*Sprint planning*</sup>

During a sprint we track progress using a [scrum or kanban-like board](#notes)<sup>4</sup> with status columns for To Do, In Progress, Blocked, Ready for Review, Ready for QA, and Done. 

After finishing a sprint we hold a retrospective to discuss what went well, what didn't go so well, and what we decide to do differently next sprint. Part of retrospective involves examining our [burndown chart](https://en.wikipedia.org/wiki/Burn_down_chart) to gauge the accuracy of our estimates and inform how we estimate and commit to the next sprint's tasks. Retrospective is also the perfect time to adjust the process to better suit our needs. 

##Exchange Program

In order to promote personal growth and inter-team knowledge transfer, the Mobile & TV Group offers an exchange program. A exchange is a single or multi-sprint-long period where a colleague from another group can contribute to Mobile & TV product development in a structured way. This allows the opportunity to learn new platforms, languages, and team processes.

If you're doing an exchange, you'll attend all sprint planning meetings and the retrospective. You'll be partnered with a member of the team to help get set up and provide guidance and mentorship along the way.

To apply for the exchange program:

1. Get approval from your manager,
2. Email gavin@vimeo.com about what you would like to work on.

We have the capacity to take on 1 or 2 people at a time per product, so we'll get back to you and start scheduling a start date.

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

