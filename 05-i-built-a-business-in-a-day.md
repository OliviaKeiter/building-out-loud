
# 05. i built a business in a day (and it was the boring part that made it possible)

2am decision. 9am domain. LLC filed, EIN issued, six agents running, two sites live, all before bathtime.

I've spent the last three entries writing about how I work with Claude. Yesterday I decided to find out what happens when you actually use all of it, all at once.

What happened was a business. Whoops.

---

## what actually got built

Let me give you the full picture before I explain how, because the how only makes sense once you understand the scope.

[Keiter & Co.](https://keiterandco.com) is a local web design business my husband Alex and I started in Petersburg, NY. The premise is simple: small local businesses in rural upstate New York and western New England either don't have a website, or have one that's embarrassing them. The market rate for quality web work is out of reach for a lot of them. Too expensive, too pretentious, or too technical for Sally from the Country Hair Salon to get her money's worth. We have the skills. We know these people. The math wasn't hard.

Here's what exists as of yesterday:

**The business.** LLC filed with New York State. EIN issued by the IRS. Which, by the way, New York State also requires you to publish your new business in a local newspaper for six consecutive weeks. *Yeah. A newspaper. Six weeks. I did not know this either.* The domain is live. The business is real.

**The service model.** Three tiers defined: Starter for simple presence sites, Standard for service businesses that want to be findable, Custom for anything requiring deeper engineering. A no-upfront payment option designed for clients where the build fee is a barrier, with a 12-month contract that amortizes the cost and drops to standard hosting after the term. A hosting model where we manage the infrastructure and clients pay monthly, so they never have to think about servers. A defined service area covering Bennington, North Adams, Hoosick, Troy, Williamstown, and surrounding rural areas, with Albany and the Capital Region in scope.

**The principles.** Five standing rules that govern every output, every client interaction, and every agent in the system. Not aspirational. Operating constraints. The one that matters most: agents recommend, build, and automate as far as possible. Humans push go. Always. No agent sends, posts, publishes, or communicates on behalf of Keiter & Co. without Olivia or Alex reviewing and approving first. That rule is written into every agent spec. Not assumed. Written.

**The agent fleet.** Six agents, each with a full spec and a kickoff prompt ready to go in Claude Code:

- **Client Intake Agent:** takes loose conversational notes from a real intake meeting and produces a structured build brief. Input is intentionally messy because real conversations with small business owners are messy. Works with what's there, flags every gap.
- **Post-Demo Proposal Agent:** takes the build brief and demo details and produces two things in sequence: an internal pricing note for us to confirm first, then a plain language client proposal in exactly three sections. What you're getting. What it costs. What happens next. Never upsells. Ever.
- **Scaffolding Agent:** reads the confirmed brief and produces a recommended site structure, then generates build-ready files once the structure is approved. Opinionated on purpose. If the brief points one direction but the content calls for something different, it says so and explains why.
- **Copy Drafting Agent:** writes first draft site copy in the client's voice, not in agency voice. Ghostwriting for the client, anchored to the voice notes from intake. Answer Engine Optimization baked in throughout, so the site surfaces when someone asks an AI assistant to recommend a local business.
- **Monthly Analytics Agent:** pulls site data once a month and produces two outputs: a plain language snapshot email for the client, and a detailed internal report for us. Client output sounds like a neighbor giving an honest update. Internal report is designed to catch problems before clients notice them.

Plus a shared agent foundation that every single one of them inherits before any agent-specific logic runs. Eight rules, loaded first, non-negotiable.

**The infrastructure.** Namecheap for domain registration. Netlify for hosting via GitHub, with Netlify DNS so SSL is handled automatically. Astro as the build framework. A VM running open source models via Ollama for internal tooling, sized to spin up when needed and deallocate when not, keeping costs manageable while the business scales.

**The client tracker.** Built in Google Sheets. Client status, tier, last contact, next actions. Updated manually for now, with direct write access as a future build.

**Two live sites.** [Keiter & Co.](https://keiterandco.com) itself. And a portfolio demo for Pegasus Water Inc., a woman-owned water purification and softening company in North Central Florida. 30 years of experience. Recognized as Best of the 352 two years running. 35 Google reviews. All of it completely buried by a Wix site that looked like it was built in 2014. The demo exists to show them what their business actually deserves. We haven't pitched them yet. The work earns the conversation.

That's the scope. One day.

---

## the hard part was the part that looked like not building

Before I registered anything or wrote a single line of code, I sat down with Claude and did the thinking.

Not "help me name my business." Not "write me a pricing page." The real thinking. What is this business, actually? What do we believe about how it should run? What will we never do? What happens when an agent drafts something for a client and it sounds wrong? What does the intake conversation look like when the client is a 65-year-old hardware store owner who has never thought about a website in his life?

The kind of thinking most people skip because it feels like procrastinating when there's actual building to do.

I ran that process twice. *The second pass found things the first one missed. I'm telling you it's worth it.*

---

## what a CLAUDE.md file is and why you need one before you do anything else

`CLAUDE.md` is a configuration file that lives in the root of a project repository and governs how Claude Code behaves in every build session it touches. It's the project's memory, its constraints, its personality, and its quality bar, all in one file, traveling with the work permanently.

Here's a section of ours:

```markdown
## How to build

- Build one step at a time. Do not get ahead of the current step.
- When each step is complete, tell me: what was built, what files were
  created or changed, and what the next step is.
- Ask before moving on to the next step.
- Do not refactor or reorganize anything I did not ask you to touch.
- Do not add features or functionality beyond what was asked for
  in the current step.
- If you think something should be done differently, say so before
  building, not after.
```

That's not a polite suggestion. That's a constraint that lives in every build session from the first file created. Claude Code reads it, applies it, and operates inside it. Every new client project spun up from our scaffold inherits that file. The agents already know who we are before the session starts.

---

## the spec plus the kickoff prompt: the actual handoff mechanism

Every agent has two files: a spec and a kickoff prompt.

The spec is the full document. What the agent does, what inputs it reads, what outputs it produces, what it never does, what rules it follows, how it handles edge cases. Written once, maintained as the agent evolves.

The kickoff prompt is the translation layer. It takes the spec and turns it into the starting instruction for a Claude Code session. You open a new session, paste the kickoff prompt, and the agent knows exactly what it is and how to work before you've said anything else.

A vague prompt gets a vague agent. A well-written spec paired with a clean kickoff prompt gets an agent that operates with real constraints from the first message. The quality of what comes out is almost entirely determined by the quality of what goes in.

The full methodology, the CLAUDE.md, the agent foundation, all six specs, and all six kickoff prompts, is public:

🔗 github.com/OliviaKeiter/olivia-keiter-build-methodology

Take it. Adapt it. Build something real with it.

---

## track every change from day one. i mean it.

Every project in our repo has three standard files that update automatically with every single change:

**`SPEC.md`** is the current state of the project. Not what was originally planned. What is actually being built right now, reflecting every decision made along the way.

**`TODO.md`** is the live task list. Checked and updated after every change. Always reflects exactly where the build stands.

**`VERSIONS.md`** is the detailed version log. Every entry includes the version number, the date, a one-line summary, and detailed notes on every file created or modified, every decision made, and anything removed or replaced.

```markdown
## v0.2 — 2026-04-09
**Summary:** Added Supabase client and environment variable setup.

**Details:**
- Created src/lib/supabase.js with Supabase client initialization
- Added VITE_SUPABASE_URL and VITE_SUPABASE_ANON_KEY to .env.example
- Removed placeholder API file from v0.1 scaffold, no longer needed
```

Going back through a build without this is genuinely painful. You end up reverse-engineering your own decisions, asking Claude what changed and when, trying to remember why you made a call three sessions ago. The version log is the receipt. Build it in from the start. You will thank yourself later. I promise.

---

## why the front load is the whole game

Here's the thing about doing the thinking first: you only have to do it once.

The business architecture, the standing principles, the voice guidelines, the agent constraints, the tracking structure. Done. Lives in the repo. Every build inherits it. Every agent carries it. The humans make the judgment calls, handle the client relationships, review everything before it moves.

And then the next morning the question isn't "how do I get this done."

It's "what do we get to build next?"

That's the shift. That's what AI enablement actually means, and most people aren't describing it this way because most people are still in the "how do I do this task faster" frame. The front load isn't overhead. The front load is what gets your brain back for the work that actually needs a human brain.

Entry 01 of this blog is six things I wish I knew when I started. Use Projects. Build a system. Think before you prompt.

Turns out if you actually do those things, you can register a business, stand up a full agent fleet, and ship two sites before dinner.

The boring part is load-bearing. Build it first.

---

🔗 repo: github.com/OliviaKeiter/building-out-loud

---

previous: __03. projects-vs-chats.md__
next: __05. coming soon__
find me on LinkedIn if the vibes feel right: __linkedin.com/in/oliviakeiter__

