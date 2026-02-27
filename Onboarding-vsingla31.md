Async Project Snapshot + Demo Log for HAAG  
-Vidushi Singla 

Problem  
Currently it is not very clear what each HAAG project is doing right now, what the current goal is, who owns what, and where the most important links live (repo, papers, docs, onboarding steps). Whatever information exists is often scattered across Slack threads, different GitHub repos, wiki pages, webpages, and older PDFs—and may be outdated or incomplete. This creates confusion for incoming students, volunteers, and even existing members who want to contribute but don’t know where to start.

Improvement Idea  
Project teams can maintain a simple, standardized “first stop” set of project context that is easy to keep updated asynchronously:

1) A one-page Project Snapshot that explains what the project is, what the current goal is, the current status, who to contact, and how to contribute.  
2) A lightweight Demo Log where teams capture small progress updates (e.g., a new result, a PR merged, a new experiment run, a quick walkthrough) with a link to the relevant artifact.

These artifacts can live in the project repo (or a linked HAAG repo if needed) and be indexed from a single wiki page. This creates an “async showcase” that improves project discoverability and collaboration without requiring a live event.

Recruitment / Onboarding Context  
This can be especially useful at the beginning of the semester (when people are choosing projects) and throughout the semester (when new contributors join or rotate). It reduces ramp-up time and helps people make better decisions about which project to join by giving them a clear, current view of the work.

Status Quo  
It would be important to understand how project context is currently communicated and where it is stored. This can be done via:

- Interviewing/Surveying newcomers (students/volunteers) about what was confusing and what information they needed to start  
- Interviewing/Surveying project leads/managers about the most repeated questions they get (“Where is the repo?”, “What should I do?”, “Who owns this?”)  
- Finding where current project information is housed (Slack, Wiki, Webpage, PDFs, GitHub repos, papers)  
- Capturing simple baseline signals such as:
  - Count of repeated onboarding questions in Slack over a short window  
  - Self-reported clarity score (1–5): “I understand what this project is doing and how to contribute”  
  - Time-to-context: “How long did it take you to find where to start?”

Potential Procedure  
Create a template or series of templates for projects to follow for publishing async context:

1) Create a Project Snapshot Template (1 page, 10–15 minutes to fill)
- Project one-liner + problem being solved  
- Current goal (this month/semester)  
- Current status (working / blocked / needs help)  
- Owners/contact points (lead + backups)  
- Key links (repo, papers, docs, datasets, meeting notes if applicable)  
- “Start here” steps for a newcomer + 2–3 starter tasks

2) Create a Demo Log Template (5–10 minutes per entry)
- What changed / what was built  
- Why it matters  
- Link to artifact (PR/commit, doc, video, screenshot, results)  
- Next step / open questions

3) Decide where it will live and how it will be indexed
- Store in repo as `PROJECT_SNAPSHOT.md` and `demos/` folder (or `DEMO_LOG.md`)  
- Add “Last Updated” date to reduce staleness  
- Create a simple wiki index page listing projects and linking to each latest snapshot

4) Communication
- Post a single Slack message pointing newcomers to the Snapshot as the “first stop”  
- Encourage teams to add a Demo Log entry whenever they have a meaningful update

Validating the Idea and Procedure  
Trial run the procedure with one project team (pilot) and a small set of newcomers or OMSCS community members:

- Ask 3–5 people to use the Snapshot and answer quick questions:
  - “Do you understand what the project is doing?”  
  - “Do you know who to contact?”  
  - “Do you know how to start contributing?”  
- Compare before/after on:
  - Clarity score (1–5)  
  - Time-to-context  
  - Number of repeated onboarding questions (or qualitative reduction in confusion)

Risks  
- Information may become outdated if not maintained.  
  - Mitigation: Add “Last Updated” and assign a primary/backup owner for refreshing monthly (5 minutes).  
- Teams may not adopt the system due to bandwidth or preference.  
  - Mitigation: Keep templates short, pilot with one willing team, and document reasons if teams decline.  
- Added overhead could create friction.  
  - Mitigation: Keep Snapshot one page and Demo Log optional; focus on links over long text.

Audience for the Procedure  
Any project lead, manager, or admin who wants to reduce onboarding friction and improve collaboration. Other stakeholders include HAAG leadership for visibility and standardization, faculty/advisors who want quick project context, and incoming students/volunteers who need a clear way to evaluate and join projects.