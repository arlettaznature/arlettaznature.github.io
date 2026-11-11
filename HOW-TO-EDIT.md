# How to edit the website

Everything on the website is stored as simple text files in this repository.
You edit them directly on github.com. **About one minute after you save, the
website updates by itself.**

---

## 1. Change text on a page

1. Find the file (see "Where is what?" below) and click on it.
2. Click the **pencil icon** ✏️ (top right of the file).
3. Change the text.
4. Click the green **Commit changes…** button, then **Commit changes** again.

That's it. If you make a mistake, you can simply edit the file again –
GitHub keeps every earlier version (see the "History" button).

### Text formatting

| You type | You get |
|---|---|
| `## Heading` | a heading |
| `### Smaller heading` | a smaller heading |
| `**bold**` | **bold** |
| `*italic*` | *italic* (e.g. for species names: `*Upupa epops*`) |
| `- item` | a bullet point |
| `[link text](https://example.org)` | a link |
| an empty line | a new paragraph |
| a new line | a line break |

### The block at the top of each file

Every file starts with a few lines between `---`, for example:

```
---
title: "Hoopoe"
---
```

This is the page title. You can change the text between the quotes,
but keep the `---` lines and the quotes.

---

## 2. Add a publication

1. Open the folder **publications** and the file of the year, e.g. `2026.md`.
2. Click the pencil ✏️ and add the reference as a new paragraph
   (an empty line before and after), in the same style as the others:

```
Author, A., B. Author & R. Arlettaz. 2026. Title of the paper. Journal 12: 34-56. [PDF](https://doi.org/10.xxxx/xxxxx)
```

3. Commit changes.

**A new year:** open the folder **publications**, click **Add file → Create new file**,
name it e.g. `2027.md` and start it with:

```
---
title: "Publications 2027"
layout: publications
year: 2027
---
```

The publications page automatically shows the newest year, and the year list updates itself.

---

## 3. Add a news item (homepage)

1. Open the folder **_news**.
2. Open an existing news file and copy its whole content.
3. Go back to **_news**, click **Add file → Create new file**.
   Name it with the date and a short title, e.g. `2026-11-20-new-project.md`.
4. Paste and adjust:

```
---
title: "Title of the news item"
category: "Research"
date: "2026-11-20"
image: "/assets/images/news/my-picture.jpg"
link: "https://link-to-the-full-story"
---

One or two sentences of text.
```

The homepage shows the newest news items first. To remove one, open the file,
click the **⋯** menu (top right) and **Delete file**.

---

## 4. Add a picture or a PDF

1. Open the folder where it should go:
   - pictures: `assets/images/` (e.g. `assets/images/news/` or `assets/images/hoopoe/`)
   - PDFs: `files/`
2. Click **Add file → Upload files**, drag the file in, and commit.
3. Use it in a page:
   - picture: `![short description](/assets/images/hoopoe/my-picture.jpg)`
   - PDF: `[PDF](/files/my-document.pdf)`

**Tip:** use file names without spaces or special characters
(`hoopoe-nest-2026.jpg` rather than `Hoopoe nest (final).JPG`),
and keep pictures smaller than about 1 MB.

---

## 5. Add a new project page

1. Open the folder **research**, open a similar existing page and copy its content.
2. In **research**, click **Add file → Create new file**, name it e.g. `red-kite.md`.
3. Paste, change the title and the text, commit.
4. The page is now at `/research/red-kite/`. To link it from an overview page,
   edit e.g. `research/projects-by-model-species.md` and add a line:
   `- [Red kite](/research/red-kite/)`

---

## 6. Change the menu, site title or colours

- **Menu:** `_data/navigation.yml`
- **Site title, subtitle, footer text, contact e-mail:** `_config.yml` (top part)
- **Colours:** `assets/css/style.css` (the first lines starting with `--`)
- **Logo:** upload it to `assets/images/`, then add a line `logo: /assets/images/logo.png` to `_config.yml`

---

## Where is what?

| On the website | File |
|---|---|
| Homepage text and photo | `index.md` |
| News items | folder `_news` |
| Research axes | `research/index.md` |
| Project overviews | `research/projects-by-….md` |
| Project pages (Hoopoe, Bearded vulture, …) | `research/<name>.md` |
| Publications | `publications/<year>.md` |
| Media | `research/media.md` |
| Book | `research/book-biodiversity-of-valais.md` |

## If something looks wrong

- Wait a minute and reload the page (the website needs a moment to update).
- Click the **Actions** tab of the repository: a red ✗ means the last change
  had a formatting problem. Open the file you just changed and check the
  `---` block at the top (quotes and `---` lines must be there).
- You can always restore an earlier version: open the file → **History**.
