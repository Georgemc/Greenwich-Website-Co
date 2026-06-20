# Greenwich Web Co. — Editing Guide

Keep this open while you edit. Your whole site is one file: **`index.html`**.

---

## Setup (once)
1. Download **VS Code** (free) — much safer than Notepad, color-codes everything.
2. Open the `greenwich-web-co` folder in VS Code.
3. Double-click `index.html` to open it in your browser too.
4. **Workflow:** edit in VS Code → save (`Ctrl+S`) → switch to browser → refresh (`F5`).

## The #1 safety rule
Before editing, copy `index.html` and rename the copy `index-backup.html`.
If you break something: delete the broken file, rename the backup back. That's your undo.

---

## How to find what you want to change
Press `Ctrl+F` in VS Code and search for the words you see on the site.
Edit only the text **between** a `>` and a `<`. Don't touch the tags themselves.

```
<h3>Web Design</h3>
      ^^^^^^^^^^ only change this part
```

---

## Common edits

| What | Search for (Ctrl+F) | What to do |
|---|---|---|
| Big hero headline | `worthy of` | Retype the words; keep `<br>` and `<em>` tags |
| Hero sub-text | `Greenwich Web Co. designs` | Retype the sentence |
| Founder 2 & 3 names | `[Founder Name]` | Replace with real names (2 spots) |
| Founder roles | `[Role]` | Replace with their role |
| Founder bios | `[Short bio` | Replace with 2-3 sentences |
| Your email | `hello@greenwichwebco.com` | Replace both spots |
| Your phone | `914` | Update if needed |
| Stat numbers | `data-t="40"` | Change the number in quotes |
| Service descriptions | `Web Design`, `Development`, etc. | Edit the `<p>` text under each |
| The brand quote | `Have nothing` | Replace quote + the name below it |

---

## Swapping photos
Each photo is marked with `<!-- PLACEHOLDER -->`. Search `PLACEHOLDER`.

**Option A — use a photo on your computer:**
1. Make a folder called `images` next to `index.html`.
2. Drop your photo in (e.g. `hero.jpg`).
3. Change the link:
```html
<img src="images/hero.jpg" alt="Describe the photo briefly">
```

**Option B — use an online image:** paste any image URL into `src="..."`.

Always update the `alt="..."` text to describe the photo (helps Google + accessibility).

---

## Changing colors (safe + powerful)
Near the top, find `:root {`. Every color is set once here:
```css
--green-deep: #14342B;
--green: #2E5A4C;
--green-soft: #6B8F7E;
```
Change a hex code and it updates everywhere. Pick new hex codes at coolors.co.

---

## Safe vs. risky

| ✅ Safe for you | ⛔ Ask Claude first |
|---|---|
| Text between `>` and `<` | Anything inside `<style>` (the CSS) |
| Image `src` and `alt` | The `<script>` at the bottom |
| Email, phone, bios | Adding/removing whole sections |
| Color hex codes in `:root` | Changing the layout structure |

---

## When you're done
Save the file. If the site is live on Vercel and connected to GitHub, your changes
go live automatically a minute after you push them to GitHub (see deploy notes).
