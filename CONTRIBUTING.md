# Contributing to osgeo.id

Anyone in the Indonesian open source geospatial community can write for this
site. You keep the byline, and your name is recorded permanently in the
repository's history.

*Bahasa Indonesia: lihat [bagian bawah](#panduan-singkat-bahasa-indonesia).*

## What we publish

Event reports, tutorials, project updates, conference notes, community news —
anything useful to people doing open source geospatial work in Indonesia.

English and Bahasa Indonesia are both welcome. Write in whichever comes more
naturally; you do not need to provide both. If you write in one and someone
later translates it, both of you are credited.

## The short version

1. Fork <https://github.com/osgeoid/osgeoid.github.io>
2. Create a folder: `posts/YYYY-MM-DD-short-title/` (or `id/posts/…` for a
   post in Bahasa Indonesia)
3. Add `index.qmd` inside it, using the template below
4. Put any images in that same folder and reference them by filename
5. Open a pull request

You do **not** need to install Quarto or build the site. A maintainer will
render it. If the build breaks, we will tell you what to fix.

## Post template

Copy this into `posts/YYYY-MM-DD-short-title/index.qmd`:

```yaml
---
title: "Your title"
description: |
  One or two sentences. This shows on the News listing and in link previews.
author:
  - name: Your Name
    url: https://github.com/yourusername      # optional
    affiliation: Your university or org       # optional
date: 2026-09-04
categories: [tutorial, qgis]
---

Write here in Markdown.

## A heading

Normal paragraphs. **Bold**, *italic*, [links](https://osgeo.id).

![Caption for the image](my-screenshot.png)
```

### Front matter fields

| Field | Required | Notes |
|---|---|---|
| `title` | yes | Sentence case. No trailing period. |
| `description` | yes | 1–2 sentences; shown on the listing and in social previews. |
| `author` | yes | See multiple authors below. |
| `date` | yes | `YYYY-MM-DD`. The date you wrote it. |
| `categories` | recommended | Lowercase. Reuse existing ones where they fit. |

### Multiple authors

List them; everyone is credited, in order:

```yaml
author:
  - name: First Author
    url: https://github.com/first
  - name: Second Author
    affiliation: Universitas Diponegoro
```

### Existing categories

Reuse these where they fit rather than inventing near-duplicates:

`tutorial` · `event-report` · `announcement` · `community` · `qgis` ·
`postgis` · `openstreetmap` · `remote-sensing` · `foss4g` · `geo-for-all`

## Not comfortable with git?

That is fine, and it is not a barrier to being published here.

Write the post however you normally write — a document, an email, a message —
and send it to the
[mailing list](https://lists.osgeo.org/mailman/listinfo/indonesia) or the
[Telegram group](https://t.me/osgeoid). Someone will help you turn it into a
pull request. **The byline stays yours**; the person who helps is a helper, not
a co-author.

## How attribution works here

Three layers, all public:

1. **On the page.** The `author` field renders under the post title and on the
   News listing.
2. **In git.** Your commit carries your name and GitHub account. `git log` and
   the repository's contributor graph show it permanently. This is why we ask
   you to open the pull request yourself when you can — it is what puts your
   account on the record.
3. **On every page.** *Edit this page*, *View source*, and *Report an issue*
   links point at the exact source file on GitHub, so any reader can see the
   full authorship and change history of what they are reading.

Corrections and improvements to someone else's post are welcome — open a pull
request. The original author keeps the byline; you appear in the history as
the person who made that change.

## Editing an existing page

Every page on the site has an **Edit this page** link in its sidebar. It opens
that file directly in GitHub's editor and will offer to create the pull request
for you. For typos and small corrections this is the entire workflow — no fork,
no clone.

## Reviewing and publishing

A maintainer reviews for accuracy, checks that the site builds, and merges.
We are not fussy about prose style. Things that will get comments:

- factual errors, especially about software behaviour or event details
- missing attribution for images, data, or text you did not create
- anything that conflicts with the
  [OSGeo Code of Conduct](https://www.osgeo.org/code_of_conduct/)

Merged posts appear on <https://osgeo.id/news.html> once the site is rebuilt.

## Building locally (optional)

Only needed if you want to preview your own work:

```sh
# install Quarto from https://quarto.org/docs/get-started/  (built with 1.9.x)
quarto preview          # live preview at localhost
quarto render           # writes docs/
```

`docs/` is the published output and is committed to the repository. If you
render, include the resulting `docs/` changes in your pull request; if you
would rather not, leave it and a maintainer will render for you.

## Licence

By contributing you agree your work is published under the same terms as the
rest of the site, and that you have the right to publish any images or data you
include.

---

## Panduan singkat (Bahasa Indonesia)

Siapa pun boleh menulis untuk situs ini, dan nama Anda tetap tercantum sebagai
penulis.

1. Fork <https://github.com/osgeoid/osgeoid.github.io>
2. Buat folder `id/posts/YYYY-MM-DD-judul-singkat/`
3. Tambahkan `index.qmd` memakai templat di atas
4. Letakkan gambar di folder yang sama
5. Buka pull request

Anda **tidak perlu** memasang Quarto. Maintainer yang akan merender situsnya.

**Belum terbiasa dengan git?** Tidak masalah. Tulis saja seperti biasa, lalu
kirim ke [milis](https://lists.osgeo.org/mailman/listinfo/indonesia) atau
[grup Telegram](https://t.me/osgeoid). Akan ada yang membantu memasukkannya, dan
nama Anda tetap sebagai penulis.

Setiap halaman punya tautan **Edit this page** untuk perbaikan kecil — cukup
klik, sunting di GitHub, dan pull request dibuatkan otomatis.
