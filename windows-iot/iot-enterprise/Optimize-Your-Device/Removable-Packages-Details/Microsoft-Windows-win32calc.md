---
title: Package - Legacy Calculator App
author: twarwick
ms.author: twarwick
ms.date: 1/12/2023
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Removable Package Details for Microsoft-Windows-win32calc
keywords: IoT Enterprise, removable packages, storage
---

# Package: Legacy Calculator App

## Description
Legacy calculator application

**Package Name:** Microsoft-Windows-win32calc

**Size:** Approximately 1,394 KB


## Removing Package

### Online Servicing 
Use the [DISM command-line tool](/windows-hardware/manufacture/desktop/what-is-dism) with the ```/Online``` command-line parameter to remove a single package via online servicing.

```powershell
Dism.exe /Online /LogPath:%WINDIR%\Temp\Microsoft-Windows-win32calc.log /NoRestart /Disable-Feature /FeatureName:Microsoft-Windows-win32calc /PackageName:@Package
````
### Offline Servicing
Use the [DISM command-line tool](/windows-hardware/manufacture/desktop/what-is-dism) with the ```/Image:<image path>``` command-line parameter to remove a single package via offline servicing.

```powershell
Dism.exe /Image:c:\offline /LogPath:%WINDIR%\Temp\Microsoft-Windows-win32calc.log /NoRestart /Disable-Feature /FeatureName:Microsoft-Windows-win32calc /PackageName:@Package
````

## File List
| File Name | Installed Location |
|-----------|--------------------|
| calculator.lnk | %programdata%\microsoft\windows\start menu\programs\accessories\calculator.lnk  |
| win32calc.exe  | %windir%\system32\win32calc.exe |

## More Resources
- [Removable Packages](/windows/iot/iot-enterprise/Optimize-Your-Device/Removable-Packages)
- [Reduce Disk Footprint](/windows/iot/iot-enterprise/Optimize-Your-Device/Reduce-Disk-Footprint)
- [Device Optimization Overview](/windows/iot/iot-enterprise/Optimize-Your-Device/Overview)