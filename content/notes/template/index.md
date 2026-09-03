---
# Copy this whole folder to `content/notes/<slug>/`, drop the PDF in beside
# `index.md`, then delete the `draft` and `build` keys at the bottom so it
# publishes. Nothing else is required except `title` and `date`.

title: 'Note title'
# Group heading on the Notes page. Omit it and the note falls into "General".
course: 'CS 180'
# Optional longer heading for the group; the first note in a group that sets
# this wins, so you only need it on one of them.
course_title: 'CS 180 — Algorithms'
# Must be a real, parsable date (YYYY-MM-DD) - it drives sorting. Hugo fails
# the build on anything else, so no 'Spring 2026' here.
date: 2026-01-15
# Optional. Shown on the card in place of the date, for coursework where the
# quarter reads better than a day.
term: 'Winter 2026'
summary: 'One line on what the note covers.'
# Optional, shown in the card footer.
pages: 12
tags:
  - algorithms

# By default the block picks up the single PDF sitting in this folder. Set
# `pdf:` only to override that — an external URL, or a second file in here.
# pdf: 'https://example.com/notes.pdf'

# --- delete both keys below when you copy this ------------------------------
draft: true
build:
  render: never
  list: never
---

Anything written below the front matter turns this into a real page: the card
then links here instead of straight at the PDF, and the PDF stays available as
a link in the body. Leave it empty for a PDF-only note and the card links
directly to the file.
