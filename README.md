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
  <Route path="/" render={() => (
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


### HTML/CSS

What are the 3 ways to apply css styles to a webpage?
<details>
  <summary>Answer here</summary>
  <ul>Use inline style attribute</ul>
  <ul>Use style block in head of html </ul>
  <ul>Load external css file using LINK tag </ul>
 </details>
<br>
<br>

Name 3 self closing HTML tags:
<details>
  <summary>Answer here</summary>
  <ul>IMG</ul>
  <ul>INPUT</ul>
  <ul>LINK</ul>
 </details>
<br>
<br>

Desribe the different kinds of selectors? How would you target these elements on a CSS page?
<details>
  <summary>Answer here</summary>
  <ul>You can use tag references ex. p, body, main,</ul>
  <ul>class attributes  ' .nav-item, .button,</ul>
  <ul>id attribute s #name, #home, #1</ul>
 </details>
 <br>
<br>
 
 What does HTML and CSS stand for?
<details>
  <summary>Answer here</summary>
  <ul>Hypertext Markup Language</ul>
  <ul>cascading style sheet </ul>
 </details>
    <br>
  <br>
    
 How is the HTML document structured?
 <details>
  <summary>Answer here</summary>
  <ul>There's always an opening and closing HTML tag,</ul>
  <ul>HEAD tag: meta, stylesheets, links,  </ul>
    <ul>BODY tag: contains majority of display, a, p, body, h1, h2, h3</ul>
    <ul> HEAD and BODY are within HTML tags</ul>
 </details>
 <br>
<br>
    
 What element(s) will the following selection effect, and what will be the resulting action/effect?

```
nav#navigation ul li a:hover {
  color: blue;
}
```
 <details>
  <summary>Answer here</summary>
  <ul>It will make the navigation list element blue on hover</ul>
 </details>
 <br>
  <br>
    
What is the purpose of the “defer” attribute and what tag should it be invoked in?
<details>
  <summary>Answer here</summary>
  <ul>It is in the HEAD sections within a script tag.  Causes JS to load after DOM loads</ul>
 </details>
 <br>
  <br>
    
How does CSS style overring work?
<details>
  <summary>Answer here</summary>
  <ul>inline style > style tags > external sheets</ul>
  <ul> within external sheet: ID > class > tags</ul>
  <ul>If two or more tags are equal, the last one on page is loaded</ul>
 </details>
  <br>
  <br>
    
 What is the difference between semantic and non-semantic html tags?
 <details>
  <summary>Answer here</summary>
  <ul>A semantic element clearly describes its meaning to both the browser and the developer.
 <br>
  <br>
    
Examples of non-semantic elements: <div> and <span> - Tells nothing about its content.

Examples of semantic elements: <form>, <table>, and <article> - Clearly defines its content.</ul>
 </details>
  <br>
  <br>
  
 What is the difference between SPAM and DIV?
 <details>
  <summary>Answer here</summary>
  <ul>The difference is that ```span``` gives the output with ```display: inline``` and ```div``` gives the output with ```display: block```.span is used when we need our elements to be shown in a line, one after the other.</ul>
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
