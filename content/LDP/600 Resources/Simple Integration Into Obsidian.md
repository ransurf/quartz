---
aliases: LDP within Obsidian
tags: [info, alignment]
---
[[LDP/000 Inbox/00 ❗ Readme]]
## Simple Integration Into Obsidian
### Why Obsidian?
Obsidian is an bare-bones markdown text editor, but with super powers. With community plugins, you can truly build a system for yourself, expanding functionality far beyond it's initial function.

Your documents are also all locally stored on your disk. There are no dependence on a cloud proprietary software, the only dependence is you (and your computer). This is truly yours to work with. Everything is yours; just yours.

And that just felt right.

### Some Assumptions
I will assume that you are familiar with the basics of Obsidian. If not, please press F1 and take a look at the manual. Also consider some Youtube videos. The official [Obsidian Discord](https://discord.gg/xSaj5Cc5GZ) is also a good place to ask for help. Moving on!

### Demo
A sparse example of LDP's organization is already set up. You should have noticed that the following organization.

>  📁`100 Projects` > 📁`Setup` = [[LDP/100 Projects/Setup/00 🧰 Setup]]
> 
> 📁`200 Disciplines` > 📁`200 🎀 Well-being (EXAMPLE)` = [[210 🎀 Well-being (EXAMPLE)]]

Projects and Disciplines are decoupled. Frontmatter tags will be used to link projects to disciplines.

### Folder Naming
The folders on the left have a numbered prefix. This is a concept borrowed from the Dewey-Decimal System, where libraries organize their books by numbers. In our case, it organizes our folders. 

Notice how `Inbox` comes first, not `Archive` when sorted alphabetically. This can also be used to sticky notes to the top of a folder, like [[210 🎀 Well-being (EXAMPLE)]].

It also allows for quick-lookup. You always know disciplines are prefixed 200, so if you ever need to reference a discipline's [[#Dashboards|dashboard]], you only need to start typing `[[2` and autocomplete will help you finish the rest.

![[LDP/600 Resources/Pasted image 20211028173232.png]]

Not all folders should follow this system. I recommend you do this for Disciplines so your most important one, your [[LDP/600 Resources/Ikigai]] Discipline, pushed to the top. 

I do not recommend this for Projects ordering doesn't matter.

> tl;dr - Dewey-Decimal System for when grouping and ordering matters.

### Dashboards
See [[LDP/600 Resources/Dashboards]].

### Obsidian Plugins
If there's some extra functionality you want, it probably exists. Here are some important plugins I consider core. These plugins have been included for this demo and can be installed through the Community Plugins panel under Settings.
- [Obsidian Tasks](https://github.com/schemar/obsidian-tasks) for managing all your tasks
- [Obsidian Dataview](https://github.com/blacksmithgu/obsidian-dataview) for aggregating information for dashboards
- [obsidian-calendar-plugin](https://github.com/liamcain/obsidian-calendar-plugin) for visual routine alignment
- [Periodic Notes](https://github.com/liamcain/obsidian-periodic-notes) for routine alignment
- [Templater](https://github.com/SilentVoid13/Templater) to reduce friction and quickly set up new disciplines, projects, tasks, alignment, etc (which reduces friction)
- [Natural Language Dates in Obsidian](https://github.com/argenos/nldates-obsidian) for inserting dates in natural English

There are many, many other plugins that you might find useful. Do your own research.

> Obsidian Tasks has been extended to support [[LDP/600 Resources/Ongoing Tasks]]. Tasks can be tagged as `#planned` to mark them as planned "today". They can also have `#ongoing` to mark as "doing now". Queries under [[00 🏠 Main Dashboard|🏠 Main Dashboard]], [[Planned Tasks (View)]], and [[Ongoing Tasks (View)]].

### Alignment
Routine alignment is done through [obsidian-calendar-plugin](https://github.com/liamcain/obsidian-calendar-plugin) and [Periodic Notes](https://github.com/liamcain/obsidian-periodic-notes). They are placed under `500 Alignment`. Check out the calendar on the right-center panel.

### Personal Knowledge Base (PKM)
Obsidian is known to be a link-based note-taking platform. Most follow some form of Zettelkasten or other graph-based organization. Your [[LDP/600 Resources/Resources]] (PKM) should stand next to LDP, not tightly integrated.

I recommend you create a folder at the root of your vault, completely dedicated to your PKM. You can then *pull* these notes into a project, create further notes, and then push them back into your PKM. How you *pull* them is up to you. You can also push as needed.

Your PKM will maintain whatever structure it currently is.

For this demo, they are placed under `600 Resources`.

### Organizing Tasks
There's a command to swap a line of text up or down. I bound it to `alt+w` and `alt+s`. Use this to quickly move a task up and down the To-do list. You can also just highlight a line and click and drag it to where you want it to go. 

Friction is lowered. You can now keep your To-Do list clean. 

Optionally, there's a [plugin](https://github.com/ivan-lednev/obsidian-task-archiver) to automatically move all completed tasks to some archived header. Even less friction!

### Habits as Repeating Tasks
Habits in essence are repeating [[LDP/600 Resources/Tasks]]. This can easily be done with the [Obsidian Tasks](https://github.com/schemar/obsidian-tasks) plugin.

Consider [[LDP/600 Resources/Tasks as Habits in Obsidian]].