---
title: "How to reset a HTML form on submit using JavaScript"
date: 2024-04-11T14:02:39+05:30
tags: ["javascript", "form", "dom"]
---

By default html forms are reset and all fields are cleared when we submit them.  
However, in instances whereby you use the `preventDefault()` method in the JavaScript file, the form doesn't reset automatically.  
In such situations, we have to trigger the reset event manually using the following [JavaScript method](https://www.w3schools.com/jsref/met_form_reset.asp):

```js
document.getElementById("formId").reset();
```

### Links

https://www.w3schools.com/jsref/met_form_reset.asp
