# osgeoid.github.io

Website of **OSGeo Indonesia**, the Indonesian local chapter of the
[Open Source Geospatial Foundation](https://www.osgeo.org/).

Live at **[osgeo.id](https://osgeo.id)** · bilingual English / Bahasa Indonesia.

## Community

| Channel | Where |
|---|---|
| Mailing list | [lists.osgeo.org/mailman/listinfo/indonesia](https://lists.osgeo.org/mailman/listinfo/indonesia) |
| Wiki | [wiki.osgeo.org/wiki/OSGeoID](https://wiki.osgeo.org/wiki/OSGeoID) |
| Telegram | [t.me/osgeoid](https://t.me/osgeoid) |
| Twitter/X | [@osgeoid](https://twitter.com/osgeoid) |

## How the site is built

[Quarto](https://quarto.org/) renders the `.qmd` sources to `docs/`, which is
what GitHub Pages serves. The rendered output is committed to the repo — there
is no CI build step, so **you must render before you push**.

```
index.qmd  about.qmd  projects.qmd  community.qmd  events.qmd  contact.qmd   # English
id/*.qmd                                                                     # Bahasa Indonesia
_quarto.yml          site config, navbar, footer
custom.scss          theme (cosmo + chapter overrides)
lang-switcher.html   geo-redirect + Indonesian navbar labels
docs/                rendered site — GitHub Pages source
```

### Editing

1. Install [Quarto](https://quarto.org/docs/get-started/) (built with 1.9.x).
2. Edit the `.qmd` files. **Every English page has an Indonesian counterpart
   under `id/` — change both.**
3. Preview locally:
   ```sh
   quarto preview
   ```
4. Render and commit:
   ```sh
   quarto render
   git add -A && git commit -m ":ok_hand: IMPROVE: ..." && git push
   ```

Pages redeploys from `master` `/docs` on push.

### CNAME

`CNAME` at the repo root is the source of truth for the custom domain. It is
declared under `project.resources` in `_quarto.yml` so `quarto render` copies it
into `docs/` — without that, Quarto cleans the output directory, deletes
`docs/CNAME`, and the custom domain gets dropped on the next deploy.

## Git commit standard (Emoji-Log)

Following [Emoji-Log](https://github.com/ahmadawais/Emoji-Log). Write commit
messages in the imperative, as if giving an order.

- `:tada: INITIAL:`
- `:package: NEW:`
- `:ok_hand: IMPROVE:`
- `:bug: FIX:`
- `:book: DOC:`
- `:rocket: RELEASE:`
- `:white_check_mark: TEST:`

See also [gitmoji](https://gitmoji.carloscuesta.me/).

## History

The chapter's first website (2019) was a Hugo site derived from
[OSGeo US](https://github.com/OSGeo-US/OSGeo-US.github.io). It is preserved on
the [`archive/hugo-2019`](../../tree/archive/hugo-2019) branch.
