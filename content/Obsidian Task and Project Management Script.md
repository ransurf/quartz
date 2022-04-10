Status: #📹/⬛ 
Tags: 
Links: [[!V Obsidian Task and Project Management]]
___
# Obsidian Task and Project Management Script
## Introduction
- Subscribe intro
- In this video, I'll share my task and project management system in Obsidian, sharing the workflow, plugins, and templates to make it all work. It's compatible for both PC and mobile usage, so it truly can work as your all-in-one planning system. 
	- If you want your tasks and projects to be highly customizable and integrated into your personal knowledge management app, be sure to watch until the very end.
## Overview/Features
### Projects
- First, I'd like to give a quick tour of the entire system to show you what's in store
- For projects, I have a main note that keeps track of all the active projects depending on their timeframes, as well as those I've already finished. 
- Each project note has a list to show which tasks I still have to do, some prompts when planning the projects and it's smaller tasks.
### Tasks
- Much like a traditional to do list, I have a main note that shows all my tasks, as well as other notes to isolate project-related, miscallaneous, or someday maybe tasks.
- Each task is comprised of a single note, and can be easily created using the TQ plugin, more on that later. The tasks can be labelled  based on their importance or urgency, and the tasks for the day can be seen in my daily note, which are sorted based on size.
- Now, it's time to prepare the tools we need to construct it all.
## Execution
### Plugins
- Thanks to some nifty community plugins, we're given some extra features to make a workflow like this come to life. The main ones needed will be TQ, templater, and dataview.
- TQ provides a UI for creating tasks which are then turned into separate notes. Through search queries, we can then organize the tasks based on various tags or values.
- Templater isn't heavily used in this workflow, but you'll need it if you're planning on using my project template.
- Lastly, Dataview is also used for sorting the relevant task and project sub-categories that fall under the main notes.
- Optional plugins include the quickadd plugin to add additional macros, the admonition plugin to have customizable block-style content, or the checklist plugin to have a UI for showing certain tasks.
Now that we have the tools ready, it's time to lay out the foundation of the system.
## Setup
- All the notes and templates I use will be in my github repository, so be sure to check it out if you just want to copy my structure.
### Hubs
#### To Do's Note Lists
- First off, let's start with the main hub notes that organize everything. In the To Do's hub, I have a reminder for the meanings of the color codings beside each task so I know what they stand for.
- Next, I have a certain tag for each to do list so I can use a dataview query to easily index them. I only have 4 lists, but you can easily make more depending on your needs.
- For the main note, I just use a tq search query to group and sort the tasks by their due date, and another query to list all my completed tasks
- More specific list notes like ones that show only project-related tasks are essentially the same, except you'll have to have sort tasks using tags like projects, somedaymaybe, etc
	- In my case, miscallaneous tasks don't have a tag, so I just omit the mentioned tags above
#### Projects Note
- There's nothing really different in the projects note, except there's additional fields you have to keep track of like its completion status. I'm currently grouping them depending on their timeframes, but you can also group them by their importance, category, deadlines, etc
#### Daily Note
- In my daily note, I have some grouped search queries for easy access when scheduling my day
- Now that the framework is set up, it's time for the templates I use
### Templates
- The note for tasks cannot be changed, but luckily the project template is made from scratch so it can be modified to your own needs. The only mandatory value you need is `completed` as it's needed in the dataview queries, so feel free to add your own like `deadline` or `hibernating`
## New Project
- Inspired by Bryan Jenk's meta template, I prefix my project notes with a tilda so the projects template is automatically inserted into the note when the meta template runs. If you want something similar, I would recommend you check his templater video out.
- If you're also grouping projects by their timeframes, be sure to appropriately tag what kind of project it is
- To have a list of tasks only related to the project, be sure to sort them by a specific project tag. In this case, I have p/w/taskandprojvideo
- After that, it mostly depends on how you like to plan your projects. In my case, I like to plan my projects using hornier goalsetting, which is a stupid, modified system of smart goals I made for fun. It's pretty self-explanatory, but I can go in-depth on another video if needed.
- When planning my tasks I categorize them into to do's which are one-time things, dailies, and habits I can variably perform throughout the day. The tasks are added through the TQ plugin, while dailies and habits are incorporated into habitica.
## New Task
- The UI is pretty intuitive but just remember to include the appropriate tags if it falls under a certain project or task category, and a tag declaring it's size if you want to sort it by that in your daily note like I do
- If you aren't using an external app for dailies like I do, there's an option for repeatable tasks
- The important and urgent tags are based off the eisenhower decision matrix, which I thought was a cool addition for helping prioritize tasks
- If you're still a bit confused, here's an example on how I would create a project 
## Examples
- 
## Conclusion
- Thanks for watching until the very end! This video covers majority of my everyday workflow, but I may not have mentioned  some things as they're related to the workflows in my other videos. If you want to learn more about my periodic projects and planning be sure to check out my periodic reviews video, and if you want to learn more about how I use my daily note feel free to check that out as well. Also, I'm running out of video ideas so please leave a comment if you have any topics or workflows you're interested in. Anyways, if you found my advice helpful be sure to like and share this video, and subscribe for more obsidian and productivity-related content. This has been John Mavrick, stay mindful.
___
# Backlinks
```dataview
list from [[Obsidian Task and Project Management Script]] AND !outgoing([[Obsidian Task and Project Management Script]])
```
___
References:

Created:: 2021-08-27 13:46
