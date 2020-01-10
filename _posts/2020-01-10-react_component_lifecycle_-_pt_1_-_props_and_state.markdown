---
layout: post
title:      "React Component Lifecycle - pt 1 - Props and State"
date:       2020-01-10 23:06:34 +0000
permalink:  react_component_lifecycle_-_pt_1_-_props_and_state
---


In the React JS framework, developers utilize React Components in order to create a React based application.  

**Components** are independent and reusable pieces of code that serve the same purpose as JavaScript functions.  Components work a little differently than regular JavaScript functions since React Components return HTML via a render function.  

React Components also have two sets of properties, which are **props** and **state**.  

A Component’s **props** are a set of external attributes (some logic or data) that are passed to the Component from its parent Component.  

The Component’s **state** is an internal set of attributes that can be manipulated by both the Component’s props and when the user interacts with the Component.

Why do we utilize props and state with our React Components? 

The React framework was created in order to help developers create complex and highly responsive applications.  Props and state allow for components to quickly react to changes from the user or other updates made to the application.  In order to achieve this functionality, Components must go through what is called a **Component Lifecycle**.  This is broadly broken up into three parts: creation, updating, and deletion.  When you look at a React application, everything you see is made up of different React Components going through one of the three steps of the component lifecycle. 
