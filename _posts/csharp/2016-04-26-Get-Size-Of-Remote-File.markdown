---
layout: post
title: "Get Size Of The Remote File"
description: "Function to get the size of the file on the remote machine."
date: 2016-04-26 10:38:00 +0530
categories: csharp
---
```csharp
private static string GetFileSize(Uri uriPath)
{
    var webRequest = HttpWebRequest.Create(uriPath);
    webRequest.Method = "HEAD";

    using (var webResponse = webRequest.GetResponse())
    {
        var fileSize = webResponse.Headers.Get("Content-Length");
        var fileSizeInMegaByte = Math.Round(Convert.ToDouble(fileSize) / 1024.0 / 1024.0, 2);
        return fileSizeInMegaByte + " MB";
    }
}
```

Usage:
Console.WriteLine(GetFileSize(new Uri("http://xyz.net/img/17.jpg")));
```csharp
