---
layout: post
title: "Technology Stack for the web site 'Learning By Teaching' "
date: 2012-05-22 16:25:06 -0700
comments: true
---

#### Fremework Selection
- whatever framework we select, we need to change/Revamp UI/UX in 6 months. So do not worry pick one and move on.
- There were some initial thoughts on **JQuery** for it simplicity, after looking **Vue.JS and Mobx.JS** youtube Videos there is noway we can DO JQuery. Just for simple CRUD UI/UX Screens you have to CODE each of C R U D operations. Where as with Vue/Mobx/Redux just do CRUD OPERATIONS on DATA STOERE, rest is Taken care ( that is how to exactly change DOM elements) .
- This way without DATA Store concept, JQuery nolonger survive. It is surviving due to complexities of  Angular/React-Redux etc.. But once  Mobx.jS Vue.JS become widespread ( popular ),  JQuery can not survive.
> **final selection: Mobx** why? Vue.js is simple but too far away from REACT, where as Mobx uses React and only replacing REDUX. In futuere if REDUX get simpler we can Swap out Mobx with REDUX, so 

- [Vue.js 2.0 in 60 min](https://www.youtube.com/watch?v=z6hQqgvGI4Y){:target="_blank"} - Best Practice for Front-end development : 3 Panel (Editor, Browser - Console split)
- [Basic Redux Introduction without REACT](https://www.youtube.com/watch?v=ucd5x3Ka3gw){:target="_blank"} - Best explantion of **PURE Barebones Redux** ( see other Tutorials in the Series from same guy till #7)
- [MobX tutorial #2 - Computed Values and Nested/Referenced Observables](https://www.youtube.com/watch?v=nYvNqKrl69s){:target="_blank"} - ( Todo Tutorial )

--------------

#### Common Utility JS Libraries for Websites
- create programmatic [dialog boxes][BootBox] using Bootstrap modals, without having to worry about creating, managing or removing any of the required DOM elements or JS event handlers
- A simple library for handling [keyboard shortcuts][keyboard] in Javascript.
[BootBox]: http://bootboxjs.com/examples.html#bb-alert-dialog
[keyboard]: https://craig.is/killing/mice

#### Install & Setup  

| Iten    | Stack Component           |       |       |        |
|:--------|:--------------------------|:------|:------|:-------|
| 1       | Dnango REST API           | John  | Adam  | Robert |
| 2       | PostgreSQL DB             |  1:30 |  2:05 |   1:15 |
| 3       | React Redux Boilerplate   | 15:30 | 14:10 |  15:45 |
| 4       | Redux coding Styles(Rajarao)|70%  |   55% |    90% |


##### Integrate Table 

| Iten    | Stack Component           |                       
|:--------|:--------------------------|:---------------
| 1       | Bootbox                   |  [4k github stars1](http://bootboxjs.com/examples.html){:target="_blank"}  |  [4k github stars2](http://bootboxjs.com/examples.html){:target="_blank"}
| 2       | PostgreSQL DB             |  [4k github stars33](http://bootboxjs.com/examples.html){:target="_blank"} |  [4k github stars44](http://bootboxjs.com/examples.html){:target="_blank"}


[BootBox1]: http://bootboxjs.com/examples.html
[newtab]: http://bootboxjs.com/examples.html{:target="_blank"}

#### Model Sites  
- [table generator](http://www.tablesgenerator.com/markdown_tables){:target="_blank"} - very simple bootstrap "Tight" bootstrap menu items  
- they used Bootbox - very good examples, All yor hassel for Alerts

#### Acknowledgments :  
Our project could not be possible without the following wonderful open source software:

- jQuery
- Bootstrap
- Bootbox
- Prism syntax highligher
- GLYPHICONS
- Spectrum Color Picker
- ZeroClipboard

