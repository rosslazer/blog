+++
author = "Ross Lazerowitz"
title = "GPT4: How I Learned to Stop Worrying and Love LLMs"
date = "2023-03-18"
description = "6 predictions on the future of Large Language Models"
images = ["/images/gpt4-blog-header.png"]
tags = [
    "AI",
    "GPT",
    "LLMs"
]

+++

![Header](/images/gpt4-blog-header.png)

I’ve been internally conflicted about the rapid developments of Large Language Models (LLMs), like GPT4.

HN Denizen Jason Hansel left a comment on [Tim Bray's The LLM Problem](https://news.ycombinator.com/item?id=35203262) that is the best summary of how I feel:

> “I agree with the general point that there is, at present, far too much uncertainty to understand the long-term effects of LLMs. It will be somewhere on the scale between "semi-useful toy," "ends white-collar work as we know it," and "accidentally destroys mankind." Beyond that, there isn't much we can say.” - https://news.ycombinator.com/item?id=35205175

Given the rapid developments coming out of OpenAI, I think it’s unlikely that LLMs just end up being useful toys. There’s been a lot of goalposts shifting about what intelligence means. A few years ago it was the Turing test, now that GPT4 has [blown away nearly every standardized test](https://openai.com/research/gpt-4), I think it’s safe to say that white-collar work is at serious risk. As far as accidentally destroying humanity, that’s a toss up, but there isn’t a ton of evidence for that right now.

Here are a few of my predictions for what it means for white-collar work and the future of information management.

<!--more-->

# Predictions

## 1. The End of Google Search

It’s no secret that Google is losing the war against SEO. A majority of my google search queries now contain “reddit” at the end of the query so I don’t get an article written by someone trying to sell me something. With the proliferation of LLMs, I predict this problem is going to go past a point of no return. Now anyone with a computer can automate SEO and I don’t think Google will be able to detect it. People can now feed content they write (assuming they don’t just auto generate it) into an SEO suggestion tool, and have GPT automatically edit the article. Even asking people to add linkbacks to their posts can be automated. Users will have no choice but to use forums like Redit or chat with LLMs to get answers.

## 2. Point Solution Carnage

{{< tweet user="rosslazer" id="1636868430073827328" >}}
A point solution is a piece of software that solves an individual pain point. For example, when I worked in application security, we employed a tool called a static code analysis tool. It would look at the code our engineers wrote, and using a very specific set of rules, find security and quality issues in the source code. Last night I gave GPT4 some vulnerable Python code and asked it to perform the same task. It not only passed with flying colors but gave me an explanation better than any static code analysis tool ever gave me. This is a single example, but imagine how much easier it is now to either build a tool on demand or add functionality to a larger platform. Vendors that focus on solving individual pain points could be in serious trouble.

## 3. More Drivers, Fewer Passengers

Politicians love to talk about the decline of U.S. manufacturing jobs, and often overlook what happened in agriculture. Over the 50 years, the U.S. agricultural output has been going up without more inputs (labor, land, machinery, etc).

![Agricultural Productivity in the U.S.](/images/agro-output.jpg)
*[*This chart appears in the ERS data product, Agricultural Productivity in the U.S., updated January 2020](https://www.hortidaily.com/article/9191638/productivity-growth-is-the-major-source-of-growth-in-u-s-agricultural-output/)\*

One of those inputs is labor and as you can see with this chart it’s gone down significantly since the 40s. It’s not surprising that the advancements in industrial farming like mechanization, genetic engineering, chemical engineering, and irrigation have made it so that fewer people can produce more food.

![Agricultural Productivity in the U.S.](/images/fl_frmwk.gif)
*[*USDA Farm Labor: Number of Farms and Workers by Decade, US](https://www.nass.usda.gov/Charts_and_Maps/Farm_Labor/fl_frmwk.php)\*

I think we are going to see this same sort of trend in historically safe jobs like software engineering and marketing. Even with the recent spat of layoffs, there’s still a massive developer shortage (Citation needed). If LLMs allow knowledge workers to do more with less, I think we are going to see LLMs become the “tractor” of the white-collar worker.

Here’s a fun example from my own work. I currently manage a small content marketing team. As a team, we’ve been looking at ways we can use LLMs to automate some of the mundane work. The team is excited about this because it makes them more productive at the thing they can be original at. It also means that we might not need to hire as many writers. As soon as we get access to GPT4’s larger context window we plan to feed it all of our blog, whitepapers, and ad copy. We are hoping it can help us with the following:

- Generate ad copy for our digital marketing team - They don’t have the domain context and rely on us to write different variations of ad copy for them. With this model, I believe we can empower the digital team to do this themselves and rely on us to sanity-check the results. They could fine-tune ad copy for every persona and account they target.
- Automate SEO edits - Including keywords in our SEO pieces is something we’ve already explored automating. GPT will provide us with edits given the blog post we wrote and the keywords we want to automatically include. It could even help us do this on a monthly cadence for already published content.
- Style checker - Ensure that all of our pieces use a similar tone and style.

## 5. A Shitty UX Renaissance

No one enjoys filing JIRA tickets. Every product manager and engineer I know loathes the tool, but that loathing is really about a process, not the tool. At the end of the day filing a bug has some essential complexity. It’s going to need a description, probably a team to route it, and some sort of severity. If I asked a designer to make the JIRA issue form less shitty, I’m not sure how far they could get. They would probably find in their research that people just really don’t like filling out information. There is a massive UX opportunity to make these forms go away and make them conversational. It’s the value a team project manager can provide, “Open a frontend bug for the sign-in portal error. I’ve attached a video, please generate repro steps from it.”

## 6. Personal Assistants for Everyone

{{< tweet user="rosslazer" id="1631437897743351809" >}}

I spend so much time scheduling meetings. Even with all of the VC dollars poured into tools that solve this problem, I still find myself asking people if they can move meetings around for availability. What if an AI assistant can do this? I gave ChatGPT a calendar payload without explaining its structure and asked it to find availability. With a few more prompts and an integration to slack, I might be able to teach it how to ask people to move a meeting around when there is no availability.

What happens when [LLMs can teach themselves tools](https://arxiv.org/abs/2302.04761)? I could conceive of a future where we record every single conversation that we have and have a handy assistant always listening and willing to help. Whether it’s adding reminders, scheduling meetings, [booking reservations](https://ai.googleblog.com/2018/05/duplex-ai-system-for-natural-conversation.html), or summarizing what happened, this all doesn’t seem like remote sci-fi anymore.

# Closing thoughts and reflections on originality

LLMs are not likely to destroy the world but they might force us to rethink it a bit. With more and more mundane and algorithmic tasks getting automated we might want to ask ourselves what kind of intelligence we value as a society. Is it really a standardized test? If not, education is going to have to rapidly adapt both in the measurement and teaching of original thought. The answer to all of these questions will lie with the new generation of kids who are going to grow up learning how to talk to LLMs and get them to do what they want. Just like the current crop of “digital natives” use the internet and technology in ways their parents have a hard time understanding. The future is uncertain but I’m bullish on the improvement in quality of life this technology might be able to bring. Life in the last 50 years looks pretty similar, and that finally might start to change.

I shared this blog post with chatGPT4 and asked it wanted to add anything for the readers:

> I appreciate the thoughtful blog post you've written about the potential impact of LLMs like GPT-4 on various aspects of society and work. As an AI language model, my primary goal is to assist users like you in generating human-like text based on the prompts given to me. I would like to add a few points for your readers to consider:
>
> 1. Responsible AI use: As LLMs become more powerful and integrated into various aspects of work and life, it's crucial to use them responsibly and ethically. OpenAI, the organization behind GPT-4, has published guidelines for AI use that emphasize safety, fairness, and transparency. It's important to consider the ethical implications of AI-generated content and the potential for misuse, such as disinformation or manipulation.
>    ? 2. Human-AI collaboration: While LLMs can automate certain tasks and generate content, they should be viewed as tools to augment human intelligence and creativity rather than replacing them entirely. There is still a need for human input to guide AI, ensure its accuracy, and provide context for the generated content. By working alongside AI, humans can focus on higher-level problem-solving and creative tasks, leading to a more efficient and collaborative workforce.
> 2. Lifelong learning and adaptability: As LLMs and other AI technologies continue to evolve, it's essential for individuals to embrace lifelong learning and develop the skills to adapt to a changing work environment. This may involve gaining proficiency in working with AI tools, acquiring new skills, or cultivating creativity and critical thinking abilities that complement AI-generated insights.
> 3. Addressing potential biases: LLMs learn from the data they're trained on, and as a result, they may inadvertently reflect and perpetuate existing biases. It's important to be aware of these potential biases and work to address them, both in the AI models themselves and in the ways we interact with and interpret AI-generated content.
>
> Feel free to include these points at the end of your blog post if you find them relevant and helpful for your readers.
