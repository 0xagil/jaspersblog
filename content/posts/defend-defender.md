---
title: "Defend Microsoft Defender"
date: 2020-07-07T16:20:03+00:00
tags: ["Mircosoft Defender", "Security", "Windows", "Powershell"]
author: "Me"
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "HowTo defend and disable Microsoft Defender"
canonicalURL: "https://jasperbraack.dev/defend-defender"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: false
UseHugoToc: true
---

Useful commands to defend Microsoft Defender

<!--post-->

## Factory Reset Microsoft Defender

<pre>
cmd /c "C:\Program Files\Windows Defender\MpCmdRun.exe" -RemoveDefinitions -All Set-MpPreference -DisableIOAVProtection $true
</pre>


## Add an Exception to a Directory or Process

<pre>
Add-MpPreference -ExclusionPath "C:\"
Add-MpPreference -ExclusionProcess "c:\internal\test.exe"
</pre>

## Disable Real Time Protection

<pre>
Set-MpPreference -DisableRealtimeMonitoring $true
</pre>

## Disable Cloud Protection
<pre>
Set-MpPreference -DisableBlockAtFirstSeen $true
</pre>

## Disable Behavior Monitoring
<pre>
Set-MpPreference -DisableBehaviorMonitoring $true
</pre>