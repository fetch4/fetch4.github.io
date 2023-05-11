# FETCH₄ Website Source

[![Deploy Hugo site to Pages](https://github.com/fetch4/fetch4.github.io/actions/workflows/hugo.yaml/badge.svg)](https://github.com/fetch4/fetch4.github.io/actions/workflows/hugo.yaml)

This repo contains the source code for the FETCH₄ website.
The site uses the [Hugo](https://gohugo.io/) framework.
The source files are written in markdown.
A [GitHub workflow](https://github.com/fet/fetch4.github.io/blob/master/.github/workflows/hugo.yaml) is configured to automatically build and deploy the website to <https://fetch4.github.io/> whenever the `master` branch of this repo is updated.

## Instructions for updating this site

To update the site, you need to change the source files on the `master` branch of this repository.
There are two ways to do this.

### Easy Way: Edit on GitHub

You can edit the source files directly on GitHub from your browser.
To do this, navigate to the `content` folder and click the edit button (little pencil symbol).
Make your changes in the editor.
When you are done, you can either "Commit directly to the `master` branch" or "Create a new branch for this commit and start a pull request".
A direct commit is appropriate for a minor change.
A pull request is best if you want your changes to be reviewed and approved by the rest of the team.
This method only allows you to update one page at a time.

### Hard Way: Edit Locally

You can also clone this repository, make local changes, and then push them.
This is better for larger changes that involve multiple files and may need debugging.

Basic git workflow
```bash
git clone git@github.com:fetch4/fetch4.github.io.git
cd fetch4.github.io
# edit files with your text editor
git add [new or modified files]
git commit -m '<your commit message>'
git push origin master
```

If you want to make a large change, it may be best to discuss it first via pull request.
In that case you would want to create a new branch, push your branch to GitHub, and open a PR.
The GitHub docs on [creating a pull request](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request) are a useful reference here.

You can also build the website locally on your own computer.
This can be useful for debugging.
To do this, you need to first [Install Hugo](https://gohugo.io/getting-started/quick-start/).
You can then use the Hugo command line tools to do stuff like
```bash
hugo new content/<name of your page>.md # create a new page
hugo server -D # serve the website on http://localhost:1313/.
```
