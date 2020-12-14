[<< back to main course website](index.html)

## Module 1: Running Agile at Scale

[Watch this module on LinkedIn Learning](https://www.linkedin.com/learning/lean-technology-strategy-running-agile-at-scale)

### Unit 1: The Problems with Agile at Scale

Unfortunately many organizations adopting agile methods end up with a paradigm we call "water-scrum-fall". In this popular pseudo-agile paradigm development teams work iteratively and incrementally, but it still takes months for work to get into the hands of development teams, and once work is "dev complete" it gets batched up into infrequent releases which must go through integration and testing. The overall lead time through this entire workflow is usually measured in many months, even years.

One of the problems with this paradigm is that it takes so long to get feedback. As a result, investment decisions are usually made through the "HiPPO method" (the "HIghly Paid Person's Opinion") rather than through economic modeling. Typically, much of the work that gets put into the investment decision is in the form of estimating costs. But as Douglas Hubbard, author of _How to Measure Anything_, [points out](https://www.cio.com/article/2438748/it-organization/the-it-measurement-inversion.html), "Even in projects with very uncertain development costs, we haven't found that those costs have a significant information value for the investment decision... The single most important unknown is whether the project will be canceled... The next most important variable is utilization of the system, including how quickly the system rolls out and whether some people will use it at all."

Another problem is that in this paradigm we batch up work into projects, which combine high-value work with low-value work and deliver it in large batches. In [research that was done](http://blackswanfarming.com/black-swan-farming-using-cost-of-delay/) at Maersk by Joshua J Arnold and Özlem Yüce, it was discovered that among the thousands of pieces of work sitting in the development backlog were three items which were each individually costing Maersk over $1m per week because they had not been delivered.

To summarize, the water-scrum-fall paradigm has the following critical problems:

* Focus on managing cost instead of creating value;
* Investment decisions are not made using economic models;
* Work is batched up into projects: no effective prioritization;
* Feedback loops are too slow: early decisions locked in;
* We waste the creative power of our people.

### Unit 2: Principles of High Performance Program Management

In this unit I present five principles at the heart of high-performance program management:

* Collaborate to set measurable outcomes at the program level
* Teams work to design and test hypotheses
* Create fast feedback loops
* Work in small batches
* Create a culture of experimentation

Many programs begin with detailed analysis: we create epics, then break them down into large features, and then break these down into stories and tasks. Instead, we should begin by agreeing on the organizational, customer and user *outcomes* we wish to achieve, expressed in measurable terms. Then we have teams experiment with ways to achieve these outcomes, designing experiments and prototypes, testing them with real customers and users, and iterating based on what they learn.

I discuss various tools that can help with this approach:

* [Impact mapping](https://www.impactmapping.org/), a collaborative exercise in which teams take an outcome, discuss the stakeholders involved and the ways that can help or hinder achieving the outcome, and then come up with deliverables which we think can achieve the outcome. Then the team agrees on the deliverable(s) which will achieve the outcome with the least work, and designs an experiment to test this hypothesis.
* [Hypothesis-driven delivery](https://www.thoughtworks.com/insights/blog/how-implement-hypothesis-driven-development), in which we express work in terms of the outcome, the people involved, and the work that will achieve this outcome.
* Running experiments using [methods from user research](https://www.usability.gov/what-and-why/user-research.html) in order to test hypotheses.

In order to work in a hypothesis-driven way, it's valuable to be able to push working experiments into production frequently and reliably. This capability is called [continuous delivery](https://continuousdelivery.com/), and can be implemented in all kinds of organizations of all sizes, even regulated ones. It allows us to work in small batches, which in turn means we can get feedback on our ideas more quickly. Amazon spent four years [re-architecting their technology stack](https://gist.github.com/jezhumble/a8b3cbb4ea20139582fa8ffc9d791fb2), which enables them to release changes to production [thousands of times per day](https://www.youtube.com/watch?v=dxk8b9rSKOo). This, in turn, enables their [culture of experimentation](https://glinden.blogspot.com/2006/04/early-amazon-shopping-cart.html).

#### Unit 2 Exercises

* Think of one of the organizational, customer, or user outcomes you're trying to achieve with your product. Take a small, cross-functional group from your organization and build an impact map.
* Using your impact map, create one or two hypotheses using the hypothesis-driven development template. Design an experiment to test your experiment which gathers data from real people without writing a single line of code.
* How easy is it to deploy a change into production at your organization? Do people have to ask permission first? How long does it take? How often do you do this? Is it even possible for someone to put an experiment or a high priority change into production without going through the whole software delivery lifecycle? What could you do to make things better?

### Unit 3: Case Study: HP FutureSmart Firmware

In this unit I present a case study which shows how the ideas presented in the rest of this unit can be implemented in practice.

HP’s LaserJet Firmware division builds the firmware that runs all their scanners, printers, and multifunction devices. The team consists of 400 people distributed across the USA, Brazil, and India. In 2008, the division had a problem: they were moving too slowly. They had been on the critical path for all new product releases for years, and were unable to deliver new features: "Marketing would come to us with a million ideas that would dazzle the customer, and we’d just tell them, 'Out of your list, pick the two things you’d like to get in the next 6–12 months.'" They had tried spending, hiring, and outsourcing their way out of the problem, but nothing had worked. They needed a fresh approach.

The targets set by the HP LaserJet leadership were to improve developer productivity by a factor of 10, so as to get firmware off the critical path for product development and reduce costs. They had three high-level goals:

* Create a single platform to support all devices
* Increase quality and reduce the amount of stabilization required prior to release
* Reduce the amount of time spent on planning

A key element in achieving these goals was implementing continuous delivery, with a particular focus on:

* The practice of [continuous integration](https://continuousdelivery.com/foundations/configuration-management/)
* Significant investment in [test automation](https://continuousdelivery.com/foundations/test-automation/)
* Creating a hardware simulator so that tests could be run on a virtual platform
* Reproduction of test failures on developer workstations

After three years of work, the HP LaserJet Firmware division changed the economics of the software delivery process by adopting continuous delivery, comprehensive test automation, an iterative and adaptive approach to program management, and a more agile planning process.

_Economic Benefits of HP FutureSmart’s Agile Transformation_

* Overall development costs were reduced by ~40%.
* Programs under development increased by ~140%.
* Development costs per program went down 78%.
* Resources driving innovation increased eightfold.

The most important point to remember from this case study is that the enormous cost savings and improvements in productivity were only possible on the basis of a large and ongoing _investment_ made by the team in test automation and continuous integration. Even today, many people think that Lean is a management-led activity and that it’s about simply cutting costs. In reality, it requires _investing_ to remove waste and reduce failure demand—it is a worker-led activity that, ultimately, can continuously drive down costs and improve quality and productivity.

### Unit 4: Continuous Improvement

In this unit I discuss how the HP FutureSmart team implemented their transformation, and present the [Improvement Kata framework](http://www-personal.umich.edu/~mrother/The_Improvement_Kata.html) that provides a general problem-solving approach that can be used to implement continuous improvement.

You can find more on the FutureSmart program in the following books co-authored by Gary Gruver:

* _A Practical Approach to Large-Scale Agile Development: How HP Transformed LaserJet FutureSmart Firmware_, by Gary Gruver, Mike Young, and Pat Fulghum.
* _Leading the Transformation: Applying Agile and DevOps Principles at Scale_, by Gary Gruver and Tommy Mouser.

In addition to the [Improvement Kata resources] available for free on Mike Rother's Website, you can also read _Toyota Kata: Managing People for Improvement, Adaptiveness and Superior Results_ by Mike Rother.

### Unit 5: Conclusion

In this unit we review the principles we presented at the beginning of this module:

1. Collaborate to set measurable outcomes at the program level
2. Teams work to design and test hypotheses
3. Create fast feedback loops
4. Work in small batches
5. Create a culture of experimentation

[<< back to main course website](index.html)
