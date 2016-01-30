---
layout: post
title: "Get The Usage (stats) Of IndexedDB"
description: "Gets the usage/limit of IndexedDB"
date: 2016-01-30 20:21:00 +0530
categories: javascript
---

```javascript
navigator.webkitTemporaryStorage.queryUsageAndQuota(
  function (usedBytes, grantedBytes) {
    console.log('IndexedDB Usage:', usedBytes, 'bytes of', grantedBytes, 'bytes');
  },
  function (e) {
    console.log('Error', e);
  }
);
```