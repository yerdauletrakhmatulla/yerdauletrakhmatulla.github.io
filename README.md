# yerdauletrakhmatulla.github.io

Personal website of Yerdaulet Rakhmatulla in English, Russian and Kazakh. Built with [Hugo](https://gohugo.io) and published by GitHub Pages. Every change pushed to `main` rebuilds the site in about a minute (see the **Actions** tab).

## Where things are

| What | Where |
|---|---|
| Home page text (headline, intro) | `content/<lang>/_index.md` |
| Bio | `content/<lang>/about.md` |
| Posts | `content/<lang>/posts/` |
| Menu and button labels | `i18n/en.toml`, `i18n/ru.toml`, `i18n/kk.toml` |
| Name spellings, email, LinkedIn, launch switches | `hugo.toml` |
| Design | `assets/css/main.css` (font: Google Sans, in `static/fonts/`) |

`<lang>` is `en`, `ru` or `kk`. English lives at the root of the site, Russian under `/ru/`, Kazakh under `/kk/`.

## Adding a post

1. Create three files with **the same file name** in `content/en/posts/`, `content/ru/posts/` and `content/kk/posts/`, for example `2026-10-20-bangkok-un-panel.md`. The same name is what links the three language versions.
2. Start each file like this:

   ```yaml
   ---
   title: "Post title in this language"
   date: 2026-10-20          # for archive posts, the original date
   slug: bangkok-un-panel    # same Latin slug in all three files
   categories: ["updates"]   # updates | archive | media
   description: "One sentence for Google and link previews."
   source: "https://..."     # optional: link to the original
   sourceName: "UNODA"       # optional: name shown for the link
   draft: false
   ---
   ```

3. Write the text below the second `---`, in the third person like the About page ("Yerdaulet Rakhmatulla presented…", then "he"). To embed a YouTube video, put `{{< youtube VIDEO_ID >}}` on its own line.
4. Commit to `main`. The site updates once the Actions run turns green.

## Launch checklist

The site starts in **review mode**: drafts are shown with a "Draft" badge, and search engines are asked not to index it. To launch:

1. In `hugo.toml`, set `buildDrafts = false` and, under `[params]`, `noindex = false`.
2. Set `draft: false` on each post you approve.
3. Custom domain (after buying `yerdauletrakhmatulla.com`): in **Settings → Pages → Custom domain**, enter the domain, then add the DNS records GitHub shows at your registrar and tick **Enforce HTTPS**.
4. Add the site to Google Search Console and submit `/sitemap.xml`.

## Preview on your own computer (optional)

Install Hugo 0.168 or later, then run `hugo server` in this folder and open the address it prints.

## Taking your content elsewhere

Everything is plain Markdown in `content/`. Any static site generator, or WordPress via an import plugin, can read it.
