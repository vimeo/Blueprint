# Blueprint

aka **How We Collaborate** :zap:

##Contents

[Overview](#overview)  
[Why Process?](#why-process)  
[Team](#team)  
[Workflow](#workflow)  
[Sprints](#sprints)  
[Notes](#notes)  
[Contributors](#contributors)  

##Overview

This document is an overview of the [Vimeo Mobile and TV Group's](#notes)<sup>1</sup> product development process (a process based on the [scrum](#notes)<sup>2</sup> and [agile](#notes)<sup>3</sup> methodologies). It describes [why process](#why-process) is important and outlines three aspects of our process: [team](#team), [workflow](#workflow), and [sprints](#sprints). This document focuses on high-level guidelines rather than specific implementation tactics in order to leave room for teams to apply them as they see fit. 

##Why Process?

Process helps us to:
 
1. Produce high quality work at a predictable [pace](#notes)<sup>4</sup>, 
3. Promote the development of an extraordinary team.
 
##Team
 
A product team is a co-located, cross-functional group of roughly 4-7 people who collaborate to bring ideas to life. Proximity builds relationships. Cross-functionality fosters autonomy and self-sufficiency. Limiting team size promotes ownership.
 
![Team composition](https://github.com/vimeo/Blueprint/blob/working-draft/assets/team-composition.png)    
<sup>*Team composition*</sup>

Teams are externally trusted, transparent, and accountable. Teams are internally creative, balanced, and practical. 

The goal of a team is to produce meaningful, high quality work at a predictable [pace](#notes)<sup>4</sup>.
 
##Workflow
 
Workflow is a structured approach to how a team evolves an idea from inception to production. Teams evolve each idea one function at a time, with each function’s output being the next function’s input. 

![Workflow and deliverables](https://github.com/vimeo/Blueprint/blob/working-draft/assets/workflow.png)    
<sup>*Workflow and deliverables*</sup>

Consider an example where the idea we're working on is captured by this user story: *"As a user, I'd like to be able to upload videos to Vimeo from within the Vimeo iOS app."* The team's product manager creates a document detailing the feature requirements. The team's designer uses this document to generate wireframes, visuals, etc. The team's developer uses the product and design documentation to build the upload feature. And the team's QA representative tests the resulting build and either reports back with bugs found or approves it for deployment. 

The idea moves from one function to the next only when the current function's output has been reviewed and approved by each of the other functions. Approving an output means that it contains all info necessary for it to advance to the next stage. This helps us make decisions when we have enough info to make them (not before, not after). It also ensures cross-functional ownership at each stage.

We solicit feedback early, ask questions often, and [document and share what we learn](#notes)<sup>5</sup> along the way.
 
##Sprints
 
Sprints are structured 2-week intervals at which a team executes the above workflow to evolve ideas. Sprints help teams establish [pace](#notes)<sup>4</sup>.
 
![Sprint workflow](https://github.com/vimeo/Blueprint/blob/working-draft/assets/workflow-with-sprints.png)    
<sup>*Sprint workflow*</sup>

Before beginning a sprint:
 
1. We assemble a rough list of stories to be included in the sprint (a mix of product, design, dev, and qa stories),
2. We determine who will work on each story (via self-selection rather than top-down assignment), 
3. Assignees break each of their stories into small, actionable chunks,
4. We estimate the amount of effort required to complete each chunk (via [planning poker](#notes)<sup>6</sup>), and
5. We commit to a specific subset of chunks by using our historical team [velocity](#notes)<sup>7</sup> to calculate how much each person should take on.

![Sprint planning](https://github.com/vimeo/Blueprint/blob/working-draft/assets/sprint-planning.png)    
<sup>*Sprint planning*</sup>

![Sprint planning](https://github.com/vimeo/Blueprint/blob/working-draft/assets/sprint-planning.svg)    
<sup>*Sprint planning*</sup>

During a sprint we track progress using a [scrum or kanban-like board](#notes)<sup>8</sup> with status columns for To Do, In Progress, Blocked, Ready for Review, Ready for QA, and Done. 

After finishing a sprint we hold a retrospective to discuss what went well, what didn't go so well, and what we decide to do differently next sprint. This is also the perfect time to adjust the process to better suit our needs. 

##Notes

1. At the time of writing, the Vimeo Mobile & TV Group is comprised of roughly 20 people. 
2. [Scrum](https://en.wikipedia.org/wiki/Scrum_(software_development))
3. [Agile](https://en.wikipedia.org/wiki/Agile_software_development)
4. To track velocity, we use [Pace-iOS](https://github.com/vimeo/Pace-iOS) and [Pace-Android](https://github.com/vimeo/Pace-Android).
5. We use Confluence for most documentation, but any wiki-like tool will do.
6. [Planning poker](https://en.wikipedia.org/wiki/Planning_poker)
7. [Velocity tracking](https://en.wikipedia.org/wiki/Velocity_(software_development))
8. We use Jira for task management, but tools like Trello, Zenhub, or a simple whiteboard or post-it note wall will work.

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

