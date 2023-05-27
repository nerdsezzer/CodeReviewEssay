
Introduction
===

The term technical debt refers to the cost of maintaining and updating software over time due to decisions that prioritise short term benefits over long-term goals.  It commonly occurs when developers take shortcuts or make compromises in the code to meet deadlines, but there are other factors that contribute to technical debt: lack of expertise, poor communication between developers and stakeholders, requirements creep, pace of change of technologies used, all of which can result in code that is difficult to maintain, update or extend.

Code review is an effective method of managing technical debt, by identifying areas of code that are poorly structured or hard to maintain, early in the development cycle, meaning bugs are less costly to fix.  It also ensures that code follows best practice and coding standards, which can make it easier to maintain and update over time.

Code review differs from code inspection, although both are methods used to improve the quality of software by looking at the code.  Code review is a collaborative process where developers review each other’s code, typically using a tool that allows for comments and replies.  The focus is finding and fixing bugs, improving code quality and ensuring that code meets the project requirements and standards.  Code reviews are less formal than code inspection.

Code inspection is a formal and rigorous process that involves a team of developers and technical experts thoroughly examining the code for defects, compliance with standards and adherence to best practice.  Code inspection involves a detailed review of the code, using a checklist.  The focus is on finding defects and improving the overall quality of the code, rather than just catching bugs.

What is the purpose of code review:
---

The purpose of code review is to improve the quality of software by having other developers examine and critique the code written by their peers.  Code review serves several purposes, including:
1.	Catching bugs and defects: Other developers can often spot issues that the original developer may have missed, which can help catch bugs and defects earlier in the development process.
2.	Improving code quality: By reviewing the code, developers can suggest improvements and best practices that can improve the readability and maintainability of the code.
3.	Sharing knowledge: Code reviews can be an opportunity for developers to learn from each other, share knowledge, and stay up to date with the latest technologies and techniques.
4.	Enforcing standards: Code reviews can help enforce coding standards and ensure that all developers on a team are following the same conventions and practices.

How does code review compare with testing:
---

Code review *and* testing are important methods to improve the quality of software, however, they differ in their focus.  Code review is focused on finding and fixing issues in code before it is released, testing is focused on verifying that the software meets its requirements and behaves as expected.  Whilst there is a large set of bugs that will be found via code review and testing, there are issues that code review is more adept at spotting:
*	Logic errors: where incorrect assumptions about data or functionality lead to errors, or where logic has been applied inconsistently. [1]
*	Performance issues: inefficient algorithms, expensive database queries etc, can impact a system’s performance .
*	Security vulnerabilities: catching instances where input validation is missing, etc, can leave an application vulnerable to attack.

As Edsger Dijkstra famously said, “Program testing can be used to show the presence of bugs, but never to show their absence!” 

Code Review, on the other hand, is a proactive approach for managing future technical debt.

Use of static analysis tools:
---

Why wouldn’t you?  Tool-assisted code review; this type of code review uses software tools to analyze the code and identify potential issues. The tools can be configured to enforce coding standards, identify potential security vulnerabilities, and provide automated feedback on code quality.

Types of Code Review:
---

Formal, informal, ad-hoc or even pair programming are all types of code review, the choice of which review is largely dependent on factors such as the size and complexity of the code, the development team’s preferences, the resources available and where the project is in its lifecycle.

*	Formal code review: This type of code review involves a formal meeting where a group of developers review the code together.  The code is typically presented by the author, and the reviewers provide feedback and identify issues that need to be addressed.
*	Lightweight code review: This type of code review is less formal than a formal code review and typically involves a smaller group of developers.  The review can take place in person or online, and feedback is typically provided via comments or annotations within the code.
*	Ad hoc code review: This type of code review is less structured than the other types and typically occurs on an as-needed basis.  Developers can review each other's code informally, either in person or online, to provide feedback and catch errors.
*	Pair programming: This type of code review involves two developers working together.  One developer writes the code while the other reviews it in real-time, providing immediate feedback and catching errors as they occur.

It is common place for a code review to be conducted when the author believes the code to be finished, however this 'big bang' approach can be costly to the project, if that is the only review that has been conducted.  

Code Reviews are about managing complexity, not egos!
---

