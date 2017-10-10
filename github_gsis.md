Getting started with GitHub
========================================================
author: Lucas Nell
date: 11 Oct 2017
autosize: true
font-family: Helvetica Neue
css: custom.css



<small>`lucasnell.com/github_gsis`</small>




Why use git and GitHub?
========================================================
left: 50%

<img src="http://phdcomics.com/comics/archive/phd101212s.gif">

***

- Collaborating with a team
- Sharing code with strangers
- Tracing and avoiding horrible mistakes


git and GitHub overview
========================================================

<img src="img/github_overview.svg" height="600" width="600">



Today's goals
========================================================

1. Tell git who you are
2. Connect securely to GitHub
3. Create a test repository
4. Clone, commit, and push your repository




Prerequisites
========================================================

- git
- GitHub account
- R and RStudio



Telling git who you are
========================================================

In RStudio, `Tools` > `Shell...`

Set global defaults for name and email.
Make sure the email below is the one you use for your GitHub account


```bash
git config --global user.name 'John Doe'
git config --global user.email 'john@doe.com'
```

Checking global git options
========================================================
title: false
Output from this command...

```bash
git config --global --list
```
... should include this:

```bash
user.name=John Doe
user.email=john@doe.com
```


Connecting securely to GitHub using SSH
========================================================

First, check if you already have an SSH key

From R:

```r
file.exists("~/.ssh/id_rsa.pub")
# Windows:
# file.exists("C:/Users/USERNAME/.ssh/id_rsa")
```

If `FALSE`, you need to make a public key first...

Making and viewing key
==========

<img src="http://r-pkgs.had.co.nz/screenshots/git-config-2.png" height="500" width="500">
<small>from `http://r-pkgs.had.co.nz/git.html#git-init`</small>

Adding key to GitHub
====================

Login to `github.com` in web browser

Go to `https://github.com/settings/ssh`

<img src="img/new_ssh.png" height="50" width="171">

Enter a descriptive title (e.g., "Personal MacBook Pro")

Paste your key into the "Key" box

<img src="img/add_ssh.png" height="50" width="163">


Initiate new repository
========================================================

<div>
From <code>github.com</code>:
<img src="img/new_repo.png" height="50" width="200" style="vertical-align: middle">
</div>

From profile page:

<img src="img/new_repo2.png" height="150" width="852">


Describe and create new repository
========================================================

<img src="img/new_repo_info.png" height="640" width="776">



Clone repository in RStudio
========================================================

`File` > `New Project` > `Version Control` > `Git`

<img src="img/clone_repo.png" height="545" width="766">


Make local changes
========================================================

If just using a test repo, edit the `README.md` file and save changes.

If wanting to move a directory over to GitHub, copy those files into the 
new repository's folder


Commit and Push
========================================================


- Under "Git" tab, checked "Staged" for file(s) that you changed or added
- Hit "Commit"
- Add useful commit message
- Hit "Commit" again

If the above works, then you're successfully using GitHub through RStudio




Additional resources
========================================================
class: smaller

- Source of info for much of this presentation: `happygitwithr.com`
- For connecting to GitHub using SSH: `r-pkgs.had.co.nz/git.html`
- Simple command line guide: `rogerdudler.github.io/git-guide`
- GitHub Education (for free private repos): `education.github.com`
- Recommended git clients (RStudio isn't great to use long-term)
    - GitKraken: `gitkraken.com`
    - SourceTree: `sourcetreeapp.com`
- If you can't connect to GitHub through RStudio, use the command line:
`happygitwithr.com/push-pull-github`


> This presentation is available at `lucasnell.com/github_gsis`
