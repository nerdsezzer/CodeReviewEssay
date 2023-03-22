---
Code Review Essay
---


Introduction
---

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

Making code review as easy and as accessible as possible by ensuring standards are agreed before implementation, providing access to static analysers within the development/CI environment and code review facilitating systems, such as Atlassian’s Crucible, etc. all help to promote the use of code review within a team, and reduce the total overhead of conducting the reviews.
and build competence within a team; it's a great way to share knowledge, keep fresh and learn more deeply about the language we're using.


First, check your ego at the door!
---

Code reviews are not meant to showcase language expertise, but rather to demonstrate one's ability to handle the complexity of the language.  When selecting code reviewers, it is important to consider their understanding of language paradigms that can increase complexity and hinder readability for the majority of the team.  For instance, consider operator precedence rules in the C language, to avoid assuming everyone knows these in detail, a rule was created that all non-obvious reliance on operator precedence should use brackets to improve understandability.  The ultimate goal of code reviews is to improve code quality, maintainability, and understandability for the entire team.

It's crucial to select code reviewers who possess a thorough understanding of language paradigms that can heighten complexity and impair readability for the team at large. As an example, in the C programming language, operator precedence rules can pose challenges for some team members, and a useful guideline is to rely less on non-obvious operator precedence and instead use brackets to enhance clarity. Ultimately, the aim of code reviews is to enhance code quality, maintainability, and comprehensibility for the entire team.


to be continued...


Code Review Maturity Matrix
---


[1]. McConnell, S. (2004). Code Complete: A Practical Handbook of Software Construction, Second Edition. Microsoft Press.
