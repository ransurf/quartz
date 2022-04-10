---
title: ReactJS Props
---

Status: 
Tags: 
Links: [ReactJS Components](out/reactjs-components.md)
___
# ReactJS Props
- Passed into a component to share values
- Read-only
## Syntax
**Object**
```jsx
//Separate Values
<Person
	firstName="John"
	lastName="Mavrick"
/>

// Bundled in an array using map
function App() {
  const products = productsData.map(item => <Product key={item.id} product={item}/>)
  return (
    <div>
        {products}
    </div>
  )
}

export default App
```
**App**
```jsx
//Separate Values
function Person(firstName) {
	<p>First Name: {firstName}</p>
}

//Bundled in an array using map
function Product(props) {
    return (
    <div>
        <h2>{props.product.name}</h2>
        <p>${props.product.price}</p>
        <p>{props.product.description}</p>
    </div>
    )
}

export default Product;
```
___
# Backlinks
```dataview
list from [ReactJS Props](out/reactjs-props.md) AND !outgoing([ReactJS Props](out/reactjs-props.md))
```
___
References:

Created:: 2021-10-03 17:01
