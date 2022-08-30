# Crowdsourcing content creation for SQL practice (Leinonen, Pirttinen & Hellas, 2020)

<!-- they describe the design they built just for themselves -->

#phase-4a

<!-- they gathered feedback and report on it -->

#phase-4b

[the paper](./the-paper.pdf)

https://research.aalto.fi/files/54408038/SCI_Leinonen_Crowdsourcing.ITiCSE_2020_SQL_trainer.pdf

7 pages

States that there are not large differences between crowdsourced content created by novices and experts, or in this specific case, students and teachers. Implies that a system of creating/presenting/assessing these at web-scale would not only be feasible, but effective.

Points out that one of the main uses of crowdsourcing is to minimize time needed for content generation during each course iteration.

Peerwise is one of the mentioned examples, but it seems to be behind an institutional login, minimizing the overall accessibility. Presumably this is an effort at content-moderation, eliminating anonymous user submissions.

Also mentiones Crowdsorceror (a project available on GitHub as a frontend in React and backend in Rails) for students to submit templates and tests for programming assignments. Seems defunct, but another good idea. If we can set up a sandbox runtime for actually evaluating templates and turning them into runnable code, we can assert submissions against tests. This might be what we need GitPod for, since that's already sandboxed by default ... :thinking:

The method of assessment for the actual work done in the paper is to create two in-memory databases for each submission: one with the expected outcome of the "correct" sql query, and one with the outcome of the student's submitted query. They're probably talking more about "views" on a table, in postgresql's definition. Provided that the underlying data is the same, we want to compare the diff of a view (query) against that data with the one the student submits. Depending on where we host/run this, the cost implications are probably vastly different. And any reasonably-sized application doing this would need to take great care to limit the potential for SQL-injection attacks, possibly via parameterized queries and other mitigations.

The topics included simple SQL select statements on one or more tables, comparisons for limiting results, constructing aggregate queries, constructing nested queries, and altering the database schema (cre-ating, removing, updating tables, working with indices). In total, the teacher generated 45 SQL assignments into the system.

this would have been cool to try and run, but it's written in java and requires an Oauth server, so may attempt to reimplement at some point in another language.
