# Contributing

Thanks for helping keep these roadmaps accurate. Courses and tools change often, so corrections are as valuable as new resources.

## What we accept

- Fixes to broken links, renamed courses, changed prices or free tiers, and outdated exam versions.
- New resources that are free-first, practical and current.
- Better ordering, clearer descriptions and missing prerequisites.
- Corrections to cross-links between roadmaps.

## What we avoid

- **Books.** Roadmaps list websites, labs, official docs, courses, videos and exercises. Books go in the `books-and-paid.md` file of the relevant folder.
- **Passive-only content.** Prefer interactive labs, hands-on exercises and projects over reading or watching.
- **Duplicates.** If a resource already exists in another roadmap, link to it instead of copying it. See "Shared topics" in the [root README](README.md).
- **Affiliate links, referral codes and tracking parameters.**
- **Anything that facilitates illegal access.** Only legal, authorized practice targets belong in the security files.

## Layout

Each field folder contains a `README.md`, a `1-basics/` folder (what everyone learns first) and a `2-specialties/` folder (one file per role).

Each specialty file uses these sections, in this order:

1. Title, then **Role** and **Prerequisites**
2. **Skills, in order**
3. **Path at a glance** (beginner, intermediate, advanced)
4. Safety or cost warning, where relevant
5. **Resources** (table)
6. **Certifications**
7. **Project**

Basics files are shorter: a path at a glance and a table. Theory files use the Type and Free/Paid columns instead.

## Resource table

Use these five columns, in this order:

| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|

- **Resource:** a Markdown link to the official page or the most stable landing page.
- **Level:** Beginner, Intermediate, Advanced, or a range such as "Beginner to Intermediate".
- **Cost:** `Free`, `Free tier + paid`, `Free + paid`, or `Paid`. Add detail in brackets where it helps, for example `Free (open source) + paid cloud`.
- **What it is:** one or two sentences. Note anything a learner should check, such as which edition is current.
- **You will be able to:** a concrete skill, starting with a verb. Avoid "understand" and "learn about".

Order rows by level, from beginner to advanced.

## Essential vs supplementary

Resources are essential by default. Start the description with `Supplementary:` for optional extras such as extra practice, alternatives or reference material. Keep the essential set small enough that a learner can finish it.

## Verifying before you submit

Check the following yourself and say in the pull request what you checked and when:

1. The link opens and goes to the right page.
2. The cost label matches what you see. If you cannot tell which parts are free, use "Free tier + paid" and add a "check" note.
3. The resource is still maintained. Look for a recent release, course update or active community.
4. Version-specific material (exam codes, framework editions, course names) is current, or the row tells the reader to verify.
5. Lab instructions are safe: isolated VMs for malware and vulnerable machines, billing alerts for cloud labs, no real data.

If you cannot verify something, say so in the pull request rather than guessing.

## Cross-links

- Use relative links, for example `../../networking/1-basics/fundamentals.md`.
- When you move or rename a file, search for old links and fix them with `grep -rn "old-file-name.md" --include=*.md .`
- Do not rename section headings that other files link to (for example `## Certifications` and `## Project` in the networking files).

## Safety rules

- Only test systems you own or have written permission to test.
- Run malware, vulnerable VMs and attack datasets in isolated, snapshotted VMs with no shared folders.
- Never put real credentials, API keys or personal data in examples.

## Submitting changes

1. Fork the repo and create a branch, for example `fix/zeek-docs-link` or `add/ghidra-course`.
2. Make a focused change. One topic per pull request.
3. Use a short imperative commit message, for example `Update Zeek docs link` or `Add Ghidra course to forensics`.
4. In the pull request, describe what changed and what you verified.

## Pull request checklist

- [ ] Links open and point to the right pages
- [ ] Cost and level are filled in for every new row
- [ ] No books, affiliate links or duplicates
- [ ] "Supplementary:" is used for optional items
- [ ] Cross-links still work
- [ ] Safety or cost warnings are present where a lab needs them
