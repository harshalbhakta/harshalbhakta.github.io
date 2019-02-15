---
layout: post
title:  "Github Pull Request Wishlist"
date:   2019-02-15 12:15:00 +0530
categories: [products-wishlist]
---

I love using Github's pull requests. It has a lot of great features and is really fun to use. But there are a few things that irritate me from time to time. Here are a few of them.

#### File filter - "Select None"

I often need to review big pull requests on <a href="https://github.com">Github</a>  that have
several files of various types (.m, .h, .csv, etc). Below is how the file filter currently works on Github. It allows you to select/deselect the type of file.

![File Filter - Before](/static/img/github-pull-request-1.jpg)

It really helpful when I want to hide files that I don't need in the current view. It allows me to focus on the files that really need my attention. I often end up hiding images, fonts and other non-code files to really get a sense of what's being implemented/changed in the code.

However, it becomes really frustating when I only want to review a single type of files. For example, I just want to see the ".m" files. To do this I need to go an uncheck all the other file types. It takes me around 10-15 clicks depending on the number of other file types.

A simple "Select None" option would have done wonders. I would be able to view just the ".m" files in 2 clicks. Below is a simple mock of how that would look.

![File Filter - After](/static/img/github-pull-request-2.jpg)

#### Image files

Github does not show a preview for images in the pull request. It simply show a message "Binary file not shown."

![Github Image Diff - Before](/static/img/github-pull-request-images-1.jpg)

They do let you see the actual images, but for that you need to click on the "Display the rich diff" button as shown in the image below.

![Github Image Diff - After](/static/img/github-pull-request-images-2.jpg)

Great! So there is a way to review image changes. But again it gets really frustrating when you have to review a lot of images. You need to click on the "Display the rich diff" button individually for each image.

I really like how <a href="https://gitlab.com">Gitlab</a> handles this. They show you the actual image diffs by default. No need to click on a button. It definitely makes sense to show image diffs by default. Whenever I am merging a pull request, if a image has been added or modified I definitely want to see what the image looks like before approving the pull request.

![Gitlab Image Diff](/static/img/github-pull-request-images-3.jpg)

#### Tree view for files

Currently Github only shows a list of the files that have changed. It does allow fuzzy search for files. But it doesn't help you see what has changed in the project at a glance.

![Github Changed Files List](/static/img/github-pull-request-tree-1.jpg)

Gitlab handles this in a much better way. They allow you to switch to the tree view to see what files were changed within your projects' directory structure.

![Gitlab Changed Files List](/static/img/github-pull-request-tree-2.jpg)