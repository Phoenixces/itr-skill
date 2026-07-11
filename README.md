# itr-skill

A Claude Code **skill** that helps any Indian individual taxpayer prepare and
e-file an Income Tax Return (ITR-1/2/3/4) on the official portal — under either
the old or the new tax regime.

It reconciles income to source documents, compares both regimes on real numbers,
fills the portal schedule-by-schedule, fixes validation defects, and guides
through payment and e-verification.

> ⚠️ **Not professional tax advice.** Indian tax rules change every assessment
> year — always re-confirm current-year slabs, limits, and forms. The taxpayer
> remains responsible for the figures filed. The agent will never enter your
> password/OTP, make the payment, or submit/e-verify on your behalf.

## What it covers

- Right ITR form (1/2/3/4) + old vs new regime comparison (115BAC) on actual numbers
- Old-regime deduction catalogue (80C, 80D, NPS, HRA, home loan, 80G, 80TTA …)
- Income reconciliation to Form 16, 26AS, AIS, bank statements, broker statements
- Presumptive taxation for freelancers/creators (44ADA/44AD)
- Capital gains — listed equity/MF (111A/112A), quarterly breakup for 234C
- Foreign assets (Schedule FA), foreign income (Schedule FSI), DTAA relief (Schedule TR)
- Virtual digital assets / crypto (115BBH, Schedule VDA)
- Independent tax computation to verify portal math before submission
- Portal navigation with workarounds for known quirks

## Repo layout

```
itr-skill/
├── README.md
├── .gitignore
├── docs/
│   └── Overview.md                 # document checklist & redaction guide
├── prompts/
│   └── evals.yaml                  # eval prompts and expected outputs for testing
└── .claude/
    └── skills/
        └── itr-india/
            ├── SKILL.md            # workflow + judgment (read first)
            └── references/
                ├── tax-regimes-and-slabs.md
                ├── deductions-old-regime.md
                ├── income-reconciliation.md
                ├── creator-44ada.md
                ├── capital-gains-other-sources.md
                ├── virtual-digital-assets.md
                └── portal-workflow.md
```

## Install

Clone and copy the skill into your Claude Code skills directory:

```bash
git clone https://github.com/<your-username>/itr-skill.git
mkdir -p ~/.claude/skills
cp -r itr-skill/.claude/skills/itr-india ~/.claude/skills/
```

Restart Claude Code. Load with `/itr-india` or just describe your ITR situation.

## Usage

```
/itr-india
```

Or start naturally:
- "Help me file ITR for FY 2025-26, I'm salaried with some capital gains"
- "I have foreign assets (ESPP) — do I need Schedule FA?"
- "Compare old vs new regime for me"
- "I'm stuck on a portal validation error"

## What to provide

Form 16, Form 26AS, AIS, bank statements, broker/MF statements for the FY.
See `docs/Overview.md` for the full document checklist.

## Disclaimer

Not a substitute for a CA or registered tax practitioner. Verify every figure
before filing. Authors are not liable for any filing made using this skill.
