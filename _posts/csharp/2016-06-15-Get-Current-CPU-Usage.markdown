---
layout: post
title:  "Get Current CPU Usage"
description: "Get the current CPU usage."
date:   2016-06-15 10:21:00 +0530
categories: csharp
---

Get current CPU usage.

```csharp
PerformanceCounter cpuCounter = new PerformanceCounter("Processor", "% Processor Time", "_Total", Environment.MachineName);
cpuCounter.NextValue();
System.Threading.Thread.Sleep(1000);
return (int)cpuCounter.NextValue();
```