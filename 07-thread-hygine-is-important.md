# three tips that will save your sanity (and your tokens) 

I'm sure that you probably already do some version of these things. Maybe even unknowingly as to why. You edit messages when Claude misses the mark. You front-load context when you want something ultra specific. You start fresh chats when Claude starts to lag.

But have you thought about why those things work? 🤔

Understanding the mechanics behind these habits makes you better at knowing when to use them, how hard to lean into them, and what you're actually trying to optimize. These aren't just standard workflow tips. They're ways of working *with* how Claude processes information instead of fighting against it.

## be specific upfront 🎯

Tell Claude what you want before it starts. Format, tone, length, audience, all of it.

This feels obvious until you watch someone spend six back-and-forth messages trying to get Claude to write something in the right voice but something keeps feeling.. off. They ask for a email response, get something too formal. Ask for something more casual, get something too loose. Ask for professional but approachable, finally land somewhere close.. well kinda. Close enough, I guess?

That's not Claude being difficult. That's Claude working with incomplete information and you iterating toward a spec you are going to wish you had written upfront. (ASK ME HOW I KNOW)

*Every response Claude gives you is based on everything it knows about what you want in that moment.* In that specific prompt. If you don't tell it the tone, it makes its best guess. If you don't specify the length, it defaults to something. If you don't mention the audience, it just picks one.

And those defaults.. don't usually get it right the first try. The issue is Claude doesn't know it's wrong until you tell it. And every correction you make is eating up tokens to fix a problem you could have prevented by being specific earlier.

OK ok, we get it Olivia, be specific.. *eye roll*

Here's what this has looked like in practice for me:

| Prompt Type | Example | What You Get |
|-------------|---------|--------------|
| **🔴 Vague** | Give me a summary of this meeting. | Generic fluff that sounds like a meeting happened |
| **🟢 Specific** | Write a minimum 2-paragraph summary of the AI Adoption and Progress Overview meeting for the company stakeholders who weren't in attendance but were invited. Focus on decisions made and next steps. Professional tone but not formal. Do not add fluff. Keep the brief to the point. Deliverables are being read by both highly technical staff and non-technical staff. | Actionable information people actually need |

**The vague prompt gets you something like:**

> The AI Adoption and Progress Overview meeting covered several key topics. The team discussed current implementation status and reviewed progress on various initiatives. Several decisions were made regarding next steps, and action items were assigned to team members. Overall, the meeting was productive and covered important ground for the project.

**The specific prompt gets you:**

> **AI Adoption and Progress Overview - Stakeholder Brief**
>
> **Key Decisions:** The leadership team approved moving forward with the pilot program in Q2, allocated $150K for initial implementation, and designated Sarah Chen as the technical lead. The compliance review timeline was extended to 6 weeks to accommodate federal requirements.
>
> **Next Steps:** Technical team will complete security assessment by March 15th, Sarah will present vendor recommendations at the next board meeting, and all department heads need to submit resource allocation requests by month-end.

See the difference? The first one sounds like a meeting happened. The second one tells you what actually came out of it.

I'm sure most of us could take that first prompt, keep talking with Claude and eventually pull out the info we need. A little prompt engineering never hurt no one, right? 🤷‍♀️

And while that's all fine and true, who wants to spend more time on something than they have to? Who want to go back and fourth trying to explain to Claude "no I meant this, not that", "This is for clients, not internal, please remove internal acronyms", "Stop drawing on the wall".. wait am I talking to Claude or my child now? Either way, understanding how they think will save you a lot of frustration.

This happens because of how Claude processes context. When you give it a vague prompt, it has to guess at what level of detail you want, what format works for your use case, who's going to read this thing based only on the context it has. It *should* default to safe, generic, covers-the-bases language because it doesn't want to get it wrong, so the better option is getting it half right.

When you're specific upfront, you're not just telling Claude what to write. You're telling it how to prioritize information, what to emphasize, what to skip. The detailed prompt above isn't longer because I like yapping (caught me, I do) it's longer because each piece of context helps Claude make better choices about what matters.

💡 **The extra upfront work isn't overhead. It's investment!!!** You spend 30 seconds being specific from the jump, build a strong brief and spec and can save yourself three rounds of "actually, can you make this more..." corrections. Or the alternative of working on a build for 3 hours and abandoning it because at this point, you've spent more time trying to save you time than you would have saved just manually doing the thing (Remember that stat of 90% of AI projects fail..?) And your final result is better because Claude had clear direction from the start instead of trying to reverse-engineer/prompt-engineer/mumbo-jumbo your intent from feedback.

## edit, don't follow up ✏️

When Claude misses the mark (and it will), try editing your original message and regenerate instead of sending a follow-up.

This one feels counterintuitive if you're used to the conversation flowing forward. But Claude isn't having a conversation with you in the way humans do. It's processing the entire context window every time, and everything in that window influences what it writes.

When you send a follow-up correction, you're not just telling Claude what to fix. You're adding that correction to the context it has to process for every subsequent response. Your thread gets longer, your context gets messier, and Claude has to work through more information to get to the part that matters to you.

Editing and regenerating gives you a clean do-over. Same context leading up to your request, but now with better instructions. Claude doesn't have to parse through the failed attempt and your correction notes to figure out what you actually wanted.

🎯 **This isn't just about keeping things tidy. It's about giving Claude the cleanest possible signal about what you want.**

**When to break this rule:** 

The follow-up correction is actually adding new information, not just clarifying what you meant originally. If Claude wrote exactly what you asked for but you realized you asked for the wrong thing and now you want to add on to that build, a follow-up makes sense. But if Claude totally missed your intent, edit and try again.

## ask Claude to write you a fresh start prompt 

When a thread feels heavy, ask Claude to summarize the conversation into a prompt you can drop into a new chat.

This is my nuclear option for context management, and it works because it forces you to be explicit about what actually matters from your conversation.

Claude doesn't "remember things" between chats, so when you ask it to write a fresh start prompt, it has to identify the essential information someone would need to pick up the conversation where you left off. Not the full conversation history. Not every tangent and false start. Just the core context and current status.

That process of distillation often reveals how much of your thread was actually noise. The rambling exploration phase that helped you figure out what you actually wanted. Because lets be honest, the product you envision in your head the first go round is almost never the finished product. It's better. 😉 The dead ends you tried before finding the right direction fall away. The clarifications that were necessary in the moment but aren't needed going forward don't take up context space anymore.

💾 **A fresh start prompt is like a save state for your conversation. It captures where you are without dragging along how you got there.**

And honestly, sometimes the exercise of asking for a fresh start prompt is more valuable than actually using it. It makes you think about what you're trying to accomplish, whether you're still on track, or if there's other area's to explore before you sit down to build.

**the thread health check nobody asked for but everyone needs 📊**

| Thread State | Vibe Check | Action |
|-------------|------------|---------|
| 15+ back and forths with Claude | 🔴 Time for intervention | Fresh start prompt NOW |
| Getting confused about what you were originally building | 🟡 Warning signs | Consider a reset |
| Clean conversation flowing well | 🟢 Keep going | You're golden |

## why this matters 

And all of this ties back to your personal preferences, giving Claude a good base of who you are, how you're using AI and what you truly need from it. Just these small changes in your workflows will really advance your outcomes, I'm excited to hear about it! 🚀

---

previous: **06. stop asking for workarounds, build solutions**  
next: **08. [coming next]**  
find me on LinkedIn if the vibes feel right: **linkedin.com/in/oliviakeiter**
