---
layout: post
title:  "Jekyll commands and configuration files"
date:   2024-01-14 11:50:33 +0900
categories: jekyll update
permalink: 
commonmark:
  options: ["FOOTNOTES"]
  extensions: ["strikethrough", "autolink", "table"]
---
# 1. Commands



# Set up
- `bundle install` | install dependencies which are configurd in Gemfile ?
- `bundle exec jekyll serve` | Run server with dependancy modules.
- `bundle exec jekyll build` |
- `jekyll serve` | run local server...
    - options :
        - `--draft` : render postings located in `_drafts` directory.



# Pages

- how to make a page :
    1. create md file on root directory.(but you could move this file any directory, and that dir name would be included when you access the page, router concept.)
    2. make layout as "page" in frontmatter

# Permalinks : permanant link or URL of a page.
- Write `permalink: "/my-new-url/"` on frontmatter, Permalink is used primaliry over field of `categories`.
- Use variables defined in frontmatter, try this -->  `permalink: /:day/:year/:title.hello-World`
- In order to use a variable, try this --> `/:(variable name)`




# 2. Files
- Gemfile |
- _config.yml |
- _posts (dir) |


# Hosting through github
1. set baseurl as github repo name.
2. create a repo in github and sync
  1. `git init`
  2. `git checkout -b gh-pages(<=branch name)` | checkout with a branch named as 'gh-pages'
  3. `git status` | checking git status
  4. `git add` | adding all files which are untracked yet.
  5. `git commit -m "initial commit"` | Do first commit.
  6. `git remote add origin  (git repo address)`| linking a repository which is made for hosting this blog.
  7. `git push origin gh-pages(<=branch name)` | push all files which is committed by user.