---
title: "Optimize Visual Studio performance | Microsoft Docs"
ms.custom: ""
ms.date: 11/15/2017
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "startup time [Visual Studio]"
  - "optimizing performance [Visual Studio]"
  - "speed up start time [Visual Studio]"
ms.assetid: d1508121-8499-4084-8eb5-fa89fa7b17d3
caps.latest.revision: 4
author: "gewarren"
ms.author: "gewarren"
manager: ghogen
f1_keywords: 
  - "vs.performancecenter"
ms.technology: 
  - "vs-ide-general"
ms.workload: 
  - "multiple"
---
# Optimize Visual Studio performance
Visual Studio is designed to start up as quickly and efficiently as possible. However, certain Visual Studio extensions and tool windows can adversely affect startup time when they are loaded. You can control the behavior of slow extensions and tool windows in the the  **Manage Visual Studio Performance** dialog box. For more general tips on improving performance, see [Visual Studio Performance Tips and Tricks](../ide/visual-studio-performance-tips-and-tricks.md).  

## Startup behavior

To avoid extending startup time, Visual Studio 2017 loads extensions using an _on demand_ approach. This behavior means that extensions don't open immediately after Visual Studio starts, but on an as-needed basis. Also, because tool windows left open in a prior Visual Studio session can slow startup time, Visual Studio opens tool windows in a more intelligent way to avoid impacting startup time.  

If Visual Studio detects slow startup, a pop-up message appears, alerting you to the extension or tool window that's causing the slowdown. The message provides a link to the **Manage Visual Studio Performance** dialog box. You can also access this dialog box by choosing **Help**, **Manage Visual Studio Performance** from the menu bar.  

![Manage Visual Studio Performance - popup reading 'We've noticed that extension ... is slowing Visual Studio'](../ide/media/vside_perfdialog_popup.png)

The dialog box lists the extensions and tools windows that are affecting startup performance. You can change extension and tool window settings to improve startup performance.  

## To change extension settings to improve startup, solution load, and typing performance

1. Open the **Manage Visual Studio Performance** dialog box by choosing **Help**, **Manage Visual Studio Performance** from the menu bar.  

    If an extension is slowing down Visual Studio startup, solution loading, or typing, the extension appears in the **Manage Visual Studio Performance** dialog box under **Extensions**, **Startup** (or **Solution Load** or **Typing**).  

    ![Manage Visual Studio Performance - extensions view](../ide/media/vside_perfdialog_extensions.png)

2. Choose the extension you want to disable, then choose the **Disable** button.  

You can always re-enable the extension for future sessions by using the Extension Manager or the Manage Visual Studio Performance dialog box.

## To change tool window settings to improve startup time

1. Open the **Manage Visual Studio Performance** dialog box by choosing **Help**, **Manage Visual Studio Performance** from the menu bar.  

    If a tool window is slowing down Visual Studio startup, the tool window appears in the **Manage Visual Studio Performance** dialog box under **Tool Windows**, **Startup**.  

2. Choose the tool window you want to change the behavior for.  

3. Choose one of the following three options:    

    - **Use default behavior:** The default behavior for the tool window. Keeping this option selected will not improve startup performance.  

    - **Do not show window at startup:** The specified tool window is always closed when you open Visual Studio, even if you left it open in a previous session. You can open the tool window from the appropriate menu when you need it.  
    
    - **Auto hide window at startup:** If a tool window was left open in a previous session, this option collapses the tool window's group at startup to avoid initializing the tool window. This option is a good choice if you use a tool window often. The tool window is still available, but no longer negatively affects Visual Studio startup time.  

    ![Manage Visual Studio Performance - tool windows view](../ide/media/vside_perfdialog_toolwindows.png)

> [!NOTE]
> Versions of Visual Studio prior to version 15.5 had a feature called **lightweight solution load**. This feature is no longer available in Visual Studio 2017 version 15.5 and later. In Visual Studio version 15.5 and later, large solutions that contain managed code load much faster than previously, even without lightweight solution load.  

## See Also
[Visual Studio Performance Tips and Tricks](../ide/visual-studio-performance-tips-and-tricks.md)
