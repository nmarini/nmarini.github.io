---
layout: post
title:      "Redux: Why and When to use it"
date:       2019-11-11 23:58:49 +0000
permalink:  redux_why_and_when_to_use_it
---


How do components pass data to one another without Redux?  

The components utilize their state and their child components' props to pass data to one each other.  If, for example, a parent component displays information that a child component should be able to change, the parent component may need to pass down an event handler to that child component's props.  Then the child component can utilize that event handler and update the data that is represented by the parent component.  

But what if that child component was nested deeper than just one level under the parent component? 
How would you pass the event handler to that deeply nested child component?  

You would have to pass the event handler to every component between the parent and the deeply nested child component.  

Depending on the size of your application, passing information from component to component may become cumbersome.  Redux solves this problem by creating on global state for the application to utilize.  This global state is referred to as the *store* and is accessible to any component.  So, instead of being forced to pass down information from one component to the next, both components can be connected to the store and have access to the needed information without going through layers of other components.  

Now the question is, why wouldn't you use Redux?  

Well, Redux does take some setup which may be time consuming; you have to create reducers, actions, connect components to the Redux store, and more.  If you are working with a small application then using Redux would hinder you more than help you.  There would be a lot of setup with little reward given the time it would take to put together versus the time you save utilizing Redux.

Redux has a lot of utility with larger applications, and applications that want to avoid passing data to components that do not necessarily need that data, but it is not useful for every type of application.  