Code reviews are not meant to showcase language expertise, but rather to demonstrate one's ability to handle the complexity of the language.  When selecting code reviewers, it is important to consider reviewers who possess a thorough understanding of language paradigms that can heighten complexity and impair readability for the team at large.  As an example, in the C programming language, operator precedence rules can pose challenges for some team members, and a useful guideline is to rely less on non-obvious operator precedence and instead use brackets to enhance clarity. Ultimately, the aim of code reviews is to enhance code quality, maintainability, and comprehensibility for the entire team.

to be continued...



What to fix, and what can go wrong?
---

Depending on the size and criticality of the code review, it may be the case that not all bugs, defects and issues found will be fixed.  Time pressures is the most common reason, why only a subset will be attended to.  It should also be noted that any time code is changed, there is a risk of introducing an additional bug, or bugs.  Depending on where inthe project lifecycle the review is happening it may mean that issues identified under the banner of maintenance are simply left as learning points for the author to consider/avoid in the next project.  Or left on the backlog to be completed as part of the next sprint/release.

For this reason it's important that to categorise issues found within a code review.


Coding Standards
===

Want to get rid of arguments and in-fighting within your dev team?  If the problems are around coding style; coding standards may be your solution.  The debate about whether programming is engineering or an art rages; my personal view is that coding is an art form, deliving reliable software requires engineering.  The choices in the solution space for a programmer at any given time is large, and how we make those choices is largely informed by our previous experience in programming, the language, the framework, and even the team around us.

The use of good coding standards reduces or removes completely any debate about what should be identified when conducting a review.

Where to start?
---

And of course, once captured a good conding standard represented 'wisdom'; a distillation of experience and best practice, gathered from the best within your organisation.

...

Summary
===

Making code review as easy and as accessible as possible by ensuring standards are agreed before implementation, providing access to static analysers within the development/CI environment and code review facilitating systems, such as Atlassian’s Crucible, etc. all help to promote the use of code review within a team, and reduce the total overhead of conducting the reviews.

and build competence within a team; it's a great way to share knowledge, keep fresh and learn more deeply about the language we're using.

...

Code Review Maturity Matrix
===

|                  | Initial / Ad-hoc | Organised & Repeatable | Defined | Managed & Sustainable | Optimise and automate |
|------------------|------------------|------------------------|---------|-----------------------|-----------------------|
|Review process (1) | Reviews are not factored into the development lifecycle, and are only called upon when concerns are raised about code quality.  Details of defects found are not captured formally. | Reviews are planned into the development lifecycle. Defects highlighted in the review are formally recorded. Code review tools are used. | Progress of the review and any follow-up work is formally reported. Estimates for time taken are based on organisational data. | Number and duration of reviews is reduced due to improved coding habits, deeper knowledge, and use of automation earlier in the development lifecycle. | Human inspection no longer required. Defect detection is fully automated. Leader in industry with quality operational excellence.|
| Coding standards (2) | Seniors review code without use of coding standards. | Open source, language specific, style guides and standards are used for all reviews. | Organisational coding standards and in-house style guidance are defined, agreed and used for all reviews. | Organisational coding standards are regularly reviewed /refreshed and adapt to feedback. | Organisational standards are automated. |
| Targettedness (3) | The reason for a review is not defined/articulated. | The goal of the review is made clear prior to the review starting. | Maintenance and style defects are not found during inspection, they are managed out of the code by automation. | Reviews focus on functional / design reviews, managing complexity, and domain specific ‘gotchas’, and are done earlier in the project reducing rework costs. | |
| Continual improvement (4) | Metrics are not captured, neither are recommendations for doing better next time. Use of linters is a personal choice. | Metrics and captured and reviewed at the project level. Static analysis tools / linters are deployed to reduce defects prior to the inspection. | Project metrics can be compared, baselines determined. Static analysis tools / linters are embedded in the CI pipeline. | Metrics are visible and contribute to improvement at the organisational level. | Real time metric visibility with insights. |
| Team impact	| Reviewees can feel like the goal posts shift, and that they’ve been setup to fail. Reviewers don’t discriminate between good coding practice and ‘I’d do it this way’. | Reviews are conducted professionally, and predictably. | Reviews are collaborative, ‘for the good of the project’ and less about personality and seniority. | Reviews are enjoyable and a chance to share knowledge of the language, system / application and domain knowledge. | Being accepted as member of the coding standards review team, is seen as an achievement. |


[1]. McConnell, S. (2004). Code Complete: A Practical Handbook of Software Construction, Second Edition. Microsoft Press.
