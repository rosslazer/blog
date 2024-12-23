+++
author = "Ross Lazerowitz"
title = "Personal AI"
date = "2024-12-23"
description = "It’s hard to take claims of AGI seriously when it can’t even order a pizza.”"
images = ["/images/personal-ai.png"]
tags = [
    "AI",
    "ideas"]
+++

# The Case for Personal AI

It’s been an inspiring last few weeks for AI models. The major labs have released huge advancements in video generation and reasoning models. OpenAI’s o3 model scored a record high of **75.7%** on the Abstraction and Reasoning Corpus (ARC), a series of brain twisters that are easy for humans but hard for AI. While these are significant developments, they are abstract to the average person. I would love to see more **personal AI**, that is, AI for the average person, not accelerators for researchers, engineers, and marketers.

What’s missing is AI designed to enhance everyday life—what I’d call **‘Personal AI.’** Personal AI should bring the same level of convenience to daily life as the automobile, dishwasher, microwave, or washing machine. Here are some examples of things that personal AI should be able to do:
- **Order me a pizza**  
- **Book a reservation** based on a query like:  
  _“Italian restaurant that serves cacio pepe and has availability for four people.”_  
- **Help me stay healthy**  
- **Coordinate multi-step travel logistics**  
- **Stay in touch with friends and family**  
- **Track and order groceries** and pair them with meal plans  
- **Guide me with housework**  

In short, it helps with **everyday tasks.** Here’s an example of that long tail from the [U.S. Census American Time Use Survey](https://www.bls.gov/charts/american-time-use/activity-by-sex.htm).  
![American Time Use Survey](/images/average-hours-per-day-sp.png)

## Why Don’t We Have It Yet?

Each of the tasks above is deceptively hard. Let’s take the simplest example: **ordering a pizza.** Imagine you ask an AI to order you a pizza. Here’s a small example of the plan it would need to follow (assuming no saved memory):  

1. **Location**: Where are you?  
2. **Delivery Services**: Which ones do you use? Payment preferences?  
3. **Pizza Type**: What kind of pizza do you want?  
4. **Restaurant Selection**: Based on ratings or your preferences.  
5. **Gratuity**: How much are you tipping?  
6. **Price Sensitivity**: What’s your budget?  
7. **Wait Time**: How long can you tolerate waiting?  
8. **Address Details**: Delivery instructions (e.g., doorman, gate, etc.).  

Furthermore, this plan is not linear. Some of the answers to these questions might loop. For example, you may want a type of pizza that is only provided by a restaurant outside of some of your criteria. Does it ask you to relax the criteria or give you another option? A good personal assistant would fill in the gaps, only ask the necessary questions, and learn quickly. I haven’t seen AI perform these heavy question-based human-in-the-loop tasks well yet. I speculate that we don’t have a ton of training data on these tasks yet. 

Even if we solve the core LLM flow, we still need to solve payment, integration to delivery services, and even outbound/inbound calling. Heck, it’s even possible that ordering a pizza is harder than solving graduate-level math problems. Math, in the end, is a system with no ambiguity. The list above is much fuzzier than any proof.

## What I’d Like To See

AI is very powerful but unapproachable to the average person. In lieu of seeing applications in their daily life, the rhetoric about it taking jobs wins. I’d love to see more companies and projects that try to use AI to make everyday life smoother. AI for the rest of us, not just the doctors, engineers, and researchers.