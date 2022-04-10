---
title: Discord Notes into MD
---
Status:
Tags: 
Links: [Obsidian Templater Plugin](out/obsidian-templater-plugin.md)
___
# Discord Notes into MD
<%* tR = tp.file.selection().replace(/\u200b/g, ''); %> <%* tR = tR.replace(/(\[\[|\]\]|\#)/g, '\`$1\`'); %> <%* tR = tR.replace(/(.*) —.*/g, '\n[' + '[$1]' + ']\n'); %> <%* tR = tR.replace(/ ?:\S*: ?/g, ''); %> <%* tR = tR.replace(/.*Twitter•.*/g, ''); %> <%* //tR = tR.replace(/@(\S*)/g, '[' + '[$1]' + ']'); %>
___
References:

Created:: 2021-06-27 22:55