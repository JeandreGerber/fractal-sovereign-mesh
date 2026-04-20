# Open Problems

This is the living list of unsolved problems in the FSM Protocol. These are genuine engineering, legal, social, and technical challenges that require domain expertise the founding team does not have.

**How this works:**
- Anyone can propose a new problem — open an Issue with the `problem` label
- Anyone can propose a solution — see [CONTRIBUTING.md](../CONTRIBUTING.md)
- Solved problems get documented in their relevant directory and marked `[SOLVED]` here
- Problems that generate significant discussion may be broken into sub-problems

The protocol is only as strong as the weakest unsolved problem. Every contribution here makes the whole system more deployable.

---

## Open Problems

---

### PROBLEM-001 — Water Recovery in Arid Climates at the Unit Level

**Status:** Open  
**Domain:** Engineering  
**Priority:** High

**The Problem:**  
A family of four in a semi-arid climate (e.g., northern Mexico, Arizona, North Africa) needs approximately 80-100 gallons per day for drinking, cooking, and sanitation. Rainwater harvesting alone is insufficient in arid conditions. What is the minimum viable atmospheric water generation setup for a single residential unit powered entirely by a residential solar array?

**Why It Matters:**  
Many of the most likely early deployment locations for FSM nodes are in arid or semi-arid climates. Water is the constraint that hydroponics alone cannot solve — you still need the input water. Without a unit-level solution, the retrofit blueprint is incomplete for a large percentage of the global deployment surface.

**What a Good Solution Looks Like:**
- Specific hardware recommendations with real 2025/2026 pricing
- Power consumption spec compatible with a residential solar array (10-15kW)
- Failure modes and redundancy requirements
- Minimum humidity thresholds for viability
- Cost per liter of produced water at steady state

**Constraints:**
- Must be operable without grid connection
- Must be maintainable by a non-specialist with access to the Alexandria Protocol archives
- Must function in humidity as low as 20% RH

---

### PROBLEM-002 — The Readiness Score Algorithm

**Status:** Open  
**Domain:** Systems Design / Multi-Disciplinary  
**Priority:** High

**The Problem:**  
The readiness score measures a household's progress toward integration readiness across four dimensions: energy independence, water independence, food contribution, and waste diversion. How should these dimensions be weighted relative to each other? Is a household that is 80% energy independent but grows no food more or less ready than one that is 40% energy independent but contributes 30% of its caloric needs?

**Why It Matters:**  
The readiness score is the primary qualification mechanism for network integration. If it is weighted incorrectly, the network either excludes valuable households or admits unprepared ones. It also needs to account for geographic variation — the score for a household in a temperate climate with reliable rainfall should be calibrated differently than one in an arid climate.

**What a Good Solution Looks Like:**
- A weighted scoring model with justification for each weight
- Geographic adjustment factors (arid, temperate, tropical, urban)
- A minimum viable score definition (currently set at 40/100 as a placeholder)
- Validation methodology — how do we know the weights are right?

**Requires input from:** Nutritionists, permaculture designers, energy engineers, systems designers

---

### PROBLEM-003 — Cross-Jurisdiction Housing Equity as Securities

**Status:** Open  
**Domain:** Legal  
**Priority:** Critical

**The Problem:**  
FSM nodes structure housing as tokenized equity in a town corporation. When a resident sells their equity or relocates to another node and exchanges equity, that is potentially a securities transaction under US, Mexican, EU, and other jurisdictions. How do you structure the corporate entity and the equity instrument so that these transfers are legally clean without triggering securities registration requirements that would make the system inaccessible?

**Why It Matters:**  
If housing equity transfers require SEC registration or equivalent in each jurisdiction, the mobility protocol and exit buyout become legally unworkable for most participants. The entire economic model depends on residents being able to hold, transfer, and liquidate their equity cleanly.

**What a Good Solution Looks Like:**
- A corporate structure (LLC, cooperative, benefit corporation, or other) that accommodates equity-as-housing in at least US and Mexican jurisdictions
- An analysis of whether blockchain tokenization helps or complicates the securities question
- Template language for the equity instrument that minimizes regulatory exposure
- A red-line list of structures that definitely trigger registration requirements

