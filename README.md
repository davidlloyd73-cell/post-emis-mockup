# After EMIS — animated EMR mockup

An animated, single-file HTML rebuild of the post-EMIS / patient-vault EMR
mockup that accompanies the position paper *"AI is making the GP EMR
monopoly obsolete"* (Lloyd, May 2026).

**Live demo:** https://post-emis-mockup.netlify.app/

The animation walks through one episode of care to illustrate the
four-layer architecture proposed in the paper:

1. **Patient vault** — patient is the primary rights-holder; practice
   is granted scoped, time-limited access (`nhs.id/a-patel-1952`).
2. **Local clinical inference** — Qwen 2.5 32B on a Mac mini M4;
   identifiable patient data never leaves the practice perimeter.
3. **Boundary diode** — only synthetic test outputs, structured metrics
   and model hashes are permitted to flow outwards.
4. **Cloud assurance harness** — multi-grader benchmarking against
   synthetic and public material; never sees patient data.

## Animation phases

| Phase | What you see | Architectural principle |
|---|---|---|
| Vault access | Top bar transitions from "requested" to "granted" | Patient as rights-holder |
| Vault hydration | Right sidebar fields appear with purple vault marker | EMR as licensee, not owner |
| Tortus scribing | Consultation summary types live, line by line | Modular EMR, best-of-breed scribe |
| Context selection | GP picks chips: leg rash, prev visit, image | Clinician controls model context |
| Local inference | "Running locally…" shimmer, then opinion streams | On-premise inference |
| Allergy cross-ref | Right-hand allergy card flashes amber | Audit + triadic care |
| Patient letter | First-class drafted artefact, GP-reviewed | Patient-facing summary |
| Send to vault | Letter written back, audit entry recorded | Patient-controlled record |

The bottom caption strip names the principle from the paper at each
phase. The **▤ Architecture** button toggles a four-layer mini-diagram
that highlights the active layer as the animation runs.

## Run locally

```bash
open index.html
# or
python3 -m http.server 8000   # then visit http://localhost:8000
```

No build step, no dependencies — single self-contained HTML file.

## Author

Dr David Lloyd — Salaried GP, Ridgeway Surgery, Harrow.
Mockup and animation prepared with Anthropic Claude as part of the
working method described in Appendix A of the position paper.
