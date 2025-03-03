# Airtable to Markdown

This demo shows how turn an [Airtable](https://www.airtable.com/) database into Markdown files using [Hugo](https://gohugo.io/).

Using a single template, Hugo will batch add any new tags you specify to your data and format the front matter inside each Markdown file to work well with [Obsidian](https://obsidian.md/). 

For a deep dive on how this project came about and how it works, read [Using Hugo to turn an Airtable database into Markdown files for Obsidian](https://harrycresswell.com/writing/using-hugo-to-turn-airtable-data-into-markdown-files-for-obsidian/).

**Note**: This project doesn’t create a website like most Hugo projects, it simply generates Markdown files for use in Obsidian.

## Prerequisites

You will need [Hugo](https://gohugo.io/) version 0.126.0 or higher installed locally.

## Installation

Clone this repository:

```
git clone https://github.com/harrycresswell/content-adapters.git
```

## Local development

To start a local development server at at https://localhost:1313/ run:

```
hugo server
```

## Getting started

Once you have a Hugo installed and a copy of this repository on your local machine, first you need to [prepare your Airtable data for Hugo](https://harrycresswell.com/writing/using-hugo-to-turn-airtable-data-into-markdown-files-for-obsidian/#preparing-the-data-for-hugo).

Next, open `layouts/index.html` and complete the following steps:

1. Update the value of `$path` from `data/nicesites.json` to `data/the-name-of-your-file.json`.
2. Find `$newTags` and replace *references* with the name of the extra tag you want to include in your markdown files. Read [Add new tags to each slice](https://harrycresswell.com/writing/using-hugo-to-turn-airtable-data-into-markdown-files-for-obsidian/#add-new-tags-to-each-slice) for more on this.
3. Locate `$filename` and update the destination folder name from *nicesites* to whatever folder you wish to output your Markdown files to within the /public folder.


## Generating Markdown files

Whe your ready to generate your Markdown files, head to the root of the project, then run:

```
hugo --cleanDestinationDir
```

This will clean the `/public` folder and regenerate your Markdown files.

## Licence

MIT