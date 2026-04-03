# 03. Projects vs Chats, and why it matters more than you think

### the feature I ignored that I absolutely should not have

---

If you didn't know Projects was a thing, you're not alone. I used Claude for longer than I'd like to admit before I actually understood what they were for. And when I finally did, it was one of those "...oh. OH." moments that made me want to go back and fix everything.

So let's fix it together.

---

## first, the orientation sentence I wish someone had given me

Claude has a feature called Projects. A Project is a dedicated workspace where your instructions, preferences, and reference documents live separately from your conversation history. Every time you open a new chat inside a Project, those instructions load fresh at the top. Every single time. ✅

I KNOW. I KNOW. We know this.. but do we REALLY?

---

## what is a context window and why should you care

Every conversation you have with Claude exists inside something called a context window. Think of it as Claude's working memory for that session. Everything is in there: your instructions, your conversation history, your examples, your guardrails, your reference material. All of it.

But here's what a lot of people don't fully understand.

All of that information is competing for space. And each session only has so much space before things get.. complicated.

As your conversation gets longer, that window starts to fill up. Claude doesn't crash. It doesn't send you a warning. It quietly does exactly what it's designed to do: it starts making judgment calls about what to prioritize and what to compress.

> ⚠️ **Quick pause because I don't want to click-bait you:** Your history isn't gone. It's just harder to surface. And to make matters worse Claude is the one deciding what comes to the top. You are not a part of that decision.

Are you okay with that? I certainly was not.

---

## the part that should make you uncomfortable

Claude doesn't know what's important unless you tell it. And in a long chat, even telling it isn't enough, because that instruction is just text competing with everything else in the window.

Your required security guardrail that says "do not access external sources"? Looks exactly as important as "use font size 12."

> 🚨 **If you work in a regulated, federal, or enterprise environment:** I am certain your cyber team has opinions about guardrails being treated as optional suggestions. I'm going to guess those opinions are very loud ones.

Please don't get me wrong. This isn't Claude failing. Claude is doing exactly what it's designed to do, and it's doing it extremely well. The problem is that we weren't giving Claude what it needed to do more.

---

## the rating scale nobody asked for but everyone needs 📊

**How are your current chat habits doing?**

| Habit | Vibe Check |
|---|---|
| Starting every conversation from scratch with no context | 🔴 We need to talk |
| Running the same chat for days or weeks | 🔴 Babe, no |
| Pasting your instructions at the top of every new chat | 🟡 Resourceful but exhausting |
| Using Projects with clear instructions | 🟢 You're doing amazing sweetie |
| Using Projects AND a setup process | 🟢 Okay we stan |

*I was firmly in the 🔴 "running the same chat for weeks" category for longer than I will publicly confirm.*

---

## so what actually fixes this??

Project instructions. *(Stick with me I'm getting there.)*

They don't live inside the conversation window. They don't compete with your history. They load fresh at the top of every single session, every time, no matter how long your chat history gets.

That's not a small difference. That's the difference between hoping Claude remembers what matters to you and building a system where it doesn't have to. 💡

---

## how to actually set up a Project: the process I use every single time

*Yes, every time. Even now. Even for this blog. You'll see why.*

---

### step one: start a chat and let er rip 🗣️

Don't open Project instructions and stare at a blank box. Open a regular chat first.

Tell Claude you need help setting up a Project. Then talk. Yap away. Tell it everything you can think of: what the Project is for, who the audience is, what you want Claude to always do, what you never want it to do, what tone you're going for, what format you prefer, what the guardrails are, how you feel about the project, why it's important to you. Don't edit yourself. Don't organize it. Don't try to build a perfect prompt. Just get it all out.

At the end of that brain dump, add this:

> *"Please continue interviewing me until you have everything you need to write a strong Project instruction file."*

Claude will ask follow up questions. Probably an annoying amount of follow up questions. Answer them. When it has enough, ask it to write the instruction file.

---

### step two: do it again (girl.. are you serious?? I am sorry!) 🔁

Take that instruction file. Open a brand new chat. Paste it in and say:

> *"Please read these Project instructions and interview me with any follow up questions you have, what is not clear and what needs more details?"*

> ⚠️ **This step is not optional.** The number of times the second pass has caught something the first missed is genuinely wild.

Here's why it matters: in the first chat, Claude is doing a lot at once. Building the file, tracking your answers, managing the conversation. The second chat has one job: read this and find the gaps. Fresh context, no competition, no history. Just a clean pass over what you built.

*A security note. An edge case. A missing feature. Two minutes of your time. Potentially hours saved. (ask me how I know)*

---

### step three: paste, test, iterate 🔧

Drop your final instruction file into your Project settings. Run a few test conversations. Notice what's missing or off. Go back and adjust.

Your Project instructions are not a "set it and forget it" situation. They're a living document. The best ones I have went through at least three rounds of real use before they felt right.

---

## the tldr for the people who scrolled straight here 👇

- Chats are for quick, contained tasks
- Projects are for anything with ongoing context, guardrails, or instructions that need to stay consistent
- Long chats don't lose your instructions, they bury them, but Claude decides what surfaces
- Project instructions load fresh every session and don't compete with your history
- Set up your instructions in a chat first, ramble everything, let Claude interview you
- Then do it again in a fresh chat to catch what the first pass missed
- Claude is doing exactly what it's designed to do. Empower it to do more.

---

*Full LinkedIn series in progress. If you found this helpful, the rest of the series is below. 👇*

---

**previous:** [02. Claude doesn't know you](./02-claude-doesnt-know-you.md)

**find me on LinkedIn if the vibes feel right:** [linkedin.com/in/oliviakeiter](https://www.linkedin.com/in/oliviakeiter)

