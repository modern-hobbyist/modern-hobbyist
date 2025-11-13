---
title: How I made this Wiki
layout: home
nav_order: last
---
# How I Made This Wiki

This wiki is built using [Jekyll](https://jekyllrb.com/) with the [just-the-docs](https://github.com/just-the-docs/just-the-docs) theme for a clean and easy-to-navigate static site. It’s hosted on [GitHub Pages](https://pages.github.com/), which makes deployment seamless and automatic.

## My Setup

I use **[Obsidian](https://obsidian.md/)** as my primary writing and note-taking tool. This allows me to treat the wiki just like any other set of notes, making it easy to update and expand over time.

To ensure my changes are automatically committed and deployed, I use the **[Obsidian Git plugin](https://github.com/Vinzent03/obsidian-git)**, which commits changes every 10 minutes if there are any updates. This means:

1. I write and edit directly in Obsidian.
2. The Obsidian Git plugin commits changes automatically to GitHub.
3. GitHub Pages automatically deploys the latest version of the site.

## Why This Workflow?

- **Seamless Editing:** Since I already use Obsidian for note-taking, maintaining this wiki feels effortless.
- **Automated Deployment:** No need to manually push changes or trigger builds—everything happens in the background.
- **Version Control:** Every edit is tracked via Git, making it easy to roll back if needed.
- **Accessible Anywhere:** Because it's hosted on GitHub Pages, I can view and share my knowledge base from anywhere.
- It's Free. $0 free. Nada. Zilch

## Downsides

- **Security**: I don't have GitHub Pro, so I am unable to make the repository that this Wiki is build from `Private`. I am *mostly* ok with that, I just have to make sure not to put any sensitive information in the documentation, which isn't usually a problem. 
- **Styling**: Styling can be a pain when going for a more custom look on a page, but markdown can get you pretty far most of the time.
- **Obsidian Links**: One of the most powerful parts of Obsidian is the `Obsidian Links`, which allow you to quickly link to another document with `[[Another Document]]` notation. This breaks when building your markdown as a Jekyll Site, since it's an Obsidian specific feature. 

## How You Can Do It Too

If you want to set up something similar, here’s a rough outline of what you need:

2. **Set Up a GitHub Repository** – Store your wiki files in a public or private repo.
3. **Install Jekyll and Just-the-Docs** – Follow the [Jekyll installation guide](https://jekyllrb.com/docs/installation/) and configure the `just-the-docs` theme.
4. **Enable GitHub Pages** – In your repo settings, set GitHub Pages to build from your main branch.
5. **Use Obsidian for Editing** – Write and organize your content just like regular notes.
6. **Install the Obsidian Git Plugin** – Configure it to commit and push changes automatically.

---

This setup allows me to focus on documenting my learning process without worrying about deployment or version control. If you have questions or want to tweak this workflow for your own use, feel free to reach out!

Thanks!

Charlie Steenhagen  
[Modern Hobbyist](https://www.youtube.com/@ModernHobbyist)

----

