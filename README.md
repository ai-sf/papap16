# PAPAP
The portal of the Particle and Astroparticle Physics Autumn Programme

This is a website built with [Pelican](http://docs.getpelican.com/en) and my theme [materializepelican](https://github.com/gpasqualetti/materializepelican).

## Rebuilding

The generated site (HTML files, `images/`, `files/`, `theme/`) is in the repository root and is served by GitHub Pages from `gh-pages`. The Pelican source is in `src/`.

    cd src
    uvx --from pelican==4.9.1 --with markdown pelican content -s pelicanconf.py -o /tmp/papap-build
    cp /tmp/papap-build/*.html ..

Build into a temporary folder and copy only the HTML files over; do not point Pelican at the repository root. `images/`, `files/` and `theme/` are not regenerated.

The footer date is pinned in `src/pelicanconf.py` (`DATE`) so rebuilds do not change it.
