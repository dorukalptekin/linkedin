# LinkedIn content agent

A weekly research agent that scans the web for FMCG news, reports and earnings, keeps what fits Doruk
Alptekin's positioning (**building brand love and turning it into revenue in FMCG**), and drafts LinkedIn
posts for recruiters, CMOs and GMs at FMCG companies in Dubai.

## Files

| Path | What it is |
|------|------------|
| `profile.md` | Positioning, audience, experience pillars (P1–P7) and voice, taken from the CV |
| `config.yaml` | Themes, regions, sources, off-limits topics, ranking weights and output format. Edit this to steer the agent. |
| `agent/instructions.md` | The step-by-step procedure the agent follows each week |
| `digests/YYYY-MM-DD.md` | One digest per week: 5 ranked stories, each with an angle and a draft post |
| `history/surfaced.md` | Stories already suggested, used to avoid repeats |
| `history/posts.csv` | What you actually posted and how it performed. Fill this in so the agent learns what drives engagement. |

## Running it

In Claude Code, open this repo and say:

> Run the weekly scan.

`CLAUDE.md` points Claude to `agent/instructions.md`. To get it automatically each week, set it up as a
scheduled task (e.g. Monday 07:00 Dubai time) that runs the scan, commits the digest, and creates a Gmail draft for you.

## Weekly routine for you (about 20 minutes)

1. Read the digest and pick one story (or the evergreen idea).
2. Check the source and edit the draft in your own words.
3. Post Tuesday–Thursday, 08:00–10:00 GST, and put the link in the first comment.
4. Reply to every comment in the first hour.
5. A week later, add the post's numbers to `history/posts.csv`.

## Off-limits

No news about Coca-Cola or PepsiCo (companies, bottlers or brands), no politics or boycotts, and no confidential
employer information. See `config.yaml`.
