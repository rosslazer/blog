+++
author = "Ross Lazerowitz"
title = "It Was Never About the Code"
date = "2026-07-27"
description = "AI isn't ending software companies, because building products was never about the code in the first place."
images = ["/images/never-about-the-code.png"]
tags = [
    "AI",
    "startup-life"
]
+++

There's been a lot of discourse lately about the end of software. Comically named the "SaaSpocalypse" in reference to the meltdown of SaaS stock valuations in the public markets. Investor reactions have been stark, leading some to stop backing software companies at all. This meme is flawed because building products was never about the code in the first place. Nothing has fundamentally changed about building, marketing, and selling software.

Let us consider for a moment that AI will replace all software. Where is a technology investor to park their cash?

**Frontier Labs** - Great idea but these labs are leapfrogging each other every few months with open source not far behind. There appears to be no durable moat here other than having the compute to serve these models, at least in the short term. Imagine if companies were switching between Salesforce and Hubspot every few months. Not practical.

**Inference Providers** - Another cool idea but these workloads are stateless and thus not sticky. They are dependent largely on good open source LLMs that can be run anywhere. You can't switch between public clouds like AWS and GCP so easily, but you can use the same model on the same GPU anywhere you want.

**AI-enabled services** - Using AI to transform services industries is a neat idea. However these are largely relationship/reputation driven companies at the top end of the market. Whatever AI advantage you build should be instantly copyable if you believe AI can rewrite software and compress margins.

It seems to me that if you believe in the AI eating all of SaaS and eroding moats argument, then logically all of the other trendy companies above will suffer the same fate. Good thing that argument is bullshit.

## It was never about the code

Why do companies buy software? They buy it because they want a solution to their problem. ServiceNow is successful because they could help you implement IT Service Management and that was how you ran an IT department. These companies aren't just buying software they are buying into a partner, an ecosystem, common skillset, and vision. To get to that point they went through a journey of evaluating the market, likely a proof of concept, pricing negotiations. Think about all of the touchpoints here: does AI eliminate the marketing that went into that ServiceNow deal? What about the skills of the sales people who navigated the organization, structured the deal, and ran a successful pilot? What about the engineers and product managers that researched the customers' needs and ensured they delivered a solution that met the quality bar of the customer?

If you believe that AI will magically solve all of those problems above, I'm not sure I can help you. You believe in a world where the AI is walking around in the physical world and attending meetings where 10 people are fighting over how many values are in the "resolution" field dropdown. Or one where the entire economy is automated and humans live in a Star Trek-like existence.

I'm not saying that our roles won't get refined, as they have through every transition, I'm simply saying that there's a lot more that goes into building a software product than the 1s and 0s. I'm also not saying that there won't be casualties. There is a lot of really simple software out there that was likely to fall victim to the forces of consolidation regardless.

## Building in-house

Some argue that the disruption won't come from the sinister frontier labs, but from the customers themselves. They will use their newfound agentic coding powers to replace expensive vendor software. This isn't a new concept, in the olden days companies used to build their own CRMs and even customer OSes for mainframes. Software was valued so little it used to come for free with the hardware. What changed? Software got very complex as it got distributed and did a lot more than adding/subtracting bank account balances. Running and maintaining this software became burdensome and fell behind what was commercially available. The commercial products came up with abstractions like [Salesforce's Apex](https://developer.salesforce.com/docs/atlas.en-us.apexcode.meta/apexcode/apex_intro.htm) that made them infinitely extensible while staying supported.

While technology companies that employ lots of software engineers may go on to replace products like Salesforce, the majority will not. Even the people best equipped to build their own software don't want to:

{{< x user="shadcn" id="2061129752308514932" cards="hidden" >}}

If the guy whose components half the frontend industry ships doesn't want to build and maintain his own tools, your VP of IT definitely doesn't. And when a team does pull it off, the story tends to end the same way. One startup vibe-coded their own JIRA that the whole company adopted, until the maintenance bill came due:

{{< x user="thericebowlgirl" id="2081575149334335552" >}}

Large enterprise software companies have the benefit of seeing requirements and usage at a large swathe of customers, and are better suited to produce the software that solves the problem. I think enterprises would rather spend their coveted engineering and AI resources on software that makes their business better. By its very definition software platforms are generic, it's not the thing that makes you unique. What makes your company unique is exactly what makes it valuable, and that's where you'd be better off spending your time.

## Margin Compression

The final argument I hear is one about margin compression. AI is going to clone all of this software and increase competition. Consider this thought experiment: the year is 2020, there is no vibe coding. Someone hands a billion dollars to a startup to copy every single feature of Salesforce end to end and then goes to market. Do they take any market share away from Salesforce? The answer is no. Salesforce has survived many attempts on its life through endeavors like that and won every time. Because it's not just about the bits, people trust Salesforce as a company to solve a real problem for them. While the license may seem expensive to a software engineer, it's actually pennies for the value most organizations see.

## The more things change, the more they stay the same

So, what does change in this new world? We keep moving up the stack, as technology always has. Every engineer is now a manager, the human in the loop, and just as we had bad managers of coders before, we will have bad managers of agents. The bigger shift is quality. Now that building software is cheap, the market floods with adequate options, and the products that survive will be the ones that earn trust through craft. Yet quality is currently a casualty of AI. Fewer people than ever are talking about what it means to build good software. Karri Saarinen, whose company won the most commoditized category in software by obsessing over exactly this, asked the only question that matters:

{{< x user="karrisaarinen" id="2054254445018710248" >}}
