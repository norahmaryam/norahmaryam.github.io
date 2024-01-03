---
title: "Slow is smooth, and smooth is fast"
summary: How a software delivery team used a data-driven approach to remove friction and deliver faster
date: 2024-01-01
series: ["PaperMod"]
weight: 2
aliases: ["/slow-is-smooth"]
tags: ["Software Engineering", "CICD", "developer productivity", "best practices", "shift left"]
author: ["Omer Ansari"]
---

### Backdrop

A few years ago my team brought Salesorce’s first-ever video streaming service, [Salesforce Plus](http://www.salesforce.com/plus) to life. We did it in a dramatic 4 month turnaround, prior to Dreamforce 2021. It was a smashing success and got much fanfare. 

Internally in the company it got a lot of visibility, and much like other projects which bring value to the company, it got more funding, and the expectations for the next Dreamforce got raised.

…and that's when the troubles started…

This is the story of version 2. The release that follows the Minimum Viable Product, and it is something I have seen a few times in my career. This is typically where the “**problems of the plenty**” start. Plenty of funding, plenty of interest, plenty of new requirements, and plenty of challenges!

The complexity and variety of issues afflicting the product during this particular phase caused us to lose many months of quality development time. With only 3 months (or 6 development sprints) left and a mountain of unfinished work before the upcoming Dreamforce, we had a “do-or-die” situation. We could fail to deliver, and that would cause us to launch some crucial software features which would impact potential marketing pipeline. Bad for our team, bad for the company, and not acceptable!

*Note: All diagrams and figures in this article are directionally accurate to convey the concepts, but all numbers and labels have been anonymized.*

---

### Surge Funding

Now, in IT, the fastest way to add capacity is through contractors and a healthy mix of an employee to contractor ratio is always good for the organization anyway. Typically, when a project is successful in its MVP launch, the business stakeholders want more of that and are willing to fund it. And adding capacity, if done thoughtfully, typically does yield value. However, if underlying bottlenecks already exist in the flow of work, and there always are, they become much more pronounced because they are stress tested. Indeed, some become full-on blockages when more work starts entering into the system.

Dr. Eliyahu Goldratt very articulately expressed this challenge in his seminal book, “The Goal” where he introduced to the world the “Theory of constraints” (TOC). TOC hypothesizes that every complex system consists of multiple linked activities, one of which acts as a constraint (aka, the weakest link) upon the entire system. ([link](https://www.linkedin.com/pulse/theory-constraints-real-estate-investing-cost-your-wyatt-powell)) We were about to learn this the hard way.

![regular](images/theory-of-constraints.png)

So, with a strong injection of capacity and a zest of ambitious software features, we were off to the races. Business stakeholders were truly excited. From a leadership perspective, all ducks were lined up in a row, and it was going to be a great unveiling of new features at Dreamforce.Inside the software development process, however, things were gunking up.

---

### There is friction in the system…

**Symptoms:** Since, at the time, we didn’t have clear [leading indicators](#1) for our software delivery process, we did not know that things were starting to slow down. There were complaints from engineers around untested code being committed, the front end team started to complain that their code was not getting merged and deployed, and the weekly updates on progress to the executive stakeholders showed little progress week over week. After the 5th week, my business counterpart executive reached out to me in exasperation and said something is seriously wrong. 

What are leading indicators? Taken from economics, leading indicators are signals early in a business cycle that give you the opportunity to influence the future since they are forward-thinking insights and predictions.

---



---



---



---


---

### Footnotes

<a name="1"></a> What are leading indicators? Taken from economics, leading indicators are signals early in a business cycle that give you the opportunity to influence the future since they are forward-thinking insights and predictions.
