---
title: "Cognitive Debt"
date: 2026-06-20
draft: true
summary: "On the quiet cost of letting AI do the thinking for you, and how to stay sharp while still shipping fast."
tags:
  - ai
  - learning
  - software-engineering
  - craft
---

I wanted to share some thoughts I’ve been mulling over for the last couple of months; in this new, daunting and exciting time of AI.

Right now; it’s far too easy to let AI do the thinking for you, write the code for you and fix things for you; while you skip the learning, the understanding and personal development. The bugs get fixed, but your mental model doesn’t move. The spec gets written; but your critical thinking skills don’t evolve. This will get worse over time. We are silently trading capabilities for present day speed. AI is honestly like a drug; and it’s in our nature to take the easy way out; let the AI do the hard part (thinking); I’m as guilty of this as anyone. The tools won’t force us to do otherwise; that part has to come from you.

As you are probably well aware, I’m a big proponent of AI; I have probably shipped more over the last 3 months than I did in all of 2025. But the default way of how we use these tools is optimized towards closing tasks. This is a problem.

Currently there is a default loop that most of us have settled into. You paste an exception, or a feature request into the CLI; the model hands you a fix; problem gone, feature implemented. You ship and somewhere along that loop the struggle between debugging, problem solving and implementation disappears. Cognitive surrender is real and is well documented online. I believe that will be the difference between okay engineers and great engineers moving forward. We are slowly offloading the verdict and cognitive load to AI. None of these moments feel like a problem today; but over time these interactions will make us mush by a thousand cuts.

There is a lot of studies that seem to all point to a similar conclusion as above (I highly recommend the read) e.g:

- [Your Brain on ChatGPT](https://www.media.mit.edu/publications/your-brain-on-chatgpt/): “LLM users consistently underperformed at neural, linguistic, and behavioral levels”
- [How AI assistance impacts the formation of coding skills](https://www.anthropic.com/research/AI-assistance-coding-skills) (Anthropic): “The largest gap in scores between the two groups (those that used AI and those that didn’t) was on debugging questions, suggesting that the ability to understand when code is incorrect and why it fails may be a particular area of concern if AI impedes coding development.”

Both studies are essentially saying: using AI without an intentionally learning along the way; degrades the skills we are being paid for as engineers.

In software engineering, complete autonomous delegation to Agents breaks down in a couple of ways:

When a novel and complicated specification is made: AI will output a solid; even amazing plan but AI will never save you from confusion. When you’re trying to output a strategy together, a plan, a specification; and you skip that “critical thinking step”, you will not be crystal clear on the execution or minutia. AI doesn’t have full context on the goal, problem and existing insights you may have gathered through experience; therefore the solution will be diluted and hollow. If you outsource any of that critical thinking to AI, you will find gaps during execution that will cause delays, outages and bugs. AI is amazing at solving “known” problems; the more novel the problem is (and we have a lot of novel challenges in the systems I work on), the worse the output will get. It’s these hard, undocumented problems that justify our salaries and require a deep understanding of the problem space.

When something breaks: generated code will crash the same way human code crashes. “Oops Copilot wrote that” doesn’t help you or the team debug the issue. Someone still needs to understand the architecture of the system. Someone needs to know why a websocket connection is dropped during an ice exchange and someone needs to know that an application gateway is at max compute and is causing timeouts downstream.

When our infrastructure breaks: our code base is ephemeral; our systems are permanent. When a security review flags a critical issue or when something breaks in our infra. You will struggle to prompt your way to a fix; you need a team that understands the system through and through to resolve an outage.

When it lies to you: I know it’s crazy; but AI can still be wrong; it can hallucinate and it can gas-light you. Our only defense here is through having enough expertise to spot the lie.

I know this is daunting; but there is light at the end of the tunnel: we just need to be intentional about it.

- Form a hypothesis before you start; don’t go in blind, even an educated guess is good.
- Explore the problem space with intentionality; having the model grill you with questions is amazing for this; it will force you to deeply think about every aspect of the issue at hand; relying on your guidance and expertise; before generating a plan.
- Ask for code after you’ve grasped the concepts and architecture. In unfamiliar territory, your first prompt should be “explore the architecture of this service and build a website to explain to me” (example) or “ explain to me how x works in detail?”
- Critique the generated output; push back on it and question it. Don’t LGTM; AI reviewed this already.
- Ask the model to teach you what it did after it does something clever or novel to you. Question it on the concepts it used and how it came to that design decision. All it takes is one extra prompt at the end of the session to completely change your takeaway from the session.

There is nothing radical here; just a couple of small steps you can take when using our everyday tooling.

Finish your days being able to say “I’ve learnt something today”; sometimes that may not be the case (that’s totally fine; you’re allowed to have lazy days and you’re allowed to have monotonous days). But if you see yourself answering the same, week after week; cognitive debt is building.

Again, this isn’t between choosing AI and learning; it’s about figuring out a workflow that allows for both.

If you’re still here; thanks for reading my shpiel; this isn’t my forte and it probably doesn’t read too easily. But I appreciate you regardless and hope you take something away from it.
