

[Visit the official KiT Tools website](https://darkcalam.github.io/KIT-Tools/)# KiT Tools

**An Arabic Windows desktop toolkit for monitoring your PC and managing everyday system tasks.**

[View the latest release](https://github.com/DarkCalam/KIT-Tools/releases/latest) · [Open the repository](https://github.com/DarkCalam/KIT-Tools)

KiT Tools brings live hardware and process monitoring together with practical Windows utilities in one desktop app. Its interface is designed for Arabic, with right-to-left layouts and English technical values where appropriate.

## Features

- Live CPU, GPU, memory, disk, and network readings, with a running-process list.
- Download manager with progress tracking and resume support where the source allows it.
- Startup app management, driver tools, and software install/uninstall views.
- Network diagnostics, printer management, screenshots, and quick Windows shortcuts.
- Cleanup tools with optional selections for actions that can remove user or system data.
- Theme and application settings.

## Requirements

- Windows 10 or later.
- The published release is the simplest way to try the application. Some system operations may ask for administrator approval when needed.

## Build from source

The desktop client uses WPF and targets `net10.0-windows`.

```powershell
dotnet restore KiT_Tools.csproj
dotnet build KiT_Tools.csproj -c Release
```

## العربية

**KiT Tools برنامج أدوات عربي لنظام Windows لمراقبة الحاسب وإدارة المهام اليومية.**

يجمع البرنامج مراقبة المعالج وكرت الشاشة والذاكرة والأقراص والشبكة والعمليات الجارية، إلى جانب أدوات التنزيل وإدارة بدء التشغيل والتنظيف والشبكة والطابعات ولقطات الشاشة.

### أبرز المزايا

- عرض مباشر لمؤشرات CPU وGPU والذاكرة والتخزين والشبكة.
- إدارة التنزيلات ومتابعة التقدم والاستكمال عندما يدعمه المصدر.
- أدوات بدء التشغيل والتعاريف وتثبيت البرامج وإزالتها.
- فحص الشبكة ومعلوماتها وأدوات الطابعات ولقطات الشاشة.
- خيارات تنظيف قابلة للتحديد، مع طلب موافقة قبل عمليات التنظيف المؤثرة.
- واجهة عربية من اليمين إلى اليسار وثيمات متعددة.

### المتطلبات والبناء

- Windows 10 أو أحدث.
- يستخدم المشروع WPF ويستهدف `net10.0-windows`؛ يتطلب بناء المصدر تثبيت .NET 10 SDK.

```powershell
dotnet restore KiT_Tools.csproj
dotnet build KiT_Tools.csproj -c Release
```

لتحميل النسخة المنشورة، راجع [أحدث إصدار](https://github.com/DarkCalam/KIT-Tools/releases/latest).
