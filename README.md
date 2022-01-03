# Software development methodologies

Contents:

* [Agile](#agile)
* [Kanban](#kanban)
* [Scaled agile framework](#scaled-agile-framework)
* [Scrum ](#scrum)
* [Disciplined agile delivery](#disciplined-agile-delivery)
* [Sprints](#sprints)
* [Six thinking hats](#six-thinking-hats)
* [Infrastructure as Code (IaC)](#infrastructure-as-code-iac)
* [Technical debt vs. unhedged call option](#technical-debt-vs-unhedged-call-option)
* [Run Until Caught](#run-until-caught)


## Agile

https://en.wikipedia.org/wiki/Agile_software_development

Agile Manifesto:

* Individuals and interactions over processes and tools

* Working software over comprehensive documentation

* Customer collaboration over contract negotiation

* Responding to change over following a plan

Principles:

* Our highest priority is to satisfy the customer through early and continuous delivery of valuable software.

* Welcome changing requirements, even late in development. Agile processes harness change for the customer's competitive advantage.

* Deliver working software frequently, from a couple of weeks to a couple of months, with a preference to the shorter timescale.

* Business people and developers must work together daily throughout the project.

* Build projects around motivated individuals. Give them the environment and support they need, and trust them to get the job done.

* The most efficient and effective method of conveying information to and within a development team is face-to-face conversation.

* Working software is the primary measure of progress.

* Agile processes promote sustainable development. The sponsors, developers, and users should be able to maintain a constant pace indefinitely.

* Continuous attention to technical excellence and good design enhances agility.

* Simplicity--the art of maximizing the amount of work not done--is essential.

* The best architectures, requirements, and designs emerge from self-organizing teams.

* At regular intervals, the team reflects on how to become more effective, then tunes and adjusts its behavior accordingly.


## Kanban

https://en.wikipedia.org/wiki/Kanban


## Scaled agile framework

https://en.wikipedia.org/wiki/Scaled_agile_framework

Principles:

* Take an economic view

* Apply systems thinking

* Assume variability; preserve options

* Build incrementally with fast, integrated learning cycles

* Base milestones on objective evaluation of working systems

* Visualize and limit work-in-progress, reduce batch sizes, and manage queue lengths

* Apply cadence (timing), synchronize with cross-domain planning

* Unlock the intrinsic motivation of knowledge workers

* Decentralize decision-making


## Scrum 

https://en.wikipedia.org/wiki/Scrum_(software_development)

Key roles:

* A "customer voice" a.k.a. "product owner role". This role that represents the product's stakeholders and the voice of the customer. The product hat creates roadmaps, is accountable for the backlog, and maximising the value that team delivers to the business. The product hat defines the product in customer-centric terms such as user stories, adds them to the product backlog, and prioritizes them based on importance and dependencies.

* A "team voice" a.k.a. "scrum master role". This role is accountable for removing impediments to the ability of the team to deliver the product goals and deliverables. The role is not a traditional team lead or project manager but acts as a buffer between the team and any distracting influences. The role has also been referred to as a team facilitator or servant-leader.

* A "delivery team" a.k.a. that does all tasks required to build the product increments (analysis, design, development, testing, documentation). The team is multi-disciplinary; the team is not just programmers.


## Disciplined agile delivery

https://en.wikipedia.org/wiki/Disciplined_agile_delivery

Key aspects:

* People-first

* Learning-oriented

* Hybrid

* Full delivery lifecycle

* Process goal driven

* Solution focused

* Risk-value lifecycle

* Enterprise aware

Primary roles:

* Stakeholder

* Product Owner

* Team Member

* Team Lead

* Architecture Owner

Secondary roles:

* Specialist

* Domain Expert

* Technical Expert

* Independent Tester

* Integrator


## Sprints

Calendar time sprint:

  * A "calendar time sprint" aims for given amount of time, such as one month, then tries to choose work that can fit into the time.

  * Example: A team decides to do a monthly sprint, then looks at all the potential work to do, and does a planning session to choose the work that is likely to fit into the time. 

Customer value sprint:

  * A "customer value sprint" aims for a business goal, such as delivering a new feature, and then gives options for scheduling time and resources.

  * Example: there is a customer cohort that will pay more when the product has a new feature. The team estimates the work, and then works on it.

Internal value sprint:

  * An "internal value sprint" aims for an infrastructure goal, such as refactoring, replatforming, or research.

  * Example: the team wants to change the code from using one kind of code to another kind, or from one hosting company to another, or from internally-built code to vendor-built code. The team estimates the work, and then works on it.


## Six thinking hats

https://en.wikipedia.org/wiki/Six_Thinking_Hats

The six thinking hats are described as a role and a hat color:

  * Managing = Blue. What is the subject? what are we thinking about? what is the goal? Can look at the big picture.
  * Information = White. Consider purely what information is available; what are the facts?
  * Emotions = Red. Intuitive or instinctive gut reactions or statements of emotional feeling (but not any justification).
  * Discernment = Black. Logic applied to identifying reasons to be cautious and conservative. Practical, realistic.
  * Optimistic response = Yellow. Logic applied to identifying benefits, seeking harmony. Sees the brighter, sunny side of situations.
  * Creativity = Green. Statements of provocation and investigation, seeing where a thought goes. Thinks creatively, outside the box.


## Infrastructure as Code (IaC)

https://en.wikipedia.org/wiki/Infrastructure_as_Code


## Technical debt vs. unhedged call option

Bad code isn’t Technical Debt, it’s an unhedged call

* By Steve Freeman
* Jul 23rd, 2010

This is all Chris Matts‘ idea. He realised that the problem with the “Technical Debt” metaphor is that for managers debt can be a good thing. Executives can be required to take on more debt because it makes the finances work better, it might even be encouraged by tax breaks. This is not the same debt as your personal credit card. Chris came up with a better metaphor, the Call Option.

I “write” a Call Option when I sell someone the right, but not the obligation, to buy in the future an agreed quantity of something at an price that is fixed now. So, for a payment now, I agree to sell you 10,000 chocolate santas1 at 56 pence each, at any time up to 10th December. You’re prepared to pay the premium because you want to know that you’ll have santas in your stores at a price you can sell.

From my side, if the price of the santas stays low, I get to keep your payment and I’m ahead. But, I also run the risk of having to provide these santas when the price has rocketed to 72 pence. I can protect myself by making arrangements with another party to acquire them at 56 pence or less, or by actually having them in stock. Or, I can take a chance and just collect the premium. This is called an unhedged, or “Naked”, Call. In the financial world this is risky because it has unlimited downside, I have to supply the santas whatever they cost me to provide.

Call options are a better model than debt for cruddy code (without tests) because they capture the unpredictability of what we do. If I slap in an a feature without cleaning up then I get the benefit immediately, I collect the premium. If I never see that code again, then I’m ahead and, in retrospect, it would have been foolish to have spent time cleaning it up.

On the other hand, if a radical new feature comes in that I have to do, all those quick fixes suddenly become very expensive to work with. Examples I’ve seen are a big new client that requires a port to a different platform, or a new regulatory requirement that needs a new report. I get equivalent problems if there’s a failure I have to interpret and fix just before a deadline, or the team members turn over completely and no-one remembers the tacit knowledge that helps the code make sense. The market has moved away from where I thought it was going to be and my option has been called.

Even if it is more expensive to do things cleanly (and I’m not convinced of that beyond a two-week horizon), it’s also less risky. A messy system is full of unhedged calls, each of which can cost an unpredictable amount should they ever be exercised. We’ve all seen what this can do in the financial markets, and the scary thing is that failure, if it comes, can be sudden—everything is fine until it isn’t. I’ve seen a few systems which are just too hard to change to keep up with the competition and the owners are in real trouble.

So that makes refactoring like buying an option too. I pay a premium now so that I have more choices about where I might take the code later. This is a mundane and obvious activity in many aspects of business—although not, it seems, software development. I don’t need to spend this money if I know exactly what will happen, if I have perfect knowledge of the relevant parts of the future, but I don’t recall when I last saw this happen.

So, the next time you have to deal with implausible delivery dates, don’t talk about Technical Debt. Debt is predictable and can be managed, it’s just another tool. Try talking about an Unhedged Call. Now all we need is a way to price Code Smells.


## Run Until Caught

https://github.com/run-until-caught/Run-Until-Caught-Development

<a href="https://github.com/run-until-caught/Run-Until-Caught-Development">Run Until Caught Development</a> is a set of principles for moving faster than large company processes normally would allow through strategic positioning of your work relative to burdensome internal processes.

There are six higher-order concepts within Run Until Caught development.

The first 4 concepts are part of the "run" part of "run until caught" development.

  * Believable Ignorance

  * Creatively Leverage Definitions

  * Defer Until Tomorrow

  * Piggyback Rides

The last two concepts are all about the "caught" part of "run until caught" development.


  * Cost Accounting (no not that one)

  * How to Respond to being 'caught'
