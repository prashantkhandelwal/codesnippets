---
layout: post
title:  "Checks If The Element Is Hidden"
description: "jQuery to check if the element is hidden or not on the HTML page"
date:   2016-01-26 21:04:00 +0530
categories: csharp
---

Below code is valid for display:[none|block] but it will ignore visible:[true|false] 

```csharp
$(element).is(":visible"); 
```