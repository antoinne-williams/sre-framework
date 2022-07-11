# SRE Framework Blueprint

<details><summary>Introduction</summary>

### Introduction

The suggestions proposed in this document are intended to serve as a blueprint for developing an SRE framework within which the corresponding engineers operate, with a goal of achieving optimal productivity throughout the various stages of maturity.

Numerous resources exist on implementing DevOps and SRE, however, the largest and most successful sources of this information, like Google and IBM, often explain the ideal end state in the context of organizations of their vast size and capital as well as years of refinement. While their insight is helpful in identifying valuable options for practical application in this regard, their approach may not be viably applicable to a majority of small and medium sized businesses, especially those of whom that are starting the process of adopting these new principles and practices.
- An example of this is the characterization of the SRE role as 50% automation and 50% production support. This approach likely works extremely well for those organizations; conversely, smaller companies tend to benefit more from capitalizing on the unique skill set of SREs, specifically automation, whereas they'll already have departments dedicated to overseeing and responding to customer impacting incidents.

</p>
</details>

<details><summary>Stage 0: Prevision</summary>

### Stage 0:  Prevision

Predict and preempt surmisable challenges to the process in order to overcome known inhibitors and accelerate advocacy at the leadership level

- Understand historical deterrents to SRE implementation and adoption
  - Silos
  - Disjointed organizational structures which cause misaligned projects and deliverables
  - Lack of support at the senior leadership level and higher
  - Bureaucracy and "Red Tape"
  - Skepticism that automation will render certain roles obsolete

- Identify obstacles that may impede the transition to SRE principles and practices, as it pertains to the specific organization
  - Key personnel in positions of influence who subscribe to the traditional model of Development and Operations
  - Ineffective or non-existent cross-team communication
  - Strict and rigid internal processes that hinder agility (i.e. the ability to adapt to changes quickly)

- Evaluate internal talent, competencies, and processes to determine the most likely path to garnering  support and creating partnerships
  - Position automation and SRE adoption as opportunities for career path progression (CPP) and facilitate this arrangement by offering relevant training and defining achievable CPP goals
  - Key personnel in positions of influence who subscribe to the modern model of Development and Operations


</p>
</details>

<details><summary>Stage 1: Assess and Define</summary>

### Stage 1: Assess and Define

Assess the current state and designate engineering roles and resources accordingly

- Ascertain the business needs and KPIs

- Define SRE (and possibly other, adjacent engineering) roles to align with short and long term goals. Common classifications include:
  - Dedicated SRE team
    - For organizations that are just starting the DevOps transformation, instantiating this team can be advantageous, as engineers that are a part of this group can easily transition to the other types as maturity around this model improves.
    - The value of this approach includes setting the standards around SRE and developing practices and processes for subsequent SREs to follow
  - Embedded SREs
    - Useful for introducing SRE practices into a team that otherwise might not have exposure
  - Consultative SREs
    - An opportune approach for organizations that can provide flexibility and freedom to this group, so that deliverables can be handled in a way that is untethered by other teams' processes, but still meet or exceed prescribed targets

- Define skill levels for the SRE career track, which will also assist with interviewing and placing internal and external candidates

- Discuss plans for the future state of the business and the SREs role in achieving it, in order to determine how to continuously align with the long term goals

- Identify opportunities for active, consistent, and reasonably manageable advocacy of internal teams with whom we expect to collaborate directly. While this may present challenges to achieve, especially in larger companies, even moderate success in this pursuit can be instrumental in establishing relationships and building trust.
  - Architecture Advocacy
    - Work with the Architecture team to determine whether the coding  and testing implementations are architecturally-aligned, if applicable, and assist the corresponding teams with accommodating this approach
  - Developer Advocacy
    - Assist Developers with optimizing and accelerating their processes as well as improving the SDLC, where possible
    - Endorse the notion of Developers understanding, and possibly managing (using prescribed standards), the infrastructure upon which their services reside, in the environments that they are accustomed to, as a mechanism to expand their insight into the configurations that constitute what is expected in higher environments (a key tenet of DevOps). This should be proposed after infrastructure management has been automated or streamlined to the point where the Developers don't need to spend significant cycles on it, as that negates the value gained from this approach
  - Quality Advocacy
    - Automate testing and promote the quality processes as integral to determining the viability of the tested code (i.e. the importance of Dev-Prod parity for unit, integration, performance, and functional tests)
  - Security Advocacy
    - Encourage Security's processes in all aspects and stages of deployment
  - Network Advocacy
    - Support network configurations across all environments, especially when promoting parity
    - Recommended and assist with automation, if necessary, where practical for SREs
  - Operations Advocacy
    - Automate manual and repetitive tasks and propose that Operations adopt this approach going forward (specifically, solving Operations issues with Software Engineering, a key tenet of DevOps)
    - Review and streamline monitoring by identifying noise as opposed to truly actionable alerts and modifying accordingly.


