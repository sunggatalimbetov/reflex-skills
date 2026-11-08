# Reflex Skills

Skills the Reflex agent loads at runtime. A merge to `main` triggers a webhook that loads every Skill in this repo, and the agent can use them on the next message, with no release.

Each Skill is a folder `skills/<name>/` holding a `SKILL.md`: YAML frontmatter with `name` (equal to the folder name) and `description`, then the instructions. A folder can also hold an optional `flow.json`, a recorded HTTP flow on one site. The full format is in [hack-paris `docs/skills.md`](https://github.com/sunggatalimbetov/hack-paris/blob/main/docs/skills.md).

A malformed Skill is skipped with a reason shown in the webhook delivery's response. The other Skills still load.
