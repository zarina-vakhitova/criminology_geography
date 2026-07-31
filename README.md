# The geography of criminological knowledge — companion visualisations

Three interactive visualisations accompanying a study of who writes criminology, which
places it studies, and how both have changed. Built from 38,746 articles published between
2000 and 2025 in the 74 journals listed solely under Criminology & Penology in the 2024
Journal Citation Reports.

**[View the visualisations &rarr;](https://zarina-vakhitova.github.io/criminology_geography/)**

## The files

| File | What it shows |
|---|---|
| `index.html` | Menu page linking to the three visualisations, with thumbnails drawn from the real data |
| `criminology_focus_map.html` | World map shaded by how many articles study each country. Select a country for its count, share and rank |
| `criminology_decoupling.html` | Animated chart tracing four world regions from 2000 to 2025, comparing each one's share of the world economy with its share of criminology authorship |
| `criminology_country_paths.html` | The same comparison for individual countries, with a dropdown covering the 33 countries that have at least 100 articles in the corpus |

Each file is self-contained: the data is embedded, there is no build step, no server-side
code and nothing to install. Sizes run from 11 KB to 162 KB; the map is the largest because
it carries its own country boundaries.

## Publishing the pages

Keep all four files in the same folder — the menu links to the others by relative path.

To publish with GitHub Pages: commit the files, then in the repository go to
**Settings → Pages**, set *Source* to "Deploy from a branch", and choose your branch and
either the repository root or a `/docs` folder. The site appears at
<https://zarina-vakhitova.github.io/criminology_geography/> within a few minutes, landing on
`index.html`.

Two things to know. Uploading an HTML file to GitHub does not by itself make it viewable —
without Pages enabled, clicking the file shows its source. And Pages on a private repository
requires a paid plan; public repositories get it free.

The pages load Fraunces and IBM Plex from Google Fonts, the only external request they make.
Without a connection they render correctly in fallback typefaces.

## What the data is

**Corpus.** Every article published 2000–2025 in the 74 sole-category Criminology & Penology
journals, indexed in Web of Science. Journals cross-listed with other categories are
excluded, as are non-article document types.

**Authorship** is attributed to the country of the corresponding author. Where a journal or
region is described as holding a share of authorship, that is the share of corresponding
authors, not of all authors.

**Research focus** (the map) counts an article once for the country it studies, identified
from its title and abstract by a dictionary validated against independent human coding.
Articles with no particular country focus, or comparing several, are not mapped. Regional
subjects such as "the European Union" are excluded. Of 23,619 country-focused articles,
23,021 fall in countries the map can render; fifteen small states and territories, among
them Hong Kong and Singapore, are in the data but too small to draw at world scale.

**Economic shares** come from the World Bank's World Development Indicators, GDP at
purchasing power parity, each region's or country's total as a share of the world figure.
Countries appearing in the corpus hold about 96% of world GDP, so these shares do not sum
to 100.

**The country pages cover 33 countries** — those with at least 100 articles, together 95.9%
of all authorship. Countries below that threshold are omitted because a year in which one
publishes two articles rather than none would swing its share wildly; the median country in
the corpus has thirteen articles across the whole period. The authorship path is smoothed
with a three-year average for the same reason, while the reported count and share for the
selected year are unsmoothed.

## Reading the country chart

Both axes rescale to the country shown, and always share a single scale, so the parity line
stays at forty-five degrees. This keeps small countries legible while preserving the meaning
of distance from the line: a path below it means a country publishes less criminology than
its economic size would suggest. The ratio reported in the panel — criminological share
divided by economic share — is comparable across countries regardless of the axis scale.

## Two things worth reading carefully

**Grey on the map means no articles, not missing data.** A grey country is one that no
article in these 74 journals, across twenty-six years, takes as its subject. That is a
statement about this literature, not about whether research on those places exists
elsewhere.

**Part of the Anglosphere's apparent decline is a coverage effect.** Web of Science added
many non-core journals to its index over this period. Within the eleven journals indexed
continuously since 2000, the Anglosphere share of authorship falls only from 95% to 85%,
against 95% to 67% across the growing journal set. The decoupling page notes this; it
matters for how the downward trend should be read.

## Licence and reuse

The visualisations publish **journal-level and country-level aggregates only**. The
underlying bibliographic records are licensed from Clarivate and are not redistributed
here.

Country boundaries are from the [world.geo.json](https://github.com/johan/world.geo.json)
public-domain dataset, simplified and embedded.

## Citation

Add the citation and DOI for the article once available, in this file and in the third
"about" panel on `index.html`.
