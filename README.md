# Page One skills

Free skills for artificial intelligence (AI) assistants, from [The Page One Project](https://pageoneproject.org). "Every doctor on the same page."

A **Page One** is a single printed page, kept current, that a patient or family caregiver hands to any doctor before the visit starts. What matters most is at the top, and every line shows where it came from. It exists because a patient's records are spread across health systems that often can't see each other, so every new doctor starts from zero.

These skills teach an AI assistant to build one the way our family does.

## What's here

| Skill | What it does |
| --- | --- |
| [`page-one-brief`](skills/page-one-brief/SKILL.md) | Builds a Page One for the doctor and a private visit prep sheet for the family, from the patient's own health records. |

A second skill, for finding and linking patient portals, is being tested and will be added here.

## What `page-one-brief` gives you

One printout, sorted into three sets. Every sheet says at the bottom which set it belongs to.

1. **Your prep sheet.** Your questions, what to tell the doctor, what to ask the office to fix in the chart, and room for notes. It stays with you.
2. **Set 1, for the front desk.** Page One, plus any supporting pages, to be scanned into the chart.
3. **Set 2, for the provider.** Page One goes into the doctor's hand as they walk in. The supporting pages stay within reach in case they want the detail.

Along the way, the skill:

- Asks what is really being taken, what has run out, and what has changed, because what the patient does beats what the chart says.
- Checks for anything new since the last summary before it reuses an old line.
- Traces refills that never arrived.
- Shows where two offices list different doses for the same medicine.
- Finds tests that were ordered and never done.
- Keeps Page One to one page, and moves the overflow to supporting pages instead of throwing it away.

## The rules it follows

- **Facts only.** No diagnosis and no treatment recommendations.
- **A source and a date on every line.**
- **Nothing invented.** If the records disagree, it shows both.
- **A person checks every line before anything is printed.** An AI can misread a record or mix up two medicines. Check each line against the records and the bottles at home.

## How to get it

**Claude (the app).** Download [page-one-brief.zip](https://pageoneproject.org/skills/page-one-brief.zip). In Claude, open Customize, then Skills, and upload the file. Claude's [skills guide](https://support.claude.com/en/articles/12512180-use-skills-in-claude) has the current steps.

**ChatGPT or any other assistant.** Open the [text version](https://pageoneproject.org/skills/page-one-brief.txt), copy all of it, and paste it into a new chat. Then tell it who the page is for.

**Claude Code, Cursor, Codex, and other coding agents.** One line installs it with the open [skills](https://skills.sh) installer:

```
npx skills add garrycook/page-one-skills
```

It asks which of your agents should get the skill. To look before you install, add `--list` to the end. Or copy the `skills/page-one-brief` folder into your agent's skills directory by hand.

Then say something like: "Make a Page One and prep sheet for my appointment on Wednesday."

## Privacy

The skill runs inside your own AI assistant. Nothing is sent to The Page One Project. Your records stay in your own account with the company whose assistant you use, so read that company's privacy settings and share only what you're comfortable sharing.

## Not medical advice

The Page One Project is not a medical provider and does not give medical advice. A Page One is a summary of facts for a clinician to read. It never replaces the doctor.

## More from the project

- [pageoneproject.org](https://pageoneproject.org): what Page One is and how we use it at a visit.
- [Find your portals](https://pageoneproject.org/portals): a free state-by-state guide to patient portals, with sign-in links, apps, and how family access works.
- [No Page One with you?](https://pageoneproject.org/emergency): what to say and do in an emergency room.
- [Using an AI assistant](https://pageoneproject.org/ai): our rules for using AI with health records.
- Questions or ideas: [hello@pageoneproject.org](mailto:hello@pageoneproject.org)

## License and credit

Copyright 2026 Garry Cook, The Page One Project.

These skills are licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). The full terms are in [LICENSE](LICENSE). You're free to use, change, and share them, including in paid products and services, as long as you give credit.

**How to give credit.** Wherever you share a skill or something built from it, include this, with the links, and say what you changed:

> Based on the Page One skills by [The Page One Project](https://pageoneproject.org), licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

**One more request.** Please keep the line "Format by The Page One Project, pageoneproject.org" that the skill prints at the bottom of each page. That's a request, not a license term. That line is how the next family, and the next doctor, finds the method.

The first version posted here (commit `9781074`) was released under the MIT License. Copies made from that version keep those terms.