**Requires input from:** Corporate lawyers specializing in cooperative housing, blockchain equity, and cross-border structures

---

### PROBLEM-004 — AI Governance Audit Protocol

**Status:** Open  
**Domain:** AI Safety / Systems  
**Priority:** High

**The Problem:**  
The FSM's central governance AI runs on a local server, air-gapped from external networks. Over time, through retraining, updates, or simply optimizing for its stated objectives in unexpected ways, it could drift from its charter objectives. How do you verify that a locally-run AI instance is still operating in alignment with the charter — without external connectivity and without requiring the kind of AI expertise that most nodes will not have?

**Why It Matters:**  
The AI is the operational backbone of the town. If it drifts — even subtly — the governance layer degrades before anyone notices. An audit protocol that requires external AI experts is not viable at scale. It needs to be something a technically literate resident can run.

**What a Good Solution Looks Like:**
- A set of behavioral tests the AI should pass to confirm charter alignment
- A plain-language audit checklist a non-specialist can execute
- Trigger conditions that should prompt a manual audit (anomalies in voting patterns, treasury movements, etc.)
- A rollback protocol if the AI fails audit

**Requires input from:** AI safety researchers, systems engineers, governance designers

---

### PROBLEM-005 — Conflict Resolution at 5,000+ People Across the Dunbar Stack

**Status:** Open  
**Domain:** Organizational Psychology / Governance  
**Priority:** Medium

**The Problem:**  
The Dunbar Stack governance model works cleanly at the tribe level (150 people) where everyone knows everyone. At the clan level (500) and especially at the full 16-town city level (5,000+), inter-tribal disputes and cross-node conflicts involve parties who do not have the relational context that makes informal resolution work. What does a formalized conflict resolution protocol look like that scales across the full stack without creating a permanent professional class of adjudicators (which would itself become a power structure)?

**Why It Matters:**  
The single biggest failure mode in intentional communities is not technical. It is interpersonal conflict that is not resolved early enough and spreads through the social fabric. At 150 people, informal mechanisms work. At 5,000, they do not — but formal courts create exactly the kind of fixed power positions the system is designed to prevent.

**What a Good Solution Looks Like:**
- A tiered resolution protocol that maps to each Dunbar layer
- Qualification and rotation requirements for mediators at each tier
- A mechanism for cross-node disputes where neither node's mediators are neutral
- How the AI assists without replacing human judgment

**Requires input from:** Professional mediators, organizational psychologists, conflict resolution researchers

---

### PROBLEM-006 — Hydroponic Monoculture Risk at Network Scale

**Status:** Open  
**Domain:** Agriculture / Systems  
**Priority:** Medium

**The Problem:**  
When the Megatropolis farming protocol orchestrates crop rotation across multiple nodes at scale, efficiency increases — but so does systemic vulnerability. If the AI optimizes all nodes toward the same high-yield cultivars on similar schedules, a single pathogen or pest that hits one node could cascade across the entire network simultaneously. What is the minimum biodiversity constraint that needs to be baked into the AI's optimization function to maintain resilience without sacrificing meaningful yield efficiency?

**Why It Matters:**  
The Irish Potato Famine is the canonical example of what monoculture at scale does when a pathogen arrives. A network that achieves 80% food sovereignty and then loses it simultaneously across 20 nodes is worse than never having built it.

**What a Good Solution Looks Like:**
- A minimum biodiversity percentage per growing zone (heirloom varieties, experimental cultivars)
- A pathogen monitoring protocol that triggers crop diversification
- How the AI balances yield optimization against resilience constraints
- Whether the network should maintain seed banks and if so, how

**Requires input from:** Agricultural scientists, permaculture designers, food systems researchers

---

## Solved Problems

*None yet. Be the first.*

---

## How to Propose a New Problem

Open a GitHub Issue with the label `problem` and use this template:

```
**Problem:** One clear sentence.

**Why it matters:** What breaks if this stays unsolved.

**Domain:** Which discipline(s) this falls under.

**What a good solution looks like:** Constraints and requirements.

**Requires input from:** What kind of expertise is needed.
```

---

*Last updated: 2026 · Maintained by the FSM community*