</p>
</details>

<details><summary>Stage 2: Implementation</summary>

### Stage 2: Implementation

Create an action plan to implement the SRE roles (and associated levels), processes, and engagement model
- Action Plan example:
  - Roles:
    - SRE
      - Levels
        - I - Junior
        - II - Intermediate/Mid-level
        - III - Senior
        - IV - Lead
        - V - Staff
        - VI - Principal
        - VII - Distinguished (awarded level; outside of typical CPP)
  - Engagement Model (overview)
    - SRE leadership convenes with the target team's leadership to identify their needs and whether there is alignment with the services offered by SRE, after which time, a document that includes the particulars of the workstream and acceptance criteria is composed, reviewed, and agreed upon by both sides prior to the initiation of the project.
  - Processes
    - Source Control and Peer Review
      - All code written will need to be contained within an SCM tool in order to facilitate collaboration inside and outside of the team, as needed.
      - The Merge/Pull Request process inherently affords the opportunity for teams to   conduct peer reviews for code contributions. It is incumbent upon the team to establish and uphold a reasonable standard of quality (may be referred to or implemented as: quality bar, quality standard).
    - Monitoring and Observability
      - Review the current implementation, tools, alerts, etc and determine what needs to be improved or added
        - System monitoring
        - Application Performance Monitoring (APM)
        - Service and endpoint healthchecks
      - Isolate the alerts that generate noise from those that are actionable and work towards either eliminating or refactoring them as necessary
    - SLI, SLO, SLA
      - SLIs and SLOs: Work with the developers to create reasonable SLOs for the corresponding services and build SLIs to measure the SLOs. Consider options for visualization.
      - SLAs: Once reliability efforts have yielded results, SLAs may be in a position to be reviewed and optimized for the customers, potentially providing favorable circumstances for the Sales team.
    - Error Budgets
      - Normalize the expectation of service failure (i.e. an SLA of 99.99% infers that 00.01% of the time, the service can be down without infringing upon the contractual obligation), while accounting for expedient recovery. As a result, it is possible to more accurately define acceptable downtime so that developers know when they are within a threshold to either take risks with the release cycle or take a more cautious approach, based on how much acceptable unreliability remains.
    - Scrum-like Daily Updates
      - A key principle behind Scrum stand-ups is ensuring short, but informative meetings (max: 15 minutes, per Scrum guidelines) that outline progress and blockers.
      - Constructing the stand-up to include updates from the previous day (Last 24), expectations for the current day (Next 24), and blockers from all members of the team intrinsically injects built-in accountability into the process. This approach can counteract challenges with stand-up participation as well as foster expanded communication with remote employees.

</p>
</details>

<details><summary>Stage 3: Establish initial workstreams and the foundation for future engagements</summary>

### Stage 3: Establish initial workstreams and the foundation for future engagements

 - Initiate communication with Development, Operations, Quality, Security, and other teams to discuss opportunities for engagement including:
    - Existing toil, i.e. processes that are:
      - Manual
      - Time-consuming
      - Repetitive
      - Reactive
    - Pain points
    - Monitoring and Observability
    - Service Level Management
    - Release Management
    - Testing

- Define the initial projects that the SRE team will work on and the benefits of those efforts
  - Provide measurable, data-driven results where possible
    - Example: Before -N- project started, the process required -X- time to complete. After the engagement reached its conclusion, the execution of the process has been reduced to -Y-, which is an improvement of -Z- percent or unit of time.
  - Emphasize relationship building and establishing trust between teams.
  - Prioritize quick, valuable wins to bolster the SRE team's profile, particularly in the early stages.

</p>
</details>

<details><summary>Stage 4: Revision (Continuous Refinement)</summary>

### Stage 4: Revision (Continuous Refinement)

Understand that the success and cultivation of this implementation is largely contingent on the ability to adapt and course correct when a process has been deemed as ineffective or less effective over time. It is, therefore, incumbent upon the stewards of this framework to continually assess our results and make the necessary adjustments.
- Data-driven results provide solid metrics by which the effectiveness of a process can be quantified, however, in many cases, whether a process is yielding the results that are expected can be organically determined by the participants. Because of this, being willing to pivot quickly when needed will help in achieving success while minimizing the loss of productivity cycles.

</p>
</details>

<details><summary>Other Considerations</summary>

### Other Considerations

- Self-healing systems, services, and operations
  - As a hallmark of modern Operations, implementing automated remediation at the system, application, and process level is immensely beneficial in decreasing downtime, improving mean time to recovery (MTTR), and improving supportability by eliminating human error. It is also important in establishing a mindset of proactive, instead of reactive, incident response.
  - Targeting known issues as candidates for self-healing operations can be an opportunity for quick wins in Stage 3.

