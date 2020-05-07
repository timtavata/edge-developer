---
description: Host web content in your Win32 app with the Microsoft Edge WebView 2 control
title: Microsoft Edge WebView 2 for Win32 apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
---

# Overview of Microsoft Edge WebView2 (Preview)

The Microsoft Edge WebView2 control enables you to host web content in your application using [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/) as the rendering engine.

The WebView2 control is currently in developer preview, during which you can prototype your solutions and share feedback with us to shape the future stable API. There will likely be some breaking changes as we evolve the API during preview, and when this happens, you will need to have both the WebView2 SDK and the Microsoft Edge (Chromium) browser updated. Breaking changes will be noted in the [release notes](webview2/releasenotes.md) of the SDK. This will lock down as WebView2 approaches beta and stable.

## Supported Platforms

A developer preview is available for Win32 C++ on Windows 10, Windows 8.1, Windows 8, Windows 7, Windows Server 2016, Windows Server 2012/2012R2, and Windows Server 2008 R2. An Alpha version for WinUI 3.0 is available [here](https://docs.microsoft.com/uwp/toolkits/winui3/). In the future, we plan to support WebView2 on .NET.  

## Getting Started

To build and test your application using the WebView2 control, you need to have both [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download/) and the [WebView2 SDK](https://aka.ms/webviewnuget) installed. See [Getting Started](webview2/gettingstarted.md) for detailed instructions, [WebView2 API Sample](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample) for an interactive guide, [API reference](webview2/reference-webview2.md) to learn about the API, and [Release Notes](webview2/releasenotes.md) for changes made between releases.

## WebView2 Benefits

## How WebView2 Works

## WebView2 Samples

The [WebView2 Samples](https://github.com/MicrosoftEdge/WebView2Samples) repository contains samples that demonstrate all of the WebView2 SDK's features and their API use patterns. As we add more features to the WebView2 SDK, we will regularly update our sample applications.

## WebView2 Resources

## Feedback

Help us build a richer WebView2 experience by sharing your feedback! Visit our [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports. It’s also a good place to search for known issues.
During developer preview, we will also be collecting telemetry data to help us build a better WebView. Users can turn off WebView data collection by navigating to edge://settings/privacy in the browser and turning off browser data collection.
