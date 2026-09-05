# הולך בדרכי — ספר לדפדוף

סיפור חייו של יעקב קבלה. ספר דיגיטלי לדפדוף, בעברית, מימין לשמאל.

**לקריאה: https://yohasson.github.io/kabala/**

---

## Holech Bedarki — RTL Hebrew Flipbook

A 3D page-turning web edition of a Hebrew family memoir.

- Right-to-left reading order — the book opens from the right
- Two-page spread on desktop, single-page swipe on mobile
- Two editions: standard (68 pp) and large print (84 pp, 14 pt)
- Hebrew UI: next / previous page, page counter, fullscreen
- Keyboard: `→` back, `←` forward, `F` fullscreen
- Live reading progress: the current chapter and percentage appear above the
  right-to-left scrubber, with a filled track and descriptive screen-reader
  value. Progress follows the source pages across mobile and desktop, from
  0% at the front cover to 100% at the final spread.
- Resume reading: returning visitors see a Hebrew card with their last page
  preview and a one-click return to it. The reader still opens at the cover.
  Reading position stays in this browser only; no account or server is used.
  Dismiss with “לא עכשיו” or `Esc`; navigating starts a new bookmark, and
  the reset control clears it. Mobile and desktop share the same saved page,
  even where mobile skips blank pages. Reading still works if browser storage
  is unavailable.

### Structure

```
index.html            the flipbook
images/regular/       standard edition, 68 pages
images/large/         large-print edition, 84 pages
```

Page images are served at screen resolution so the site loads quickly on
mobile data. The 300 DPI print masters are kept outside this repository.

Built with [StPageFlip](https://github.com/Nodlik/StPageFlip) (MIT),
vendored locally in `vendor/` — see `HANDOFF.md` before changing that.

**Rebuilding this site from a new edit of the book?** Read `HANDOFF.md`
first — it covers the full build pipeline, a real pagination mismatch
between the current print PDFs and these deployed images, everything
measured against the Heyzine reference this was styled on, and several
non-obvious bugs (and their fixes) that only surface under real
interaction testing, not a quick look.

See `NOTICE.txt` — the memoir text and photographs are not licensed for reuse.
