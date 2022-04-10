---
title: React Context
---
Status: 
Tags: 
Links: [ReactJS](out/reactjs.md)
___
# React Context
- [React Docs](https://reactjs.org/docs/context.html)

Wrap all content that needs it in context provider
- 
```js
<Context.Provider value={values}>
	<everything that needs it>
</Context.Provider
```

Class
```js
<Context.Consumer value={values}>
	<everything that needs it>
</Context.Consumer>
```

Function
`import { useContext } from 'react'`
`const darkTheme = useContext(ThemeContext)`
___
# Backlinks
```dataview
list from [React Context](out/react-context.md) AND !outgoing([React Context](out/react-context.md))
```
___
References:

Created:: 2022-01-15 20:26