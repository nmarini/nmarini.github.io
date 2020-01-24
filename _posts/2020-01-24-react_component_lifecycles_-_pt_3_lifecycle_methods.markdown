---
layout: post
title:      "React Component Lifecycles - pt 3 – Lifecycle Methods"
date:       2020-01-24 22:28:44 +0000
permalink:  react_component_lifecycles_-_pt_3_lifecycle_methods
---


React Components can be either *Functional* Components or *Class* Components.  One of the differences between the two styles of components is that Class components have access to lifecycle methods and Functional components do not. 

The following is an explanation for some of the React Component Lifecycle methods categorized by the lifecycle event:

# Pre – Mounting
Given that React Class Components are just basically just JavaScript classes, the class’s constructor function is called.  The **constructor** method establishes the components state and also can utilize the components props.  
# Mounting
After the constructor method is called, the static getDerivedStateFromProps will get called just before the component renders.  **getDerivedStateFromProps** has access to both props and state and can change and return state before the component renders.  The method gets called anytime the component renders.  This method is rarely used, and may negatively impact the performance of your component give the added logic that is used when rendering and re-rendering the same component.  
Just after a component is rendered, componentDidMount is called.  **componentDidMount** is typically used to render asynchronous processes that may not be initially available when the component mounts.  This way, once the process is complete, the method will re-render and use the API content.  
# Updating 
Anytime a component is re-rendered, methods that focus on updating the component will be called.  **shouldComponentUpdate** method is invoked right before a component is about to re-render, and gives you the chance to compare the new and old props and state to prevent unnecessary re-renders.  
Just before the component updates, getSnapshotBeforeUpdate is called. **getSnapshotBeforeUpdate** method returns a snapshot of what is currently occurring on the UI (ex: scroll position) and componentDidUpdate has access to this snapshot.
**componentDidUpdate** method is called after a component is rendered and updated.  This method has access to previous props and state and can utilize this information to make changes when needed. 
# Unmounting
This lifecycle event occurs when the component is deleted and cleared out of the page.  The only lifecycle hook/method that is called at this stage is **componentWillUnmount**. This method gets called just before the component is about to be deleted.  This method is utilized to clear out or change any data that was being utilized by the soon-to-be deleted component.   


