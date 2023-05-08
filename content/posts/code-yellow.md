+++
author = "Ross Lazerowitz"
title = "Code Yellow: The Secret Weapon for Tackling Product Disarray"
date = "2023-05-08"
description = "A Potent Tool for Getting Things Done Fast"
images = ["/images/code-yellow.jpeg"]
tags = [
    "eng-management",
]

+++

![Header](/images/code-yellow.jpeg)

# Code Yellow: The Secret Weapon for Tackling Product Disarray

Are you a startup that's been heads down racing to build features and now finds yourself with more bugs than time or people? Or maybe you are a larger company that’s let your product fall into disarray? If this resonates with you, it's time to call for a Code Yellow and establish a War Room.

## What is a Code Yellow?

The term "Code Yellow" seems to have originated at Google [1]. In 2008, Google declared a Code Yellow to improve speed, granting a designated leader the power to recruit anyone within Google to help out, regardless of their current project.

> "In 2008, Google issued a Code Yellow for speed. (A Code Yellow is named after a tank top of that color owned by engineering director Wayne Rosing. During Code Yellow, a leader is given the shirt and can tap anyone at Google and force him or her to drop a current project to help out. -In the Plex Pg. 186"

There are four key components to a successful Code Yellow:

1. Problem Statement: Clearly define the problem and ensure it's agreed upon by all stakeholders.
2. Exit Criteria: Set specific, measurable goals to achieve, e.g., reduce latency from 5 seconds to 5ms.
3. Timeframe: Clearly define the start and end dates, as this operating model isn't sustainable indefinitely.
4. Workstreams: Divide the work into manageable sections, such as Availability and Design.

### The Code Yellow Operating Model in a Nutshell

- Appoint a War Room Chief Operator (usually the VP or Head of Engineering) and Operators for each workstream. These individuals can make decisions within their workstreams, with the Chief Operator having the final say.
- Implement a daily Standup to review the War Room backlog and provide status updates. A project management tool like JIRA can be helpful for tracking progress.
- Hold daily Office Hours for Operators to clarify scope, resolve disputes, or review requirements. This provides a clear channel for decision-making.
- Provide Daily Updates to the engineering team and stakeholders to keep them informed.

### Advice from the trenches

A Code Yellow is a challenging yet powerful tool in the engineering management arsenal. Use it with caution and keep the company and team's wellbeing in mind. The initial weeks will be disruptive, but always remember the importance of solving the problem at hand.

To help visualize this process, I’ve created a fictional Code Yellow Memo as an example. If you find yourself in need of a Code Yellow, consider sharing a similar memo with your engineering team.

## Example Code Yellow Memo

The Product Usability (PU) code yellow was declared today at the company kickoff meeting by Emma and Todd. We will hold a daily war room starting Feb 15th during the next 90 days to address first-day SWE usability issues.

The exit criteria of the code yellow/war room:

- Burn down the 266 bugs on the war-room1 list
- Achieve grade A for the six common workflows, which includes realizing new designs for consumption workflows
- Extensive use of the product for one hour will not encounter new bugs
- North Star: No sales loss due to product usability issues

The operating model of the war room:

- Small operators group: Todd for final calls, Phil for definition, and Ross for design
- Priority: Single List under war-room1 JIRA label, Decision In The Room
- Urgency: 1 Hour Daily War Room Standup With Engineers
- Overriding: Any Engineer That Is Tapped Will Join The War Room
- Communication: Daily Snippets/Weekly Update
- Output Driven: Interlock With Sales/Users Continuously

Workstreams:

- Coding workstream with UI/API engineers to fix bugs and code the design stream, led by Emma, code name Raid
- Design workstream with PM/designer/engineers for log, metric, dashboard new workflows, to get to approved designs and then hand it over to the Raid stream, led by Ross, code name Workshop

Meetings:

- 9:30-10:30 am PDT, Boredroom & Zoom. Attendees: anyone who is an assignee of the open Critical priority bugs on JIRA_LINK
- 4-5 pm PDT, the Left room & Zoom. Office hours for any Q/A
- Each workstream will have its own cadence per their needs

Communication:

- General communication channel: #pu-war-room
- Coding workstream: pu-war-room-raid (private)
- Design workstream: pu-war-room-workshop(private)
- Daily snippets are sent to the whole company via email by the operator group
- Monthly update to Board by Emma

Raid workstream war room rules:

- At 9:30-10:30 standup, we will run through the JIRA filter by Priority=Critical then assignee, bug by bug. We will not talk about bugs that are not in Critical priority
- The assigned developer should own the bug end 2 end, making sure requirement, design, and testing are all done properly, please don’t assign the bug out unless it means transferring coding ownership
- Please update your assigned bug initially with Understanding of the problem, Solution sketch, ETA (expected time to arrive), and then daily progress afterward
- On avg, we are hoping to complete an average of 1-2 bugs/day per engineer, you can pace accordingly. For large bugs that take weeks, try to break them down to help size and also parallelize
- If you are blocked, please @ your manager and Emma to unblock any time of the day
- If you have questions on clarifying requirement that is not addressed during the standup, please come to the office hours 4-5 pm Left Room physically or virtually starting this Wed

### FAQ

- What happens with the normal six-week sprint?
  - While the war room is one of the most important focuses of the next two sprints, we will still have a regular program and plans for the sprint, so that the important work that is NOT part of the war room can continue with the defined cadence.
- Do I expect to drop everything if I was assigned a critical war room bug?
  - If you don’t have critical customer bugs or production issues, you are expected to prioritize war room bugs. When there is a conflict and you are not sure, please ask in the pu-war-room or the raid channel. The other way is to do a quick triage of the bug and then ask what to do next.
- What if I am not clear on the requirement of the bug?
  - Please try to come up with the design, when doubt, tag the operators for clarification
- Why do you use war-room1? Is there a war-room2?
  - Every good thing will have a sequel, and the war room is no different, but let’s focus on the first one!

[1] https://markcarrigan.net/2016/01/10/googles-war-against-latency/
