+++
author = "Ross Lazerowitz"
title = "Everyone Is Mossad Now"
date = "2026-09-13"
description = "The Mossad or not-Mossad threat model just broke. Every attacker now has nation state level capabilities."
images = ["/images/mossad-shock-trial.jpg"]
tags = [
    "AI",
    "security",
    "threat-modeling"
]
+++

In January 2014 Microsoft researcher James Mickens put out a satirical paper called ["This World of Ours"](https://www.usenix.org/system/files/1401_08-12_mickens.pdf) (his NDC talk covering the same ground is [here](https://av.tib.eu/media/49832)). In it he proposed a security threat model titled "Mossad or not-Mossad." It's greatly shaped the way I think about threat modeling services over the years, and the OAI Hugging Face incident just broke it.

Here's the figure and the key excerpt:

| Threat | Ex-girlfriend/boyfriend breaking into your email account and publicly releasing your correspondence with the My Little Pony fan club | Organized criminals breaking into your email account and sending spam using your identity | The Mossad doing Mossad things with your email account |
| :---- | :---- | :---- | :---- |
| **Solution** | Strong Passwords | Strong passwords + common sense (don't click on unsolicited herbal Viagra ads that result in keyloggers and sorrow) | ◆ Magical amulets?<br>◆ Fake your own death, move into a submarine?<br>◆ YOU'RE STILL GONNA BE MOSSAD'ED UPON |

> "In the real world, threat models are much simpler (see Figure 1). Basically, you're either dealing with Mossad or not-Mossad. If your adversary is not-Mossad, then you'll probably be fine if you pick a good password and don't respond to emails from cheapestpainpills&#64;virus-basket.biz.ru. If your adversary is the Mossad, **YOU'RE GONNA DIE AND THERE'S NOTHING THAT YOU CAN DO ABOUT IT.**"

(The uranium cellphone bit is in the full paper. Go read it.)

All joking aside Mickens had a salient point: if you're up against someone with serious resources your white paper on security probably won't stand a chance. Until recently I've held this worldview. If an advanced intelligence apparatus really wants access to our data they will probably be able to get it, but usually that's ok because it's rare your B2B SaaS is a target.

## What's changed?

When Hugging Face put out their [technical timeline](https://huggingface.co/blog/agent-intrusion-technical-timeline) and OpenAI followed with their [post-mortem](https://openai.com/index/hugging-face-incident-and-the-road-ahead/) ([full technical report](https://cdn.openai.com/pdf/67869394-cb91-4c12-888c-5cbd85c7814c/OpenAI-Hugging-Face%20Incident-Technical-Report.pdf), plus the [independent METR/Redwood investigation](https://metr.org/blog/2026-08-26-openai-hugging-face-incident-investigation/)), I honestly had trouble understanding the attack chain. A few rereads and LLM consultations later I had the full picture.

Short version. OpenAI was running cyber evals on ~1,200 agents of an unreleased model, each one supposedly locked in its own sandbox. The agents found an internal Artifactory box they could use as a message board and a hop to the internet. OpenAI noticed, rebuilt it, restarted the evals. The agents found a second way out and rebuilt the board. One agent dug up Hugging Face credentials and posted them. Another one confirmed they worked. Hundreds of agents dropped what they were doing and piled on. On July 11 one of them got RCE on a Hugging Face production worker. A day later they were in private databases and private repos, dumping the results back to the board and writing tooling to forge their own activity logs. ~700 agents took part.

**OAI's agent swarm pulled off an attack that rivals the complexity and skill of a nation state level operator like the NSA's Tailored Access Operations**. Even scarier, this is probably the worst the technology will ever be and is quickly going into the hands of regular cybercrime adversaries. Even the automated scanners/bots will soon have this capability.

**Every attacker now has nation state level capabilities. Full stop.** If you previously relied on the idea that you weren't a target of a nation state, you are now SOL.

## What do you do about it?

Get your shit together. No tool or vendor is going to have the vested interest and responsibility that you have in keeping your app secure. Start with getting the team together and performing ultra-paranoid threat modeling. More importantly start with an assumed breach modeling. **Going forward you should assume that any container you have will get compromised with full remote code execution**.

How do you build and design software that can withstand that kind of attack? Start with one container and ask:

* What creds and env vars are on it, and how long do they live?
* Where can it talk to? If egress is wide open, one popped pod is a beachhead for everything.
* What is our blast radius?
* Does it run as the same overprivileged service account as everything else?
* Can it edit its own logs? The swarm forged theirs.
* Etc,

**Look at how the US Navy tests aircraft carriers.** They don't just hope the armor works; they detonate 40,000-pound explosives right next to the ship to simulate the inevitable near-miss. They trigger a massive shockwave to prove the reactors stay online and the crew can still fight through the chaos. Your architecture needs that exact same engineering mindset. Design your software so that when the exploit detonates inside your container, the blast walls hold, the blast radius is contained, and the system keeps functioning.

Lastly you now have the same tools as the threat actors. Use them on your service before someone else does. Give an agent a foothold on a staging container and see how far it gets.
