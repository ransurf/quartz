---
started: 2021-09-05
finished:
status: new idea
category: obsidian
---
Tags: #videoidea #📹/⬛ 
Links: [!V Video Ideas](!V%20Video%20Ideas)
___
# !V Smart Notes in Obsidian
- [Smart notes in obsidian youtube description](Smart%20notes%20in%20obsidian%20youtube%20description)
## Notes
[Reference](https://theknowledgeworker.substack.com/p/how-to-take-smart-notes-in-obsidian)
- [Smart Notes Structure](Smart%20Notes%20Structure) 
## Details
### Prompts
##### What
**How would you describe this project?**
- because it is a popular topic
##### Who
**Is there a target audience? Why will the audience watch the video?**
- People who want to take smart notes
##### Why
**Why are you doing this project? How does this video benefit me/my channel?**
- Because I want to showcase my vault and so I can better understand how my vault has unconsciously followed smart notes

**What ideas/messages do I want to focus on in the video?**
- Stuff in the reference and my application note

##### How
**What skills and knowledge will you need to complete this project?**
- 

**What will my script include?**
- 

**What will my video include?**
- 

**What materials, resources, etc. will you need to complete your project?**
- 

## Brainstorming
### Intro
**How will you make sure the viewer is seen/understood within the first 15 seconds?**
- If you're looking for a structure for your zettlekasten vault in Obsidian but need some inspiration, then look no further. In this video, I'll show the different notes and systems I have in place in my obsidian vault, including the plugins, templates, external programs, and practices I use to make the entire system work. Without any further ado, here's how I take smart notes in obsidian.
### Recommended readings
- This video will mostly be on the implementation rather than the theory behind the system, so if you want a little bit of background on the zettlekasten or smart notes system I would recommend you learn a bit about it beforehand. You can do this by reading the book "how to take smart notes" or a summary of  the principles of the book like this article I'll link in the description: https://theknowledgeworker.substack.com/p/how-to-take-smart-notes-in-obsidian
	- If you want to learn more about some of the practices of this workflow, lots of the functionality is copied from bryan jenk's 4 hour comprehensive workflow video, so I would highly suggest watching that as well if you want some more clarification
#### Types of Notes
- In the book, there's 4 main kinds of notes discussed: fleeting notes, literature notes, permanent notes, and project notes

**Fleeting Notes**
- Fleeting ideas are temporary reminders of information, and I categorize the notes I take for these ideas as either informational and actionable

**Informational fleeting notes**
- To create my information or idea related fleeting notes, I tend to simply open the quick switcher, type the idea or topic, and press shift and enter to create it
- In most cases, I tend to create notes for most ideas I think of, especially for more personal ideas
- If it's a personal idea, I prefix the title with an equals sign to automatically import a template with extra prompts to spark reflection and elaboration
- If the idea is more informational or objective, I just name it normally and it will import the default note template I use
- To organize these notes based on their developmental stages, I use the evergreen notes system popularized by andy matuschak
- In the status field of my note, I set the tag to:
	- a seedling if it's a bare-bones idea
	- a herb if it could still use some expansion
	- a sun if it's developed but is lacking connections to other ideas
	- an evergreen note if it's finished
	- not gonna lie, I have not been conscious for maintaining this system so most of my notes have no status lmao
	- The types of informational notes I make can widely vary, so I just use a simple template and add onto it depending on the situation
		- It's automated using templater and my meta template from bryan jenks which can be a bit complicated if you aren't into programming, but you can always manually import templates using plugins like templater or quickadd
			- To make the most out of the interconnectedness obsidian allows, spend some time thinking of relevant tags so it can be connected to the rest of your vault
				- Tags are for general topics it's related to, while links are for it's hierarchical relations to bigger ideas like a traditional file structure

**Actionable fleeting notes**
- If the idea is something more actionable like a task, I tend to use lists to keep track of it
	- If it's something related to my vault or the contents of it, I've recently downloaded a reminders plugin to help me easily see some things I need to keep note of
		- To create a new reminder, simply create a task, write down what you want to be reminded of, then set the date for the reminder using the following syntax
			- Then, I can access it in the reminders pane in my sidebar
				- I find this plugin useful as it actually has notifications when you open obsidian, and the process of creating a reminder is simple yet effective
	- Otherwise, I use to do lists to keep track of things I need to do throughout the day. If you're interested in an in-depth explanation, be sure to check out my task and project management video

**Literature/input notes**
- I use literature notes to keep track on my progress of certain inputs
- I have different templates, depending on the type of input it is
	- Books should not be consumed in the same way as short articles or podcasts
		- Video on how I take book notes if you're interested in learning a bit more about my workflow and templates
- For the most part, I just have fields like when I started, when I finished, and some relevant things to keep track of like the link
- Also, copied from bryan jenk's workflow, I have prefixes for the note titles so I can easily organize and search them up
	- Also serve to help automate the template insertion through templater
- You could embed videos and pdfs, but I prefer to just view things on the browser or books on calibre


**Project Notes**
- Project notes contain my project planning, any relevant resources, and organize the different tasks I have into their respective projects
	- I'm gonna sound like a broken record, but this is also elaborated upon in task and project management workflow video


**Permanent notes**
- I like to hoard things so usually all my notes stay as permanent notes. The only time I'll delete notes are if I'm starting to get a lot of task notes that are cluttering my system, or if I feel like a seedling idea isn't worth expanding on. I know some people prefer to delete literature or project notes once they're done transferring the information into permanent notes, but I just like to keep them as a reference

Now that you have a general idea on the types of notes featured in my vault it's time to get into how I organize and structure everything
#### System components
**Inbox**
- It's self-explanatory, but an inbox used to quickly capture and sort things to work on them later
- I have different inboxes for seedling notes, inputs I need to consume, things to act upon within my vault, and tasks
	- I use a workbench note to see what notes I need to work on
		- it has queries to search for seedling, herb, or sun notes that may need further development
		- Using the workbench plugin, I can run a command to link the current note in my workbench as a reminder
	- For information inside my vault, I use the reminder plugin I referenced earlier as it's quick and simple
- To keep track of my inputs inbox, I currently use pocket to easily save any things I want to consume, but I'm planning on switching to raindrop as it has folders you can do some organizing with

**Manage the tracking and storage of my inputs**
- To manage the tracking and storage of my inputs, I have a main note for all my inputs, which are then broken down into the different kinds
	- To keep track of all my literature notes, I use kanban lists using dataview queries to keep track of everything
		- In the note, I tag the status of the note, with stages including not finished, reading, implementing, and finished
- Book notes are separated as I'm more thorough with my book readings but the note to organize them also has a dataview kanban list
	- I've been reading on my kindle so i use the kindle highlights plugin to import all my selections into obsidian, which are then all stored in a single note
	- However, I've also been trying to incorporate calibre and it's different highlights and annotation capabilities so I can be more indepth in my notes

**Task and Project Management**
- I currently use todoist to keep tack of tasks and habitica to track dailies and habits, but you can definitely use obsidian task plugins like mentioned in my task and project management video
	- Benefits include having more room to work with as each task is a whole note if you're using tq, having everything stored in one place
		- It's also free and customizable so you won't have to pay a monthly subscription for features
	- However, I just switched because I switch between 4 different devices as a university student, so I need the easy access todoist has
- I do like to keep my project notes on obsidian still, and I feel like these paired with my weekly review have really helped me stay productive and ambitious
- I have a project hub for seeing my current projects which are then sorted by their timeframes
	- Also used to have different notes with different searching filters for when I had my task management in obsidian

#### Extra Personal Uses
These aren't really zettlekasten related, but they're still useful ways I utilize the vault
- Daily notes
- I also apply the kanban list idea into other things like my video projects
- To keep track of some of my workflows and personal practices, I like to include the prefix "My" to the notes
	- You can also have a note to keep track of all your personal workflows using dataview, like shown
- You can make obsidian work with other programs. For example, I like to create my anki cards in obsidian, start and stop time entries in toggl, etc
#### My personal benefits
Easy recollection
- The main benefit I've noticed in comparison to other note taking systems is how easy it is to recall and access information
- by taking note of virtually all your ideas and forming connections, you won't have to do much retrieval from your brain
	- To access different ideas, I just use quick switcher as I name my notes well enough
		- If that doesn't work though, you can always use the search query to look for documents with certain text inside, or just start at a relevant note and use links or the local graph
- By having such easy and varied access to all your information, it makes it easy to think of topics and find content for writings and videos as all you have to do is organize information

Freedom of organizaiton
- Second, I've found the flexibility of the structure of my notes to be game-changing
	- I can have a folder structure while also connecting higher-level ideas together
		- Notes don't only have to be under one hierarchy, they can be connected to a lot of different things
		- Instead of using folders, I would recommend using hierarchical tags as they're less tedious than moving notes into folders
### Conclusion
**What are some relevant references or links?**
- So, that's about everything! Thanks for watching until the end of the video
- My workflow is highly copied by bryan jenks, so I would highly suggest checking out his workflow videos as there may be things I didn't find useful that could be for you
- How to take smart notes can help if you're struggling to understand the purpose, as he provides some good examples and his writing is very good

**How can I sum up the contents of the video?**
- So that's essentially the structure of my obsidian vault
	- I did read the smart notes book but didn't really focus on trying to implement the zettlekasten method, but it seems as if my vault has a rough resemblance of it
- You don't have to copy the system exactly as it's just the ways I've managed to implement some of the ideas in the book. Feel free to watch other videos and workflows to mix and match ideas and come up with something that best suits your needs
- Generic outro
___
References:

Created:: 2021-09-05 15:33

