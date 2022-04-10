Status: 
Tags: 
Links: [[ReactJS]]
___
# React CSS and Styles
## Principles
- Cannot put two elements in at once, unless you type cast as a div
- `class` in html => `className` for JSX
	- ex) `<p className="{name}">This is a paragraph</p>`
	- Cannot apply to components, only elements
### In-code styles
- Used for more dynamic js based on variables
**Inline**
```jsx
<p style={{color: "#00FFFF", fontSize: 24}}>This is a paragraph</p>
```
**Using `style` var**
```jsx
const styles = {
	color: "#00FFFF",
	fontSize: 24
}

<p style={styles}>This is a paragraph</p>
```
___
# Backlinks
```dataview
list from [[React CSS and Styles]] AND !outgoing([[React CSS and Styles]])
```
___
References:

Created:: 2021-10-03 15:18
