---
layout: post
title:  "Simple Mapper In C#"
description: "A simple mapper in C# without any explicit mapping"
date:   2016-01-23 14:10:00 +0530
categories: csharp
---

From: http://weblogs.asp.net/imranbaloch/simple-mapper-C

```csharp
public static class Mapper
{
      public static T2 Map<T1, T2>(T1 t1)
      {
          var json = JsonConvert.SerializeObject(t1);
          return JsonConvert.DeserializeObject<T2>(json);
      }
}
```