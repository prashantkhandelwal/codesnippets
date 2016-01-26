---
layout: post
title:  "Reverse Short URL"
description: "Reverse the short URLs"
date:   2016-01-26 20:53:00 +0530
categories: csharp
---

Function to reverse lookup the short URLs. For example: http://bit.ly/dfh54

```csharp
public static string ReverseShortURL(string ShortURL)
{
    HttpWebRequest Webrequest = (HttpWebRequest)HttpWebRequest.Create(ShortURL);
    HttpWebResponse Webresponse = (HttpWebResponse)Webrequest.GetResponse();
    Uri uri = Webresponse.ResponseUri;
    return uri.AbsoluteUri;
}
```