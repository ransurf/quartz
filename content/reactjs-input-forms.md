---
title: ReactJS Input Forms
---
Status: 
Tags: 
Links: [ReactJS Web Features](out/reactjs-web-features.md)
___

# ReactJS Input Forms
First, store form parameters
```js
const [formParams, setFormParams] = React.useState({
  key: value,
});
```

Set up a form (in this case it's Material UI textField)
```js
<form onSubmit={handleSubmit}>
	<TextField
	  onChange={(e) => onHandleChange(e, "key")}
	  label="field" //shown above text box
	  placeholder="Enter field" //shown in text box
	  type="key" //idek
	  fullWidth
	  required
	/>;
</form>

//remember to have button with type submit !
```

Each time an input form gets changed, call `onHandleChange()`
```js
const onHandleChange = (e, field) => { //e = event
  switch (field) { //only change the changed value
    case "key1":
      setFormParams({ ...formParams, key1: e.target.value }); //keeps old value
      break;
    case "key2":
      setFormParams({ ...formParams, key2: e.target.value });
      break;
  }
};

```

Once the form is submitted, 
```javascript
const handleSubmit = async (e) => {
    e.preventDefault(); //prevent page reload
    const request = await APIFirebase.signUp(
        formParams.key1, 
		formParams.key2
    ); //api call to store data into firebase
    if (!request) { //if no response
        console.log("Signup Failed!");
    } else { //request successful
        console.log("Signup Successful!");
    }
};
```

## Examples
OnlyProfs
- `LoginPage.js`
- `SignUpPage.js`
- `UploadLecture.js`
___
References:

Created:: 2022-03-19 22:17
