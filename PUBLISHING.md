# How to publish on Stars and Scarves

Every article is one markdown file in the `_posts/` folder. Push it (or create it on github.com in your browser) and it is live at starsandscarves.com about a minute later. The newest post automatically becomes the big lead story on the homepage; the next three fill the Latest Takes grid.

## Write a new article

1. Create a file in `_posts/` named with the date and a short slug:

   `_posts/2026-07-21-pulisic-was-right.md`

2. Start it with this header (the "front matter"), then write the article in plain markdown below it:

   ```markdown
   ---
   title: "Pulisic Was Right and Everyone Owes Him an Apology"
   categories: usmnt
   standfirst: "One sentence teaser that shows under the headline and on the homepage cards."
   ---

   First paragraph gets an automatic red drop cap, so start strong.

   ## Subheads look like this

   > Pull quotes look like this. Use one per article, max two.

   Regular paragraphs, [links](https://example.com), and lists all work.
   ```

3. Save, commit, push. Done.

## The fields

- `title` — the headline. Quotes required if it contains a colon.
- `categories` — one of: `usmnt`, `mls`, `worldcup`, `takes`, `section`. Controls the tag on the card and the URL (e.g. `/usmnt/pulisic-was-right/`).
- `standfirst` — the teaser sentence. Shows under the headline, on homepage cards, and as the Google description. Keep it punchy.
- Author defaults to Derek Benson automatically; add `author: "Someone Else"` to override.

## Three ways to publish

- **From this folder:** create the file, then `git add -A && git commit -m "New post" && git push`
- **From any browser:** github.com/SpinDash16/stars-and-scarves → `_posts` → Add file → Create new file → paste → Commit. Works from your phone.
- **Ask Claude:** describe the take, review the draft, it handles the rest.

## Gotchas

- The date in the filename must not be in the future, or Jekyll hides the post.
- If a new post does not appear after a few minutes, the GitHub Pages build may need a manual kick (Claude can do this, or check the repo's Actions/Pages settings).
- Never rename a published post's file casually: the URL changes and old links break.
