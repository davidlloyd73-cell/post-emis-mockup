# After EMIS — a post-duopoly AI infrastructure for one NHS GP practice

A set of single-file, dependency-free HTML mockups that together map out — and
partly demonstrate — an AI infrastructure for an NHS GP practice. They accompany
the position paper *"After EMIS — AI is dissolving the GP EMR duopoly"*
(Lloyd, v2.5, May 2026) and draw on the working Ridgeway Surgery prototype.

**Live demo:** https://post-emis-mockup.netlify.app/

## The four pages

| Page | What it is |
|---|---|
| **`index.html`** — Consultation | The original animated mockup: one episode of care, walking the four-layer architecture (patient vault → local inference → boundary diode → cloud assurance). |
| **`infrastructure.html`** — Infrastructure map | An interactive map of the *whole* practice AI estate. Every layer of the architecture, populated with the real Ridgeway GitHub apps placed in their layer, with data-classification badges, the boundary diode, the governance wrap and the directional economics. Click any node to inspect it. |
| **`assurance-harness.html`** — Cloud Assurance Harness | The technical centrepiece of the paper, made into a working dashboard. Runs a synthetic-only assurance sweep through the four-layer evaluation stack (deterministic safety checks → guideline-grounded RAG → frontier multi-grader critique → human adjudication) and produces a versioned assurance report for the clinical safety case. Never sees patient data. |
| **`referral-pa.html`** — Refer-to | The service-owned referral directory from the *Refer-to* concept (companion to *The Referral PA*). Plain-English search returns one current service card — criteria, exclusions, route, what to attach, freshness — with NHS / statutory / VCS tier badges, safeguarding banners, and an AI steward that never overrides what a service says it does. |

## The architecture being mapped

1. **Patient vault** — patient is the primary rights-holder; clinical systems are
   licensees of scoped, time-limited access (`nhs.id/...`).
2. **Local clinical inference** — Qwen 2.5 32B on a Mac mini M4; identifiable
   patient data never leaves the practice perimeter.
3. **Boundary diode** — only synthetic test outputs, structured metrics, model
   hashes and signed inbound templates may cross.
4. **Cloud assurance harness** — multi-grader benchmarking on synthetic and
   public material; never sees patient data.

All wrapped in a governance layer: DCB0129/0160 clinical safety case, DPIA,
DSPT, named clinical safety officer, immutable audit, and triadic care
attribution (AI as a named, visible participant).

## Where the apps in the map come from

The infrastructure map places the author's real repositories into their
architectural layer — e.g. `survivalemr` (AI-native EMR), `diagnostic-teammate`,
`consultation-analyzer`, `refletter`, `Patient-Briefing`, `we-take-blood`,
`WSIC_Anon` (de-identification at the boundary), `gp-population-simulator` and
`gp-surgery-simulator` (synthetic test cohorts). See
[github.com/davidlloyd73-cell](https://github.com/davidlloyd73-cell).

## Run locally

```bash
python3 -m http.server 8000   # then visit http://localhost:8000
```

No build step, no dependencies — four self-contained HTML files that cross-link
via the nav bar at the top of each page.

## Author

Dr David Lloyd — Salaried GP, Ridgeway Surgery, Harrow.
Mockups prepared with Anthropic Claude as part of the working method described in
Appendix A of the position paper — locally-bounded AI for identifiable work,
cloud frontier capability for non-identifiable knowledge work and assurance.
