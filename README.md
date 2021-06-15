# Psychoinformatics.de Website

This repo has all of the sources and assets for the website of the
Psychoinformatics Lab at the Research Center in Jülich
(https://www.psychoinformatics.de).

Pages are generated using [Pelican](https://blog.getpelican.com).

Content is written predominantly in HTML and [reStructuredText](https://docutils.sourceforge.io/docs/ref/rst/restructuredtext.html).
Pelican is flexible like that.

## Building
To setup the build environment:

* clone the repo and pull submodules
  ```
  git clone https://github.com/psychoinformatics-de/psychoinformatics-www.git
  cd psychoinformatics-www
  git submodule update --init --recursive
  ```
* setup and activate a virtualenv
  ```
  python3 -m venv ~/.venvs/pelican
  source ~/.venvs/pelican/bin/activate
  ```
* install Pelican and dependencies
  ```
  pip3 install pelican invoke beautifulsoup4
  ```
* run the development server
  ```
  pelican --autoreload --listen
  ```
* point your browser to `http://127.0.0.1:8000`.

Your copy of the docs will be served locally at that address, and any changes
will automatically trigger a rebuild.

## Publishing
GitHub Actions is used to build and test all PRs. When commits make it to the
`master` branch, they are built, the results saved in the `gh-pages` branch,
and then hosted by GitHub Pages.

## Notes
Props to Alexandre Vicenzi for making and sharing his [Flex theme](https://github.com/alexandrevicenzi/Flex/).
Though this site's theme has evolved much since then, his theme served as a very
productive starting point.

## Licence
When in doubt, the license of all content/artwork is [CC-BY-SA-4.0](https://creativecommons.org/licenses/by-sa/4.0/legalcode),
[SIL OFL 1.1](https://scripts.sil.org/cms/scripts/page.php?item_id=OFL_web) for
fonts, and [MIT](https://opensource.org/licenses/MIT) for all code. Please see
the `content/pages/copyright.rst` page for a more granular, Debian-style
declaration of files and their licenses.
