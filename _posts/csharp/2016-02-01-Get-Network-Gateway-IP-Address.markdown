---
layout: post
title:  "Get Network Gateway IP Address"
description: "Returns the network gateway IP address"
date:   2016-02-01 08:46:00 +0530
categories: csharp
---
```csharp
/// <summary>
/// Returns the Network Gateway IP
/// </summary>
/// <returns>Gateway IP Address</returns>
public string NetworkGateway()
{
    string ip = null;

    foreach (NetworkInterface f in NetworkInterface.GetAllNetworkInterfaces())
    {
        if (f.OperationalStatus == OperationalStatus.Up)
        {
            foreach (GatewayIPAddressInformation d in f.GetIPProperties().GatewayAddresses)
            {
                ip = d.Address.ToString();
            }
        }
    }
   return ip;
}
```