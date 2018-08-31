# react-notes

## Authors

* Craig Fell
* Wendy Parsons
* Hedim Ramirez

# Questions

### General
What is React?
<details>
  <summary>Answer here</summary>
  A javascript library for building user interfaces.
</details>
<br>

What are the 3 main design concepts of React?
<details>
  <summary>Answer here</summary>
  <ul> Components </ul>
  <ul> Reactive Updates </ul>
  <ul> Virtual View & Memory </ul>
</details>
<br>

###  Components
Functional vs Class Components

Why would you use a Functional vs a Class Component.
<details>
  <summary>Answer here</summary>
  <ul>Functional Components are lighter weight, simply rendering the component. </ul>
  <ul>Class Components are Stateful. </ul>
  <ul>Class component mush have a render function</ul>
  <ul>Class Components are extensible. </ul>
</details>
<br>



### Lifecycle

What are the phases of the React Lifecycle

<details>
  <summary>Answer here</summary>
  <ul>initializing (getDefaultProps, getInitalState) define defaults and intial values for this.props and this.state </ul>
  <ul>mounting (componentDidMount) components are inserted into the DOM. </ul>
  <ul>updating - component properties and state are updated. </ul>
  <ul>unmounting (componentDidUnmount) - component is unmounted from the DOM.</ul>
</details>
<br>


### Rendering

What are the 3 things that can cause re-rendering.

<details>
  <summary>Answer here</summary>
  <ul> when a parent prop getting passed to a child is changed. </ul>
  <ul> when any state changes </ul>
  <ul> when a component gets rendered to the dom for the first time </ul>
</details>
<br>

### State

Describe the React state data structure
<details>
  <summary>Answer here</summary>
  <ul> Object! </ul>

</details>
<br>


### React-Redux

What are the 3 principles of React-Redux and how do they relate to each other
<details>
  <summary>Anser here</summary>
  <ul>Store - object that brings actions and reducers together; stores the STATE of our app</ul>
  <ul>Action - object that informs reducer how to change the state</ul>
  <ul>Reducer - pure function that takes previous state and an argument to return a new state.</ul>
</details>
<br>

What is the purpose of mapStateToProps and mapStateToDispatch? How do you connect them?
<details>
  <summary>Anser here</summary>
  <ul>mapStateToProps allows the state held in a store file to be sent to a component as props</ul>
  <ul>mapToDispatch is similar but maps the actions to the component</ul>
  <ul>The mapping to components is linked to the component using `connect`from 'react-redux' </ul>
</details>
<br>

Explain in detail how mapStateToDispatch functions
<details>
  <summary>Answer Here</summary>
  <ul>you can define a function called mapDispatchToProps() that receives the dispatch() method and returns callback props that you want to inject into the presentational component</ul>  
  <ul>```const mapDispatchToProps = dispatch =>
  bindActionCreators(
    {
      createPost
    },
    dispatch
  );
    ```
  </ul>
</details>
<br>

### React-Router
Given the following route, what resource will the user be shown when visiting the site root if authenticated/logged in.
```<Switch>
  <Route path="/home" render={() => (
  loggedIn ? (
    <Redirect to="/dashboard"/>
  ) : (
    <PublicHomePage/>  )
)}/>
  <Route exact path="/dashboard" render={() => {
    return <ProfilesHome />
  }}/>
</Switch>
```

<details>
  <summary>Answer here</summary>
  <ul>ProfilesHome </ul>
 </details>
<br>
<br>


Fix this function so that it works. (hint, there are 2 items that need fixing.)

```import React from 'React'
import { Route, Redirect } from 'react-router-dom'

const Navigation = () => {
  return (
    <Link to="/login" className="nav-link">Login</Link>
  )
}

export default
```
<details>
  <summary>Answer here</summary>
  <ul>Add Link to react-router-dom import </ul>
  <ul> export Navigation </ul>
 </details>
<br>
<br>





### Future Question Topics
Props

State Management
  - how do you manage State
  - State Inheritance

What is the difference between controlled & uncontrolled components.

JSX
