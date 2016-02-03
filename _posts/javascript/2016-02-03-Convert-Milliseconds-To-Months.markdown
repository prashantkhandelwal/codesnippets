---
layout: post
title:  "Convert Milliseconds To Months"
description: "Javascript function to convert milliseconds to months"
date:   2016-02-03 16:22:00 +0530
categories: javascript
---

Function to convert milliseconds to months. It will round the returned value to 1 decimal place.

```javascript
var MsToMonths = function (ms) {
   return (ms * 3.80264862082E-10).toFixed(1);
};
```