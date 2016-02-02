---
layout: post
title:  "Get The Number Of Occurences In The Given String"
description: "Get the number of occurences in the given string"
date:   2016-02-02 19:23:00 +0530
categories: csharp
---

Extension mehod to get the number of occurences in the given string.

```csharp
/// <summary>
/// Returns the number of occurences in the given string
/// </summary>
/// <param name="str"></param>
/// <param name="searchString"></param>
/// <returns></returns>
public static int GetOccurencesOf(this string str, string searchString)
{
    if (searchString.IsNullOrEmpty())
        return 0;

    int count = 0;
    int searchIndex = str.IndexOf(searchString);

    while (searchIndex > -1)
    {
        ++count;
        searchIndex = str.IndexOf(searchString, searchIndex + searchString.Length);
    }
    return count;
}
```