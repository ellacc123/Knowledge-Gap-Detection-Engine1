# Knowledge-Gap-Detection-Engine
An ML system that automates knowledge gap detection for research team onboarding. This is part of ongoing research project, so I cannot disclose code. 

Link (if doesn't work scroll down for screenshots): http://playfair.cs.washington.edu:8590

Process:

1. The engine turns a research team's scattered artifacts (meeting transcripts, notes, papers) into a negotiable onboarding map.
2. The system proposes candidate knowledge units and lets the newcomer mark what they know, correct what the system misread, and trace every inferred gap back to the source text that produced it.
3. The output is a living knowledge graph that surfaces contested, missing, and prerequisite knowledge.
4. Then converts gaps into concrete learning actions.

---

## Screenshots

**Sign in / create a workspace.** A newcomer joins an existing team by name and PIN, or starts a new project by uploading a seed document. Teammates join later and their self-assessments stay private while team-level coverage is shared.

![Sign-in and workspace creation](01-signin.png)

**The map.** Extracted concepts laid out as an interactive graph. Colored nodes encode status (green known, orange gap, yellow contested/unsure, dark prerequisite); rings denote teammates. Nodes are draggable and the map redraws as claims are marked on the left.

![Knowledge graph map view](02-map.png)

**Gaps.** Identified gaps in priority order, each tagged with a learning level and its prerequisites, with entry points to inspect provenance or pull learning actions.

![Gap finder](03-gaps.png)

**Why is this a gap.** Provenance tracing. The gap is resolved to the specific source claims extracted from team artifacts, each shown with its claim type and confidence, so the user can judge whether the inference is sound or a misread.

![Provenance / why-a-gap view](04-why.png)

**Actions.** A gap converted into a concrete learning plan, including prerequisite reading pulled from Semantic Scholar with authors, year, and citation counts.

![Learning actions](05-actions.png)

**Artifacts.** The documents feeding the workspace. Removing one deletes its claims and rebuilds the map.

![Uploaded artifacts](06-artifacts.png)
