---
title: ReactJS + Firebase User Creation
---
Status: 
Tags: 
Links: [ReactJS Web Features](out/reactjs-web-features.md)
___

# ReactJS User Authentication
## Server-Side
In `firebase.js` have
```js
const auth = getAuth(); 
```

Import functions
```js
// Coder-made functions to create documents to store user info
import { 
	createProfessorDocument,
	createInstructorDocument 
} from "./create.js"; 

//Official Firebase methods used for user authentication
import { 
	signInWithEmailAndPassword,
	createUserWithEmailAndPassword,
} from "firebase/auth";  
```

Call Firebase functions
```js
const signUpProfessor = async (
    email,
    password,
    username,
    title,
    description
) => {
    let user = undefined;
    await createUserWithEmailAndPassword(auth, email, password)
        .then((userCredential) => {
            user = userCredential.user;
            user.displayName = username;
            createProfessorDocument(user, username, title, description);
        }) //
        .catch((error) => {
            console.log(serverError(error.code, error.message));
        });
    return user;
};
```

Creating the professor document
```js
const createProfessorDocument = async (
    user,
    userUsername,
    userTitle,
    userDescription
) => {
    await setDoc(
        doc(db, `Professors/${user.uid}`),
        {
            email: user.email,
            username: userUsername,
            title: userTitle,
            description: userDescription,
        },
        { merge: true } //add onto already-existing
    );
};

```
Export functions
```js
export { signIn, signUpProfessor, signUpInstructor };
```
### Usage for React
Import functions from files
```js
import * as Auth from "./firebase-files/Auth";
import * as Create from "./firebase-files/create";
```
## Examples
OnlyProfs

___
References:

Created:: 2022-03-19 22:40
