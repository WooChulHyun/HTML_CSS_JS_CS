# Gitbook On GitHub

### GitBook

<hr>

For the Gitbook, there are two ways to create a Giitbook. One is a self-hosted service provided by https://gitbook.io, and other is a Gitbook project that creates static sites as open source.

Here we will create a Gitbook through the Github page.

### GitHub Page

<hr>

There are three main ways to host Github Pages.

1. The master branch of the repo named username.github.io.

2. Any repo with docs folder.

3. Any repo with gh-pages branch.

We will create a gitbook with second way, any repo with docs folder.

1. Create a repository.

<img src="https://i.postimg.cc/15XRkcsK/repoMain.png">

2. Connect local Git and github via `git clone` or `git init`.

3. On the settings page, activate the page with master branch.

<img src="https://i.postimg.cc/Gt5RLVdx/github-setting-page.png">

### GitHub installation

<hr>

First of all, because the Gitbook is based on node.js, node and npm should be installed in the system. npm is usually installed with node.js.

Now that you have npm installed on your system, install `gitbook-cli` with the following command:

I will display the branch name together. Just copy the code after \$.

```
(master) $ npm install -g gitbook-cli
```

When the installation is complete, run the gitbook init command from the project directory.

```
(master) $ gitbook init
```

After running, there will be README.md and SUMMARY.md files in the project directory.

```
// README.md
# Introduction


// SUMMARY.md
# Summary

* [Introduction](README.md)
```

You can build and upload directly using `gitbook build` command, but that can make it inconvenient to manage your project directory structure and files built.

So let's split the branches that make up the markdown and the files that we build into.

```
(master) $ git add .

(master) $ git commit -m "init gitbook"

(master) $ git branch docs
```

Now, we committed the files created by gitbook init, and created the docs branch.

This docs branch will be the branch we will use to write down the markdown files, and the existing master branch will be used to build the gitbook and host the built-in html files.

Before we checkout, let's build it once. (You do not have to follow)

```
(master) $ gitbook build
```

After you build, you will have a \_book directory.

```
_book/  <----
  gitbook/
  index.html
  search_index.json
README.md
SUMMARY.md
```
