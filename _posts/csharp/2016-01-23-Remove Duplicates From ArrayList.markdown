---
layout: post
title:  "Remove duplicate from ArrayList"
description: "FFunction to remove duplicate values from an ArrayList"
date:   2016-01-23 21:50:08 +0530
categories: csharp
---
```csharp
private static ArrayList RemoveDuplicates(ArrayList arrList) 
{ 
    ArrayList list = new ArrayList();
    foreach (string item in arrList) 
    { 
        if (!list.Contains(item)) 
        { 
            list.Add(item); 
        } 
    } 
    return list; 
}
```