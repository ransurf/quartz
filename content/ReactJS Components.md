Status: 
Tags: 
Links: [[ReactJS]]
___
# ReactJS Components
## Principles
- Capitalized

Storing
- Can render functions/other files which store elements
- Store components into folders

- Can be passed [[ReactJS Props]] for dynamic
### Tips
- Hide components if empty parameters
	- ex) `<h3 style={{display: props.question ? "block" : "none"}}>`
	- ex) `display: !props.question && "none"`
- Can use `array.map` to efficiently send data to smaller components and make code for lists more compact
	- You can just put an array in the return
## Example
### Hierarchy Structure
[![Image from Gyazo](https://i.gyazo.com/74bb75d54ca247438249d4e0bb8bb0eb.png)](https://gyazo.com/74bb75d54ca247438249d4e0bb8bb0eb)
### App.js
```jsx
import react from 'react';
import reactDom from 'react-dom';

function App() {
  return (
    <div> 
      <h1>John Mavrick</h1>
      <p>Bla bla bla this is a paragraph</p>
      <ol>I would like to visit:
        <li>Africa</li>
        <li>And Africa</li>
        <li>Or Africa</li>
      </ol>
    </div> //used for multi-element functions
  )
}

export default App; //exports for other files to use
```
### index.js
```jsx
// ./ means search from current dir, no need to include .js
import App from './App';


ReactDOM.render(
	<MyApp />,
	document.getElementById('root')
);
```
___
# Backlinks
```dataview
list from [[ReactJS Components]] AND !outgoing([[ReactJS Components]])
```
___
References:

Created:: 2021-10-01 19:32
