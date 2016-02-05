---
layout: post
title: "Convert DataType To Another DataType"
description: "Function to covert one datatype to another datatype"
date: 2016-02-05 15:33:00 +0530
categories: csharp
---
```csharp
/// <summary>
/// converts one type to another
/// Example:
/// var age = "28";
/// var intAge = age.To<int>();
/// var doubleAge = intAge.To<double>();
/// var decimalAge = doubleAge.To<decimal>();
/// </summary>
/// <typeparam name="T"></typeparam>
/// <param name="value"></param>
/// <returns></returns>
public static T To<T>(this IConvertible value)
{
    try
    {
        Type t = typeof(T);
        Type u = Nullable.GetUnderlyingType(t);

        if (u != null)
        {
            if (value == null || value.Equals(""))
                return default(T);

            return (T)Convert.ChangeType(value, u);
        }
        else
        {
            if (value == null || value.Equals(""))
                return default(T);

            return (T)Convert.ChangeType(value, t);
        }
    }
    catch
    {
        return default(T);
    }
}

public static T To<T>(this IConvertible value, IConvertible ifError)
{
    try
    {
        Type t = typeof(T);
        Type u = Nullable.GetUnderlyingType(t);

        if (u != null)
        {
            if (value == null || value.Equals(""))
                return (T)ifError;

            return (T)Convert.ChangeType(value, u);
        }
        else
        {
            if (value == null || value.Equals(""))
                return (T)(ifError.To<T>());

            return (T)Convert.ChangeType(value, t);
        }
    }
    catch
    {
        return (T)ifError;
    }
}
```