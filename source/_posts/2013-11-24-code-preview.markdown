---
layout: post
title: "How I fixed Octopress installing issues"
date: 2013-11-24 14:15:27 -0500
comments: true
categories: code, Octopress
---
In this post I will talk about the installing issues I met and how I fixed them when I tried to install Octopress from the official Octopress website.

1.No such directory

It's easy, just change the path. 
```bash
cd octopress
```

<!--more-->

2.Github Page 404

Because you don't host the Github page correctly，previously Github use *username.github.com*，but now it's *username.github.io*. If you want your own domain，change both A record and CNAME.

3.I met this when I configured git and used ```rake deploy```

```bash
! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'https://github.com/stevenlordiam/stevenlordiam.github.io.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Merge the remote changes (e.g. 'git pull')
hint: before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```
Many people asked the same question on stackoverflow, I tried to Google but none can fix this. Some said it's SSH problem, some say it's version collision of git. Finally I fixed this problem by this step: 
master branch is in ```octopress/_depoly```, pull after going into this folder and come back to octopress folder and deploy. It works!

```bash
cd octopress/_deploy
git pull origin master
cd ..
rake deploy
```

The blog is almost set. Next step：

~~-Add Tag Cloud~~

-Make the webpage load faster

-Mobile page optimization