- Blameless culture
  - Promoting a blameless culture greatly improves internal relationship building and process refinement, in that, a failure is not tied to an individual and, therefore, there is no chastisement, rather there was a breakdown in process that needs to be assessed and corrected. Using this approach, there is a concerted effort placed on improving the processes to the point where the business is in a position to consistently observe and expect a minimal level of success of said processes, irrespective of skill level (self-healing and automated remediation works well for this example).

- Organizational and Engineering maturity
  - A proper assessment here should serve as a guide in appropriately determinating the most effective approach to a solution or project as well as more accurately defining reasonable timeframes
    - Embrace graduality and iterative improvement where needed. For example, if a project is an epic, break down the deliverables in meaningful ways, while still working to meet and exceed proposed timelines by leveraging technologies and processes that are in line with the maturity of the organization.
  - The DevOps Maturity Model provides viable milestones that can be used to accurately determine progress.
    - **Stage 1: Initial**
      - Traditional separation between Development and Operations.
    - **Stage 2: Managed**
      - In this stage, the mindset change required to start the DevOps transformation begins to permeate throughout the organization. Development teams' focus on velocity, efficiency, and agility and Operations begin to prioritize and implement automation with regularity. There is also an emphasis placed on collaboration and expanded cross-team communication.
    - **Stage 3: Defined**
      - Automation is more prevalent and processes are more well defined and consistently adhered to. The DevOps transformation is beginning to tangibly and observably take shape organization-wide.
    - **Stage 4: Measured**
      - At this stage, processes and automation are prominent enough to substantiate the collection of free metrics, which  be leveraged to further improve this model.
    - **Stage 5: Optimized**
Successes are considerable and visible; silos are broken down and collaboration is frequent and effective, which is reflected in the results of projects and the quality and velocity of project delivery.

- Everything-as-Code / X-as-Code
  - Approach systems, services, and processes with a goal of achieving their desired states in a declarative, programmatic way
    - Infrastructure-as-Code
    - Configuration-as-Code
    - Network-as-Code / Software Defined Networking
    - Security-as-Code
    - Pipeline-as-Code
    - Database-as-Code
    - Policy/Compliance-as-Code

- "Automate Everything" mentality
  - While there is much overlap with this and X-as-Code, the objective here is shifting to and perpetuating the mindset that all manual actions can be and, more importantly, should be automated as the first option.
    - An example of how to enact this would be to suggest performing an action manually once in order to understand the dependencies and desired state, then automate the same action as soon as possible (specifically, before the next time the action is needed)

- Mutable vs Immutable Infrastructure
  - Mutable infrastructure basically consists of servers that can be manually modified. The concept of Pets vs Cattle falls under this category.
    - Pets represent the traditional approach to server management, in that, each server is treated as unique and critical such that losing one produces catastrophic results.
    - The notion of cattle is more modern and resilient than pets because servers that follow this model can be destroyed and replaced with minimal impact, due to the fact that the configurations are identical and implemented in a consistent and repeatable manner.
  - Immutable infrastructure cannot be modified in any way after provisioning. The OS image includes the corresponding applications and configurations needed for the services to run successfully, immediately after being spun up. This is the most restrictive type of infrastructure, but also the most secure and scalable. When changes are required (like configuration updates, OS patches, new application versions), the OS image needs to be updated and redeployed.

- Zero downtime (ZDT) deployment strategies
  - The foremost benefit of this approach is inherent in the name, however, one of the critical aspects of this model is ensuring that rollbacks are as equally unobtrusive as the release process itself. Backward and forward compatibility of the release is another consideration which helps facilitate smooth updates and rollbacks (though there should be a process to account for major releases that may introduce functionality that breaks compatibility).
Common strategies include:
    - Atomic
Storing past, current, and upcoming release artifacts in a structure that enables rapid deployment by linking to the target release (or rollback) version.
An example would be creating a current directory that includes the expected release version and a releases directory that has all of the versions that might be used and using symlinks to set the current deployment.
    - Blue/Green (A/B)
Setting up equivalent infrastructure that mirrors the live environment (which would be updated) and deploying the updated release to the mirror, then validating and directing traffic there. Updates can then be applied to the original set or the previous release can remain for easy rollback by directing traffic back to it.
    - Canary
Deploying updates to a subset of servers (which would be taken out of service) in the environment in a rolling fashion until the entire set has been completed.

- GitOps
  - With the GitOps model, traditionally manual system and platform operations are handled in an automated way. The trigger for these actions is a pull request from Git. This requires that Git is the source of truth for the desired state (via declarative specification) of the target environments.
  - A common (and simplified) characterization of GitOps is "Operations by Pull Request".

