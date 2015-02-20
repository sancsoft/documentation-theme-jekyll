---
title: Getting started
permalink: /getting_started/
---

Although you can get started with this theme by simply gutting the existing jekyll-docs theme and replacing it with your own content and values, that's not how I intended this theme to be used. I'm assuming that you may have multiple projects that you'll be publishing, and that you want to use the theme as a template for each project. As such, you can simply leave the jekyll-doc content as is. The following steps explain how to create a new project for the theme.

{{alertprimary}} In these instructions, to simplify things, I'm assuming your project's name is "ACME." Customize these instructions to swap in your real project name.{{end}}

To publish a new project with the jekyll-doc theme, do the following:

## Clone the jekyll-doc repository

1. `mkdir acme`
2. `cd acme`
3. git clone `https://github.com/tomjohnson1492/jekyll-doc.git .`

## Copy the blankproject folder inside projects

1. Inside the projects folder, copy the "blankproject" folder and paste it (duplicating it). Don't just rename it or it messes up future `git pull` requests. Once you copy the blankproject folder, change the name to your project's name -- in this case, I'll assume "acme" is your project name.

## Customize the configuration
1. In the projects/acme/configurations folder, rename config_blankproject.yml to config_acme.yml.
2. Open config_acme.yml and customize all the values. The file contains notes for each part you need to customize. Basically everywhere you see "blankproject", change it to your project's name. 

## Customize the pages
1. Open the pages folder inside acme. Here is where you add your pages. Leave the reuse and drafts folders there. You add links, callouts, and notes in those reuse folders, so you can easily include them into your pages.

## Customize data

1. In the data folder, nav.yml contains the navigation for the sidebar and topnav. The current values are for the jekyll-doc theme, so you can see some example formatting. Change these values with your own page titles and URLs. Spacing matters in YML syntax.
2. In data/options.yml, open this file and customize the values. Options contains various settings for Disqus, Google Analytics, and more.

## Set the homepage ID

1. In the configuration file, you set a homepage ID value. In projects/acme/pages, open home.md and change the ID to the homepage_id value you set in the configuration file.

## Customize the build script

1. In the root directory, rename blankproject.sh to acme.sh.
2. Open acme.sh (in a text editor) and change all instances of `blankproject` to `acme`.

## Build your site

`cd` to your project folder.
Type `. acme.sh`.

{{calloutprimary}} You can run `git pull` to get updates to the theme. The updates will not overwrite your other project files that you have added. For example, the updates from the theme won't overwrite anything in content/acme. However, if you change content in content/jekyll-doc, the updates will overwrite that folder. In short, if your cloned repo has files A,B,C, D, E, F, and the repo has only files A, B, C, then only A, B, C, will be overwritten when you pull new updates. I won't add any new subfolders under projects other than jekyll-doc.{{end}}