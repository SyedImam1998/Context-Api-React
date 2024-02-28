# Context-Api-React

### Start
- First you need to create a new file at the root directory name it as

``` 
Context.jsx
```

### Intilize the Context

- Inside the Context.jsx start write code below.

``` 
import React,{createContext} from 'react';

export const Context=createContext(null);

export const UserInfo=(props)=>{
    const [isLoggedIn,setIsLoggedIn]=React.useState(false);

    const userObj={
        isLoggedIn,
        setIsLoggedIn,
    }
    return (
        <Context.Provider value={userObj} >
            {props.children}
        </Context.Provider>
    )
}
```

### Wrap App

``` 
 <UserInfo>
    <App />
 </UserInfo>
```

### How to access the state values and methods

```
const {isLoggedIn,setLoggedInStatus}= useContext(Context);
console.log(isLoggedIn); 
setLoggedInStatus(false);

```

