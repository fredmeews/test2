---
layout: post
title: Explore, Expand, Extract
---

<img src="/images/3x.png" alt="3x" width="500"/>

In the software world, [Kent Beck](https://twitter.com/KentBeck) is an interesting guy to watch. He has a long history of taking simple ideas and combining them in ways that are fresh and highly practical for development teams. When Kent joined Facebook in 2011, he was appalled to observe that most teams were not using agile methods. In fact, much of what they were doing was more akin to waterfall processes from days of yore. 

As he describes in a series of talks, he moved from thinking “wow - I have a lot to teach these guys” to the realization that the team were tackling big problems of scale and stability - less important was the experimentation which characterized much of his career up to that point.  Kent began to wonder if the processes the teams were using were in fact better suited to their specific challenges and constraints.  His attempts to understand why that might be the case resulted in a model called Explore, Expand & Extract or “3X” for short.

3X was inspired by a pair of financial investment concepts…

**Convex payouts** start with a small investment. Most times, you will lose the entire investment. Occasionally though, there is a big payoff... 

![convex payout](/images/3x_convex.png)

**Concave payouts** require a large investment, but have a stable, predictable return. 

![concave payout](/images/3x_concave.png)

Bringing the curves together helps describe the lifecycle of a “typical” software project: it starts out with market Exploration, followed by a spurt of significant Expansion and finally a stabilization period where a reliable source of revenue can be Extracted from it. 

Let’s look at the characteristics of each phase…

### Explore

![explore](/images/3x_explore.png)

During Explore, no idea is a bad one. Failure is expected and is indeed encouraged because we simply don’t know what’s going to connect in the market. There’s a timer on this phase - after which the money (and market patience) will run out. Until that happens though, the primary goal is to run as many experiments as possible and quickly adapting from the feedback.

If you’re working in Silicon Valley, this probably sounds familiar. You might spend your entire career jumping between companies in this phase. 

It’s important for the team and leadership to agree on when you’re in Explore mode.  I recall one project where our team was overconfident in our belief that we’d hit on the killer app.  We stopped exploring too soon, focusing instead on Expansion concerns like massive scalability.  Turns out what we were building wasn’t what the market wanted though - i.e. the project would have benefitted from a lot more experimentation driven by customer feedback.

### Expand

![expand](/images/3x_expand.png)

You don’t get to decide when you transition from Explore to Expand - the market tells you that you have a winner and it’s off to the races! Your meager Exploration budget grows but so do performance issues. Scalable software and hardware architecture takes center stage.

Expansion is arguably the most exhilarating phase and also the most profitable.  Likely you'll experience this phase only a handful of times during your career.  As an example, I worked on a project to expand the use of a low-volume screening system to every international airport.  The scalability requirements were daunting, and the release date was congressionally mandated - i.e. unmovable.

In this situation, we had the luxury of the all the best hardware, consultants and pizza… everything except time.  We delivered on time, but not without a cost… for 6 months we saw each other more often than or families.  Although that project more a decade ago, I am still friends with those guys.  We went through the software project equivalent of a war together.

### Extract

![extract](/images/3x_extract.png)

At some point, the “war” that is expansion ends and is followed by a period of relative stability.  Feature-wise, we look for things that will give a modest increase in ROI without destabilizing the core.  Operationally, the focus is on matruing code & procedures to avoid any serious failures. 

Sound boring?  Fear not - there is plenty of room for Exploration within Extract.  However when it comes to experimentation, you’ll often find the tolerance for failure and investment budget will not be the same.  Alternatively, you can build on your loyal customer base to produce spin-off products and kickstart a new cycle!

### What phase are we in?

When team members make individual assumptions about the project's current phase, it's akin to a sports team showing up to the field and half the players are expecting a soccer game, the others football.  Someone's gonna get hurt.


| In...   | the main idea is...                 | where we value... | over...         |
|---------|-------------------------------------|-------------------|-----------------|
| Explore | Experiment, Feedbqack, Fail, Repeat | Experimentation   | Architecture    |
| Expand  | Run run run!                        | Scale             | Funcationality  |
| Extract | Safety first                        | Reliability       | Experimentation |


As the table shows, phase essentially determines what the team values.  This of course impacts all aspects of your project... from prioritization, to budget to hiring.

So how does a team go about determining which phase they're in?  At what point does the phase change?  Unfortunately, there are no generic rules that will apply to all proejcts.  However, I believe you'll find that 3X is a useful concept for productive, ongoing conversations as your project evolves.
