---
layout: post
title:  "Quick n' Dirty: Keyboard Navigation"
date:   2016-12-26 12:00:00 -0600
categories: jekyll
---

I was recently on a comic website and was struggling heavily with their poor UI layout that made navigating pages quite painful so I wrote a tiny [tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=en) script to add in WASD style navigation. This particular site has both between issue and in-issue Previous/Next, so there is a "next page" and a "next comic" button.

For compatibility this is written as an ES5 IIFE with ye-olde dom events instead of some sexier DOM 3 tricks. Links are grabbed by text content which is expensive but this particular site didn't have consistent classes or ids. I use `focusin` and `focusout` to make sure we aren't in a textfield when navigating so you can still use search and whatnot (and it's way cheaper/easier than patching every input with custom events and pretty well supported in most browsers).

For some potential upgrades, move to ES6, use `compositionstart` and `compositionend`, and use the new keyboard API instead of fighting keyCode.

```javascript
// ==UserScript==
// @name         e6 key
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  add keyboard navigation
// @include        *://blah.com/*
// @exclude     *.json
// @exclude     *.xml
// @grant        none
// ==/UserScript==

(function(window, document) {
  'use strict';
  var isEditing = false;

  //patch so we can disable ourselves on editing events
  document.addEventListener('focusin', function(){
    isEditing = true;
  });
  document.addEventListener('focusout', function(){
    isEditing = false;
  });

  function getLinkByText(text) {
    var aTags = document.getElementsByTagName("a");

    for (var i = 0; i < aTags.length; i++) {
      if (aTags[i].textContent === text) return aTags[i];
    }
  }

  document.addEventListener('keydown', function(event) {
    var target;
    if(isEditing) return;

    switch(event.keyCode) {
      case 87: //w
        window.scrollBy(0, -250);
      break;
      case 83: //s
        window.scrollBy(0, 250);
      break;
      case 81: //q
        target = getLinkByText('Previous');
        if(target) return target.click();
        event.preventDefault();
      break;
      case 69: //e
        target = getLinkByText('Next');
        if(target) return target.click();
        event.preventDefault();
      break;
      case 65: //a
        target = getLinkByText('<< Previous');
        if(target) return target.click();
        event.preventDefault();
      break;
      case 68: //d
        target = getLinkByText('Next >>');
        if(target) return target.click();
        event.preventDefault();
      break;
      case 82: //r
        target = getLinkByText('Random');
        if(target) return target.click();
        event.preventDefault();
      break;
    }
  });

})(window, document);
```
