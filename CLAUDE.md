# CLAUDE.md: Concept to Comics repo

## What this repo is
A model-agnostic skill that turns any concept into a 3-5 panel kid-level comic using analogies from the reader's own culture. It is SK's "Weekend Project #1": free, open source, built to grow an audience for the weekly weekend-project series and the paid "Build your first app with AI" sessions.

## The product is SKILL.md
- `SKILL.md` is the single source of truth. It must work BOTH as an Agent Skill AND when pasted as the first message into ChatGPT/Gemini.
- So: keep it **self-contained**. Never make SKILL.md depend on other files to work. `cultures/` packs are optional extras.
- Keep it under ~350 lines. No tool-specific features (no Claude-only tool names) in the core flow.
- Keep the frontmatter `name` and `description` valid per the Agent Skills spec (agentskills.io/specification).
- Default output is light (script + mapping + where it breaks + menu). The AI-drawn HTML page is opt-in ("draw") because it costs ~10x the tokens. Always ask setup; never guess audience/culture/language.

## The viewer (`viewer/index.html`)
- Free, no-login page on GitHub Pages: https://techiesasikumar.github.io/concept-to-comics/viewer/
- Draws any script written in SKILL.md's Step 4A format (COMIC / PANEL / Place / Show / Things / Board / Caption / speech). If you change that format in SKILL.md, update the viewer parser too, and vice versa.
- Single self-contained file (no build step, no dependencies except Google Fonts). Share links store the script in the URL hash, so no server.

## Structure
```
SKILL.md            the skill (core product)
README.md           GitHub landing page, written for non-tech readers
viewer/index.html   free comic viewer: paste a script, see it drawn (GitHub Pages)
cultures/           community culture packs (_template.md + one file per culture)
examples/           finished sample comics: script.md + comic.html + preview.png
assets/             README demo.gif + social-preview.png (1280x640)
LICENSE             MIT
```

## Quality bar (never compromise)
Every comic covers WHAT, WHY and SO WHAT, has one idea only, and every row of its mapping table is factually true. Simple AND correct.

## Current TODO
1. [x] Build `examples/inflation-tamil-kids/comic.html` from its script.md (follow SKILL.md Step 4B), screenshot it to preview.png
2. [ ] Add examples: `jvm-college-students` (Tamil Nadu, Tanglish), `photosynthesis-kids-global` (English), `internet-elders-tamil-nadu`
3. [ ] Test SKILL.md by pasting it into ChatGPT and Gemini; note any differences and tighten the wording
4. [x] Record demo GIF for README (`assets/demo.gif`, made with Playwright + ffmpeg)
5. [x] Add Build with me waitlist line + Instagram links in README (live session link still "coming soon")
6. [x] `git init`, first commit, create public GitHub repo `concept-to-comics`, push
7. [x] Build the free comic viewer (`viewer/index.html`) and point SKILL.md + README to it
8. [x] After push: turn on GitHub Pages (main branch, root) and check the viewer URL works
9. [x] Launch prep: "Try it now" section in README, social preview image (`assets/social-preview.png`, 1280x640)
10. [ ] Create the Gemini Gem from SKILL.md and add its share link to the README "Try it now" section
11. [ ] Upload `assets/social-preview.png` in GitHub repo Settings → General → Social preview (no API for this)

## Style
- README: simple English, emojis OK, short sections, non-tech people should understand it.
- Commit messages: short, present tense ("Add JVM example").
