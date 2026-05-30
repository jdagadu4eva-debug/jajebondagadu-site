# Joyce Ajebon-Dagadu — Author Website

A single-file author website for **Crowned to Lead** and the children's Bible
storybook series. All ten cover images are embedded inside `index.html`, so the
whole site is just one file — nothing else needs to load.

**Live domain:** jajebondagadu.org (hosted on Cloudflare Pages)

---

## What's in this package

| File | What it is |
|------|------------|
| `index.html` | The entire website. This is the only file that has to be served. |
| `README.md` | This guide. |

---

## Part 1 — Put it on GitHub

**Easiest (web browser):**
1. Go to https://github.com/new and create a repository, e.g. `jajebondagadu-site`.
   Set it to **Public** (Cloudflare Pages reads it either way).
2. On the new repo page, click **uploading an existing file**.
3. Drag in **`index.html`** (and `README.md` if you like).
4. Click **Commit changes**.

That's it — the file is now on GitHub.

---

## Part 2 — Connect it to Cloudflare Pages

1. Go to https://dash.cloudflare.com → **Workers & Pages** → **Create** → **Pages**
   → **Connect to Git**.
2. Pick the repository you just created.
3. **Build settings — leave them empty.** This is a plain static site:
   - Framework preset: **None**
   - Build command: **(blank)**
   - Build output directory: **/**  (just a forward slash)
4. Click **Save and Deploy**. In under a minute you get a preview link
   like `jajebondagadu.pages.dev`. Open it to check the site.

---

## Part 3 — Attach your domain

1. In the Pages project, open the **Custom domains** tab → **Set up a domain**.
2. Enter **jajebondagadu.org**.
3. Because Cloudflare also runs your DNS, it adds the records and SSL
   automatically — both `jajebondagadu.org` and `www` — usually within minutes.
4. (Optional) Add **www.jajebondagadu.org** too, so both work.

Done. Every time you commit a change to the repo from now on, Cloudflare
re-publishes the site automatically.

---

## Editing the site later

Open `index.html` in any text editor and search for these tags:

- **`EDIT:LULU`** — the buy links. There's one for *Crowned to Lead*, one for the
  main store button, and the nine children's books are together in one list
  (`const BOOKS = [...]`) near the bottom. Paste your Lulu URL between the
  quotes for each.
- **`EDIT:BIO`** — your About text. (Drafted from our past conversations —
  please read it and adjust your title, focus, or any personal details.)
- **`EDIT:CONTACT`** — the email address and social links in the footer.
- **`EDIT:CROWNED`** — the Crowned to Lead description.
- **Author photo** — in the About section, replace the placeholder box with
  `<img src="...">` (search for "your photo here").

After editing, commit the file back to GitHub and Cloudflare updates the live
site on its own.

---

## Still to fill in

- [ ] Real Lulu links (store + each book)
- [ ] Contact email
- [ ] (Optional) Author photo
- [ ] Review the bio wording
