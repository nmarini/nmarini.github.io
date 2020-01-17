---
layout: post
title:      "React Component Lifecycles - pt 2 – Lifecycle Hooks and Rendering "
date:       2020-01-17 17:36:37 -0500
permalink:  react_component_lifecycles_-_pt_2_lifecycle_hooks_and_rendering
---


To ensure that the app can quickly react and update when needed, React Components are equipped with** lifecycle hooks** or **lifecycle methods**.  These methods give the developer opportunities to change how the component behaves throughout different points in the component’s lifecycle.  

This is where the lifecycle hooks/methods get their name; they are available before the component is created, after it is created, and when it is going to be deleted.  

**Render**: the render method is the only method required for a React Component to be valid.  This method returns the HTML that is required of all React Components.  

There are a number of different methods that can be utilized to manipulate a Component.  The optional methods can be used to manipulate the Component during Pre-Mounting, Mounting, Updating, and Unmounting.

