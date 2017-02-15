---
layout: post
title: "Technology Stack for the web site 'Learning By Teaching' "
date: 2012-05-22 16:25:06 -0700
comments: true
---

#### 1/ Fremework Selection
- whatever framework we select, we need to change/Revamp UI/UX in 6 months. So do not worry pick one and move on.
- There were some initial thoughts on **JQuery** for it simplicity, after looking **Vue.JS and Mobx.JS** youtube Videos there is noway we can DO JQuery. Just for simple CRUD UI/UX Screens you have to CODE each of C R U D operations. Where as with Vue/Mobx/Redux just do CRUD OPERATIONS on DATA STOERE, rest is Taken care ( that is how to exactly change DOM elements) .
- This way without DATA Store concept, JQuery nolonger survive. It is surviving due to complexities of  Angular/React-Redux etc.. But once  Mobx.jS Vue.JS become widespread ( popular ),  JQuery can not survive.
+ > TOdoMVC github repos : files below are STORES 
- [Mobx](https://github.com/mobxjs/mobx-react-todomvc/blob/master/src/stores/TodoStore.js) -- ( [creator by](https://www.mendix.com) )
- [Redux](https://github.com/reactjs/redux/blob/master/examples/todomvc/src/reducers/todos.js) -- ( all React big boys support REDUX )
- [Vue](https://github.com/tastejs/todomvc/blob/gh-pages/examples/vue/js/app.js) -- ( fans: Laravel PHP webFramework, gitlab )

> **final selection: Mobx** why? Vue.js is simple but too far away from REACT, where as Mobx uses React and only replacing REDUX. In futuere if REDUX get simpler we can Swap out Mobx with REDUX, so 

- [Vue.js 2.0 in 60 min](https://www.youtube.com/watch?v=z6hQqgvGI4Y){:target="_blank"} - Best Practice for Front-end development : 3 Panel (Editor, Browser - Console split)
- [Basic Redux Introduction without REACT](https://www.youtube.com/watch?v=ucd5x3Ka3gw){:target="_blank"} - Best explantion of **PURE Barebones Redux** ( see other Tutorials in the Series from same guy till #7)
- [MobX tutorial #2 - Computed Values and Nested/Referenced Observables](https://www.youtube.com/watch?v=nYvNqKrl69s){:target="_blank"} - ( Todo Tutorial )

--------------

#### Common 2/ Utility JS Libraries for Websites
+ create programmatic [dialog boxes][SweatAlert] using Bootstrap modals, without having to worry about creating, managing or removing any of the required DOM elements or JS event handlers
- SweatAlert > [Bootbox][Bootbox]
+ A simple library for handling [keyboard shortcuts][keyboard] in Javascript.
+ Client side (Browser) HTTP Request library 
  - [axios][axios] - promise based ; all Redux Project using this one for AJAX requests
  - [superAgent][superAgent] - good Docs , [comparison][ax vs. sA]
  
+ [UX Clean Design](http://whereis-whoishiring-hiring.me/index) - can be re-designed with React Mobx /w 'State Data Store' FIREST approach
  
  [axios](https://github.com/mzabriskie/axios)
  [superAgent](http://visionmedia.github.io/superagent/#request-basics)
  [ax vs. sA](https://www.sitepoint.com/comparison-javascript-http-libraries/)

> **Discovery ( How to find these JS Libraries?)** : for **Keyborad** shortcut Libs, when I searech github with 'keyboard' (order by most stars), above Mousetrap lib was found.
> using [javaScripting.com][javaScripting] website, for same 'keyboard' search showed 'mousetrap' heighest Stars(76), but it also shows related Libs, so this seems better than Github serach for JS Libs

[javaScripting]: http://www.javascripting.com/search?q=keyboard
[SweatAlert]: http://t4t5.github.io/sweetalert/
[BootBox]: http://bootboxjs.com/examples.html#bb-alert-dialog
[keyboard]: https://craig.is/killing/mice



#### Layout Model - some of the Layout considered 

| Iten    | Layout        |                        
|:--------|:--------------------------|:---------------
| 1       | HTML Ref site             |  [htmlRef site](http://htmlreference.io/element/article/){:target="_blank"}  
| 2       | TeachApCS                 | site is down, github has file , cloned on Mac 
| 3       | Exercisim                 | [shows Iteration 1 , 2, 3 ](http://exercism.io/submissions/306ebe1f98ca4e0ab8754d64484eb907){:target="_blank"}  
| 4       |      python Tutor        |  good interactive pyton


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

