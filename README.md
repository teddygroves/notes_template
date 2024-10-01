# Template for a static website using Sphinx and GitHub Pages

## Instructions

### 1. Fork repository

- now you are already publish the site which looks identical to the template site
 (see it here)
- jump to step 5 to do that directly.

### 2. Open in GitHub Codespaces

- go to [github.com/codespaces](https://github.com/codespaces)
- create a new codespace using the forked repository

### 3. Edit files

- update in `conf.py` at least the author, project and copyright information at the top
- write something about you in `about.md`
- write articles in `folder_topic/article_topic.md`
- update the `index.md` file to include new files
- use [pandoc](https://pandoc.org/try/) to convert your previous files into markdown or
  reStructuredText

### 4. Build the site locally

> Have look at `.github/workflows/build-website.yaml` to see how the site is built.

- Open a terminal (GitHub Codespaces)
- install required packages from [`requirements.txt`](requirements.txt):
  ```bash
  pip install -r requirements.txt
  ```
- build the site (you could set an alias if you want):
  ```bash
  sphinx-build -n -W --keep-going -b html ./ ./_build/
  ```
- open the site in a browser:
  - install "Live Preview" extension in Visual Studio Code
  - open the `_build/index.html` file in the browser

### 5. Publish the site

Follow 
[these instructions](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) 
to publish the website using GitHub Pages.

- Select the `gh-pages` branch as the source for the GitHub Pages site (currently step 7)
