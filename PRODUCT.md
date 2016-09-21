
##Contents

[Overview](#overview)  
[Requirement Documentation](#requirement-documentation)  
[Sprint Planning](#sprint-planning)  
[Development Sprint Mix](#development-sprint-mix)  
[Design Sprint Mix](#design-sprint-mix)  
[The How and When of Sprint Planning](#the-how-and-when-of-sprint-planning)  

##Overview 

On our Agile team, the product owner’s core responsibilities are to:
- Define and document feature requirements
- Plan sprints
- Maintain and prioritize feature and bug backlogs
- Maintain the product roadmap 
- Monitor and report on product KPIs. 

Every product owner does things a little different. Here’s how our team’s product owners tackle documentation and sprint planning.

##Requirement Documentation

Requirement documentation is the first stage in the process of building a feature - loosely defined as a new piece of functionality, whether it be user-facing, or something like new analytics. Before design or development can start building something, the team must have a shared understanding of the problems we’re trying to solve and why we want to solve them. Those questions are answered via a detailed document that should:

- Explain why we’re building the feature.
- Define behaviors or metrics we want the feature to drive.
- Define a high-level use case, or use cases.
- Identify any inter-team dependencies, if possible.

While not necessary, this document might also include high-level user experience recommendations, user flow sketches, market research, and product data.

##Sprint Planning

The product owner is responsible for planning and prioritizing all tasks in a sprint. We run distinct sprints for design and development teams, as each has their own cadence of how work is done. 

###Development Sprint Mix

Development sprints should be a mix of 5 distinct types of tasks: Features, bugs, technical debt, research, and QA. Each task type has it's own backlog in a project tracker tool (such as JIRA, Pivotal, or Zenhub). Every sprint should contain at least a few points worth of each task type, to ensure no single task type receives disproportionate attention. Committing to servicing all of these task types ensures we maintain product stability while still continuing to ship new and exciting features in the most efficient way possible. 

The product owner maintains and prioritizes a feature, bug, and QA backlog, while the engineering lead maintains and prioritizes the technical backlog.

- **Features:** Building new user-facing features, or optimizing existing ones. All feature work tasks are created by and for developers, and are created during developer research, defined below. 
- **Bug fixes:** Fixing issues uncovered by QA or user feedback. Bug tasks are created by QA and Product. 
- **Technical debt:** Improving the product via non user-facing improvements, such as library and/or SDK updates, performance optimizations, architectural modifications, etc.
- **Research:** Developing strategies for feature implementation. This task type involves reviewing design and product documentation and creating feature tasks for future sprints (research and implementation should not happen in the same sprint). Product creates and prioritizes research tickets.
- **QA:** Creating and executing test cases, and running regression tests. Our team creates distinct tasks for test case creation, test case execution, and bug fix verification. Product creates and prioritizes QA tasks.

When allocating developer time, we generally try to create a sprint mix consisting of 60% feature work, 20% bug fixes, 10% tech debt, and 10% research (QA tasks are handled by a dedicated QA resource). There are of course times when more bug fixing or technical debt is required. In those cases, we reduce the load of feature and research work to accommodate.

When the sprint mix is finalized and the tasks have been assigned, the product owner is responsible for prioritizing each engineer’s task queue. There should never be a question of ‘what do I do next?’. The answer should be dictated by the priority in the task queue.

###Design Sprint Mix

Designing a feature generally consists of 5 unique task types: Feature discovery, wireframing/prototyping, production design, reviews, and documentation. These tasks should be performed in this specific order, and can oftentimes span multiple sprints. We allocate time for each of these task types to ensure that no part of the design process is unaccounted for, so designers have plenty of time to review requirements and document their work before handing it off to developers. These tickets are created and prioritized by the product owner.

1. **Feature Discovery:** Gain a complete and holistic understanding of the feature and the associated requirements, and develop a high-level plan for how the design will be executed. It cannot start until the product owner has finalized the feature requirement documentation. It can involve any combination of reviewing product requirement documentation, performing competitive research, and running user tests. There are no required deliverables associated with the task, but if competitive research or user testing is done, that should be documented in Confluence.
2. **Wireframes and Prototypes:** Produce low-fidelity documentation that shows how a user navigates through a feature, and what types of design elements it might involve. Try to avoid using real images and styling - stick to black and white, blocky diagrams that show the structure of a feature, without defining its aesthetic. 
3. **Wireframe/Prototype Review:** Review the wireframes or prototypes with representatives from Product, Development, and QA. Discuss if it meets the product requirements, and the implementation feasibility. Designers should not proceed to production design until this has taken place.
4. **Production Design:** Create high-fidelity designs of screens, interactions, and other UI defined in the wireframing stage. Production designs should account not just for the ‘default state’ of a feature, but also edge cases like empty states, no internet state, etc. There are no required deliverables associated with this task.
5. **Design Review:** Review production designs with representatives from Product, Development, and QA. This is the last chance for any stakeholder to provide feedback or suggest changes before the feature is implemented (Once development has started on a feature, designs should not change).
6. **Documentation:** Export all production assets to Zeplin, and documenting any complex user interactions in a Confluence doc (if any exist). The designer should produce a deliverable that enables a developer to fully understand and implement the feature. 

For some design tasks, not every step in this cadence is required. For instance, if the feature is to add an additional option to a settings screen, wireframes are probably overkill. If the work is to simply update a current design, minimal feature discovery may be required. We try to use this cadence as a template, and then make adjustments on a feature-by-feature basis.

There are no guidelines for how long each of these tasks should take. Sometimes Feature Discovery could span an entire sprint, if in-depth user research is required. Alternatively, the entire cadence of tasks could happen in a matter of days if the design estimates the work to take that long.

###The How and When of Sprint Planning

A sprint should be fully ticketed and prioritized prior to your ‘Sprint Planning Day’, when the task assignment, planning poker and commitment meetings occur. Ideally, sprints are ticketed and prioritized far in advance of that day, so developers and designers have a chance to review tickets and provide feedback.

The easiest way to plan a sprint is with careful and consistent management of the task backlogs. For the development team, we have backlogs for each task type: Feature work, bug fixing, technical debt, and QA (research tasks are contained in the feature backlog). If each of these backlogs gets constant attention, planning a sprint is as simple as dragging the appropriate amount of tasks from each backlog into the sprint.

