Status: 
Tags: 
Links: [Obsidian MOC](Obsidian%20MOC.md)
___
# Quartz (Graph Website Deployer)
[FAQ](https://quartz.jzhao.xyz/notes/troubleshooting/#can-i-publish-only-a-subset-of-my-pages)

[Configuration](https://quartz.jzhao.xyz/notes/config/)

[Excluding pages](https://quartz.jzhao.xyz/notes/ignore-notes/)
- .gitignore

https://github.com/ozntel/oz-image-in-editor-obsidian/releases/tag/1.4.9
- plugin has commands to convert Wikilinks to Markdown links and vice-versa in all files within the vault or only in the active file. This is amazing for switching _to_ wikilinks for **seeing transclusions in editor mode using this plugin**, or for people trying to convert to Markdown links for interoperability with other programs like static site generators.
- 2021.09.04

[Deploying](https://quartz.jzhao.xyz/notes/hosting/)

[Changing URLs](https://quartz.jzhao.xyz/custom-Domain/)

```shell
# Navigate to Quartz folder
cd <path-to-quartz>

# Commit all changes
git add .
git commit -m "message describing changes"

# Push to GitHub to update site
git push origin hugo
```

[Customizing Webpage](https://quartz.jzhao.xyz/notes/config/)
___
# Backlinks
```dataview
list from [[Quartz (Graph Website Deployer)]] AND !outgoing([[Quartz (Graph Website Deployer)]])
```
___
References:

Created:: 2022-01-20 15:32
