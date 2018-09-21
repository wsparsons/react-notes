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
    Examples of non-semantic elements: DIV and SPAN - Tells nothing about its content.
    Examples of semantic elements: FORM, TABLE, and ARTICLE - Clearly defines its content.</ul>
 </details>
  <br>
  <br>
    
    
 What is the difference between SPAN and DIV?
 <details>
  <summary>Answer here</summary>
  <ul>The difference is that SPAN gives the output with display: inline and DIV gives the output with display: block. Span is used when we need our elements to be shown in a line, one after the other.</ul>
  </details>
   <br>
  <br>


### GIT and GITHUB
<hr>

What is the difference between Git and Github?
<details> 
  <summary>Answer here</summary>
  <ul>Git is a revision control system, a tool to manage your source code history. </ul>
  <ul>GitHub is a hosting service for Git repositories.</ul>
  <ul>So they are not the same thing: Git is the tool, GitHub is the service for projects that use Git.</ul>
  </details>
   <br>
  <br>


What is the difference between forking and cloning?
<details> 
  <summary>Answer here</summary>
  <ul>A fork is a copy of the repository, it allows you to freely make changes without affecting the original project</ul>
  <ul>A clone is when you are connecting that version of the code. You can simply do it with a command line: git clone url_of_the_clone </ul>
  <ul></ul>
  </details>
   <br>
  <br>

What is the difference between git pull and git fetch?
<details> 
  <summary>Answer here</summary>
  <ul>GIT pull command pulls new changes or commits from a particular branch from your central repository and updates your target branch in your local repository while GIT fetch pulls all new commits from the desired branch and stores it in a new branch in your local repository.</ul>
  <ul>Git pull = git fetch + git merge</ul>
  </details>
   <br>
  <br>

What is Git?
<details> 
  <summary>Answer here</summary>
  <ul>GIT is a distributed version control system and source code management (SCM) system.</ul>
  <ul>It can track changes to a file</ul>
  <ul>It allows you to revert back to any particular change</ul>
  <ul>Its distributed architecture provides many advantages over other Version Control Systems</ul>
  </details>
   <br>
  <br>

What are the advantages of using Git?
<details> 
  <summary>Answer here</summary>
  <ul>Data redundancy and replication</ul>
  <ul>High availability</ul>
  <ul>Collaboration friendly</ul>
  </details>
   <br>
  <br>

What is head in Git? How many head can be created in a repository?
<details> 
  <summary>Answer here</summary>
  <ul>A ‘head’ is simply a reference to a commit object. In every repository, there is a default head referred as “Master”.</ul>
  <ul>A repository can contain any number of heads.</ul>
  </details>
   <br>
  <br>


<details> 
  <summary>Answer here</summary>
  <ul></ul>
  <ul></ul>
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
