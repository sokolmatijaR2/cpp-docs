---
title: "/MIDL (Specify MIDL Command Line Options)"
ms.date: "09/05/2018"
f1_keywords: ["/midl", "VC.Project.VCLinkerTool.MidlCommandFile"]
helpviewer_keywords: ["-MIDL linker option", "MIDL", "/MIDL linker option", "MIDL linker option", "MIDL, command line options"]
ms.assetid: 22dc259e-b34c-4ed3-a380-4beb734482c1
---
# /MIDL (Specify MIDL Command Line Options)

Specifies a response file for MIDL command line options

## Syntax

> **/MIDL:\@**<em>file</em>

## Arguments

*file*<br/>
The name of the file that contains [MIDL command line options](/windows/desktop/Midl/general-midl-command-line-syntax).

## Remarks

All options for the conversion of an IDL file to a TLB file must be given in *file*; MIDL command-line options cannot be specified on the linker's command line. If /MIDL is not specified, the MIDL compiler will be invoked with only the IDL file name and no other options.

The file should contain one MIDL command-line option per line.

### To set this linker option in the Visual Studio development environment

1. Open the project's **Property Pages** dialog box. For details, see [Setting Visual C++ Project Properties](../../ide/working-with-project-properties.md).

1. Select the **Configuration Properties** > **Linker** > **Embedded IDL** property page.

1. Modify the **MIDL Commands** property.

### To set this linker option programmatically

- See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.MidlCommandFile%2A>.

## See also

[Setting Linker Options](../../build/reference/setting-linker-options.md)<br/>
[Linker Options](../../build/reference/linker-options.md)<br/>
[/IDLOUT (Name MIDL Output Files)](../../build/reference/idlout-name-midl-output-files.md)<br/>
[/IGNOREIDL (Don't Process Attributes into MIDL)](../../build/reference/ignoreidl-don-t-process-attributes-into-midl.md)<br/>
[/TLBOUT (Name .TLB File)](../../build/reference/tlbout-name-dot-tlb-file.md)<br/>
[Building an Attributed Program](../../windows/building-an-attributed-program.md)
