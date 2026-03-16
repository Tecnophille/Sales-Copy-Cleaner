# Sales Copy Cleaner

A Claude Code skill that removes hype language from sales copy and rewrites it
as credible, professional prose.

Hype repels skeptical buyers. Specificity converts them.

## Installation

### Recommended

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/Tecnophille/sales-copy-cleaner.git ~/.claude/skills/sales-copy-cleaner
```

### Manual

```bash
mkdir -p ~/.claude/skills/sales-copy-cleaner
cp SKILL.md ~/.claude/skills/sales-copy-cleaner/
```

## Usage

In Claude Code, invoke the skill:

```
/sales-copy-cleaner

[paste your sales copy here]
```

Or ask directly:

```
Clean this sales copy: [your text]
```

Or:

```
Remove the hype from this: [your text]
```

## What it does

Takes copy like this:

> 🚀 Our world-class, cutting-edge platform is trusted by thousands of happy
> customers worldwide! Supercharge your team and take your business to the next
> level! Act now — limited time only!! RESULTS GUARANTEED!!

And turns it into this:

> Our platform connects your CRM, billing, and support tools so your team works
> from one dashboard. Used by 1,200 teams across 40 countries. If you don't see
> measurable improvement within 60 days, we offer a full refund.

## 20 patterns detected

### Content
| # | Pattern | Example before | Example after |
|---|---------|---------------|--------------|
| 1 | Superlative overload | "world-class, industry-leading, unmatched" | Specific performance data |
| 2 | False urgency | "Act now! Limited time only!" | Actual deadline if one exists |
| 3 | Vague power claims | "cutting-edge, revolutionary, next-gen" | What it actually does |
| 4 | Exclamation abuse | "Sign up! Get access! Results guaranteed!" | Plain statements |
| 5 | Empty benefit statements | "Supercharge your sales!" | Specific outcome with numbers |
| 6 | Hollow guarantees | "Proven system. Results guaranteed — period." | Guarantee with actual terms |
| 7 | Buzzword stacking | "seamless end-to-end ecosystem synergy" | What connects to what |
| 8 | Pain amplification overload | "Are you tired of struggling, grinding, failing?" | One honest acknowledgment |
| 9 | Fake social proof | "Trusted by thousands of happy customers!" | Real numbers and named clients |
| 10 | Overblown origin story | "After years of sleepless nights..." | Actual founding context |

### Language
| # | Pattern | Example before | Example after |
|---|---------|---------------|--------------|
| 11 | Feature listed as benefit | "Featuring advanced AI analytics!" | What the analytics actually show |
| 12 | Adjective piling | "incredibly powerful, beautifully designed, deeply intuitive" | Who it's built for and what it does |
| 13 | Lifestyle overclaim | "the key to the life and freedom you deserve" | Specific time saved |
| 14 | False exclusivity | "Not for everyone. Only the serious need apply." | Actual eligibility criteria |
| 15 | Certainty overclaim | "You WILL double revenue. This never fails." | Realistic range with caveats |
| 16 | Vague competitor dismissal | "Unlike overpriced outdated tools..." | Specific pricing or feature comparison |
| 17 | Loaded questions | "Don't you deserve to finally succeed?" | Direct statement of value |
| 18 | Passive value claims | "Designed to transform your workflow" | Actual measured outcome |
| 19 | Generic CTAs | "Start your journey today!" | Specific next step |
| 20 | Over-formatted hype | "✅ GUARANTEED!! 🚀 ACT NOW!! 💥" | Clean, plain text |

## Output format

Every cleaned piece comes back with three things:

1. **Cleaned copy** — the rewritten version
2. **What was removed** — brief bullets with pattern names
3. **[NEEDS DATA] flags** — claims that need real numbers before the copy is
   ready to publish

## Works on

- Product descriptions
- Email campaigns
- Landing pages
- Social media ads
- B2B and B2C copy

## Tone

Output is professional and formal by default — no exclamation marks unless
quoting a customer, no emoji in B2B contexts, active voice, short paragraphs.

## Platform support

| Platform | File | How |
|----------|------|-----|
| Claude Code | `SKILL.md` | Install to `~/.claude/skills/` and invoke with `/sales-copy-cleaner` |
| Claude.ai | — | No install needed. Paste copy and ask "clean this sales copy" |
| Warp | `WARP.md` | Paste entire file into Warp AI, add copy at the bottom |
| ChatGPT | `CHATGPT.md` | Use as a Custom GPT system prompt, or paste at start of chat |
| Gemini | `GEMINI.md` | Use as a Gem, or paste at start of chat |

## License

MIT
