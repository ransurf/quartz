---
started: 2022-02-28 
finished:
rating:
---
Status: #📥
Tags: [[JavaScript Mastery]]
Links: [[+ Videos]]
___
# + Build and Deploy a Fullstack Responsive Portfolio Website
> [URL](https://www.youtube.com/watch?v=3HNyXCPDQ7Q&list=PLntFhxSBHZuqXRHjvQ-cKCyzU9UcDEvNV&index=13&ab_channel=JavaScriptMastery)

## Notes
- import react-tooltipzzzz
- Take note on the good react coding practice
	- Folder structure
	- index.js to export to other parts of the application
- Syntax
	- ../../ helps you go up a layer???
- BEM methodology
	- https://www.devbridge.com/articles/implementing-clean-css-bem-method/
	- app__navbar
	- block element modifier

Inspect on mobile
- Toggle device toolbar in top left of inspect element
#### deployment
npm run build
- netlify
- drop build folder into netlify
- go to sanity manage, CORS origins, add new website into thingy
- ctrl + shift + r to do hard reload
#### scss
var(--white-color)
using vars:
#### header
add blur for content behind:
backdrop-filter: blur(4px);
-webkit-backdrop-filter: blur(4px);

subtle border
border: 1px solid rgba(255, 255, 255, 0.18)
- scss allows you to nest instead of creating new things for each
	- then add media queries, etc
- flex: 1; takes up all space from non-fixed
- transition: all 0.3s ease-in-out

Framermotion
<motion.div> in navbar.jsx

background-repeat: repeat;

subtle drop shadow
`box-shadow: 0 0 20px rgba(0,0,0,0.1)

- Use motion.div to make information responsive
	- whileInView{{opacity: 1}}
	- whileOnHover
	- add keys for each item just by adding the index

#### sanity
1:45:00
client.js

`sanity manage`

.env is to hide variables bruh
Reloading is done through ctrl c + ctrl y

Can give clients a cms website to edit info of website :o
- Can also create content

### Practices
#### css
- Use in-line style for logic-related css
- Using span to have different styling for a heading/text

adding color to grayscale
- refer to brands

motion in a div
- framer motion
- refer to any div lmao

Change the type of display depending on the the screen size using media queries
	- Sometimes even completely change
	- 950 is for small
	- min-width 2000 is for large large
#### Coding
- Separate external imports (libraries) with internal imports (classes, etc) using a space
- If typing something long, create a long const
- Use state to keep track of loading and submitted states, use conoditional code to display different messages

`const { name, email } = formData;
- Removes need to also type formData


#### Higher order components
2:02:00
- Wrapper that is casted onto the export part of a thing
- Add it to all components

## Thoughts/Questions
- 
### General Style
- Use of shapes and unique layout
- Transitions on literally everything
### Future Learning
- Learn when to use margin vs padding
- Learn how to use scss
	- Variables
- Using different types of HTML
- 
___
# Backlinks
```dataview
list from [[+ Build and Deploy a Fullstack Responsive Portfolio Website]]
```
___
Created:: 2022-02-28 11:02


