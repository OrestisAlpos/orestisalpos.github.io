---
published: false
---
# Adding a lesson

Copy `_template.md` to a new file named after the lesson date, e.g. `2026-09-11.md`,
then delete the `published: false` line.

- `date:` is the heading on /folk-dances/zentroom/ and sets the order (newest first).
- `dances:` is a list of slugs. A slug is the filename in `_dances/` without `.md` —
  it is also written in each dance's `slug:` field. A slug that matches nothing is
  shown on the page as an error rather than silently skipped.
- Everything below the front matter is free text and is optional.