- CI/CD
  - Evaluate the current deployment process, automate manual operations, and convert the steps into stages in a CI/CD pipeline. Common stages include:
    - Code checkout
    - Code compile (if needed)
    - Code quality scans
    - Security, vulnerability, and compliance scans
    - Unit testing
    - Package code
    - Acceptance testing
    - Deployment
  - Benefits:
    - Deployment velocity
    - Quicker fault isolation
    - Better feedback loop on the deployment process
    - Test reliability
  - Understand that handoffs and approval gates (usually imposed as a result of segregation of duties) drastically slow down the release process. 
    - Devise a plan to effectively accommodate testing and approvals in a manner that works within a CI/CD pipeline

- Scaling Optimization: Applications/Services and Infrastructure
  - Identify how scaling is handled at present and what factors dictate whether scaling will be horizontal or vertical. If the process is data-driven and concrete parameters inform the decision in a systematic way, it is typically safe to consider automating the conditions as currently constructed. On the other hand, if the process is loosely defined or highly reactive, converting it intto a more data-driven operation would be a useful first step.
  - Pursue autoscaling based on system, application, and business relevant metrics.

- Risk Management
  - Effectively managing risks is the responsibility of the organization at large, however, accounting for risks, in any magnitude, within engineering practices can be helpful in determining safe (as decided upon by the business) options for implementing a given solution.
  - The ISO 31000 and COSO ERM risk management frameworks offer valuable insight into capably handling risk management in a comprehensive way (i.e. more suited for org-wide consideration; likely too extensive for SRE or any individual team to incorporate into their workflows, but a solid basis to pull viable processes from)
  - Concepts for engineering teams to consider in their workflows:
    - Positive risk
      - As the most favorable type of risk, this can be categorized as a minimal negative impact-high reward scenario. In a general sense, conditions that yield high value in their attainment, but only costs engineering cycles (POCs that require a moderate amount of time, for instance) are prime examples of positive risk
    - Negative risk
      - In short, anything that poses a tangible threat to business goals
    - Risk thresholds
      - The minimum and maximum acceptable levels of risk, as defined by the business. This may or may not be directly useful to SRE, but, understanding that it may be a consideration down the line, could be helpful in effectively assessing risk at the engineering level, respective to the specific organization.

- Loosely define the process of evaluating trade-offs, concessions, and compromises when considering the viability of proposed solutions  respective to business need, engineering maturity, maintainability, etc

- Assess, then reduce and eliminate technical debt
  - While this is not explicitly a function of SRE, generally technical debt is amassed and accrued over time, but not addressed with priority as a direct result of availability, or lack thereof.
  - This may be a high value opportunity which can be pursued as a part of Stage 3
  - The expectation should be reasonable, i.e. reduce and eliminate technical debt where most feasible without encroaching upon other, higher value opportunities and without the expectation that 100% of technical debt will be addressed, if that is not a realistic possibility.

- Regularly publicize the recognition and acknowledgement of effective and successful collaboration and promote this behavior as a cornerstone of the culture
  - This can be helpful in building relationships, establishing trust, and fostering favorable lines of communication

- Incentivization
  - DevOps/SRE adoption can be very challenging to achieve for any organization, even in early stages. Providing incentives to the individuals who would convert to this new model has yielded excellent results, based on my observations and experience.
    - This approach treats the transformation as an investment and drastically improves engagement as well as active participation and collaboration.
    - As the most effective incentives might include monetary gifts or additional PTO (if it is not already unlimited) upon meeting predefined criteria, it requires buy-in and coordination with the business, but this has also been difficult to get support and approval for, even if it is historically proven to have the highest success rate in driving and achieving adoption.


- Cloud-Native Design Principles
  - Organizations customarily elect to lift-and-shift platforms from on-prem in an effort to start their migration to the public cloud. While there is merit to this approach (which is referred to as "cloud enabled") depending on the circumstances and goals, the optimal strategy would be to adopt and implement cloud-native technologies from the beginning of the process in order to leverage the substantial benefits that they provide.
    - The most notable detractor to this approach is engineering cost (from the perspective of time and effort). Transitioning from a traditional architecture to cloud-native often requires rewriting applications in order to facilitate compatibility and ultimately take advantage of the technology.
    - Key benefits:
      - Faster, more reliable releases, due to built-in support for CI/CD workflows. From a business perspective, this expedites time-to-market.
      - Reduced costs as a result of cloud standards. For instance, compute and storage can be allocated as needed, therefore costs can be minimized by spinning down resources when they are not in use.
      - Fault tolerant systems. Cloud-native technologies inherently include resiliency and self-healing, so there is no additional engineering cost to achieve this.
      - Independent scalability. Because cloud-native microservices perform a single task, they can be scaled horizontally without affecting any other service. 

</p>
</details>


