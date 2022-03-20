# markhor-action

For the static site generator, see [tufteddeer/markhor](https://github.com/tufteddeer/markhor).

## Example

The following workflow will generate static html from the sources in your repository and publish them using GitHub pages.

```yaml
on: [push]

jobs:
  hello_world_job:
    runs-on: ubuntu-latest
    name: Generate site
    steps:
      - name: Checkout repository
        uses: actions/checkout@v3
      - name: Generate site
        uses: tufteddeer/markhor-action@v0.2.0
      - name: Deploy to GitHub Pages
        uses: JamesIves/github-pages-deploy-action@v4.2.5
        with:
          branch: gh-pages
          folder: out
```