---
description: Distribution options when releasing an app using Microsoft Edge WebView2
title: Distribution of Microsoft Edge WebView2 Application
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
---

# Distribution of Applications using WebView2


**With the 2 version models. Both require effort from a developer for distribution. This article outlines the steps and evaluation a dev must do when distributing an application using WebView2.**


## App Distribution
The WebView2 control utilizes the Microsoft Edge (Chromium) browser. When distributing your app it is important to ensure that the Edge browser is installed on all user machines where your application will run. You should also be aware of which version and channel is installed, e.g. Stable, Beta, Dev, or Canary. The WebView2 controller will utilize the most stable version of the browser when installed on a machine.

### Future Planned Changes

We recognize that the Edge browser may not be available on all user machines your application is intended to run, or that control of the Edge browser install process may be difficult. To ensure your application will run on all machines, independent of the install status of the client Microsoft Edge browser, we will release the Microsoft Edge WebView2 Runtime. We will further update WebView2 to search for the stable version of the Runtime before searching for pre-release versions of the installed browser.

We also recognize that some app developers operate in constrained environments, and so intend to support two distribution options, evergreen and fixed version.

Evergreen is the recommended distribution model for most developers. In this mode updates to the WebView2 Runtime will be fully managed by Microsoft keeping you up to date automatically without additional effort from your application. With this self-updating model you can be assured that your app is taking advantage of the latest features and security updates for hosted web content.

For constrained environments we will also support a fixed version distribution model. In this model your application will select and package a specific WebView2 version. Updates to the WebView version will be the responsibility of the application and will be independent of any managed Microsoft update mechanisms. You should choose this model if it is crucial to be able to have absolute control over the browser version and update times your application is taking advantage of.