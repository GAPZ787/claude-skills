# claude-skills

Personal collection of [agent skills](https://skills.sh) for Claude Code, kept in one
repo so every project — local or cloud container — can pull the same set.

## Contents

67 skills under [`.claude/skills/`](.claude/skills), sourced from:

| Source | Skills |
| --- | --- |
| [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) | `web-design-guidelines`, `vercel-react-best-practices` |
| [vercel-labs/skills](https://github.com/vercel-labs/skills) | `find-skills` |
| [mattpocock/skills](https://github.com/mattpocock/skills) | `grill-me`, `grill-with-docs` |
| [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) | `brandkit`, `industrial-brutalist-ui`, `gpt-taste`, `image-to-code`, `imagegen-frontend-mobile`, `imagegen-frontend-web`, `minimalist-ui`, `full-output-enforcement`, `redesign-existing-projects`, `high-end-visual-design`, `stitch-design-taste`, `design-taste-frontend` |
| [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | 50 marketing skills (`ab-testing` … `video`) |

## Use it in a project

Add as a submodule so the skills land where Claude Code looks for them:

```bash
git submodule add https://github.com/GAPZ787/claude-skills .claude/skills
git commit -m "Add Claude skills"
```

Update later with:

```bash
git submodule update --remote .claude/skills
```

## Use it in every cloud container (no per-repo step)

Add this to your Claude Code web environment's setup script — it seeds the
container's user-level skill directory on every session, regardless of repo:

```bash
npx -y skills add GAPZ787/claude-skills --global --yes --copy --skill '*'
```

## Use it locally

```bash
npx -y skills add GAPZ787/claude-skills --global --yes --copy --skill '*'
```

Skills run with full agent permissions — review before use.
