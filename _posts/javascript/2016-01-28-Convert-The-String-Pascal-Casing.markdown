---
layout: post
title:  "Convert The String To Pascal Casing"
description: "Javascript to convert the string to pascal casing."
date:   2016-01-28 16:35:00 +0530
categories: javascript
---

Code to convert the string to pascal casing. 

E.g.
---
BUILDING: Building
---

```javascript
var ToPascalCase = function (str) {
 return str.replace(/(\w)(\w*)/g,
   function (g0, g1, g2) {
    return g1.toUpperCase() + g2.toLowerCase();
  });
};
```