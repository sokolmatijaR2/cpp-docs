---
title: "/Fp (Name .Pch File)"
ms.date: "11/04/2016"
f1_keywords: ["VC.Project.VCCLCompilerTool.PrecompiledHeaderFile", "/fp", "VC.Project.VCCLWCECompilerTool.PrecompiledHeaderFile"]
helpviewer_keywords: ["Fp compiler option [C++]", "-Fp compiler option [C++]", "naming precompiler header files", "PCH files, naming", "names [C++], PCH", ".pch files, naming", "precompiled header files, naming", "/Fp compiler option [C++]"]
ms.assetid: 0fcd9cbd-e09f-44d3-9715-b41efb5d0be2
---
# /Fp (Name .Pch File)

Provides a path name for a precompiled header instead of using the default path name.

## Syntax

> **/Fp**<em>pathname</em>

## Remarks

Use this option with [/Yc (Create Precompiled Header File)](../../build/reference/yc-create-precompiled-header-file.md) or [/Yu (Use Precompiled Header File)](../../build/reference/yu-use-precompiled-header-file.md) to provide a path name for a precompiled header instead of using the default path name. You can also use **/Fp** with **/Yc** to specify the use of a precompiled header file that differs from the **/Yc**<em>filename</em> argument and from the base name of the source file.

If you do not specify an extension as part of the path name, an extension of .pch is assumed. If you specify a directory without a file name, the default file name is VC*x*0.pch, where *x* is the major version of Visual C++ in use.

You can also use the **/Fp** option with **/Yu**.

### To set this compiler option in the Visual Studio development environment

1. Open the project's **Property Pages** dialog box. For details, see [Working with Project Properties](../../ide/working-with-project-properties.md).

1. Click the **C/C++** folder.

1. Click the **Precompiled Headers** property page.

1. Modify the **Precompiled Header File** property.

### To set this compiler option programmatically

- See <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.PrecompiledHeaderFile%2A>.

## Example

If you want to create a precompiled header file for a debugging version of your program and you are compiling both header files and source code, you can specify a command such as:

```
CL /DDEBUG /Zi /Yc /FpDPROG.PCH PROG.CPP
```

## Example

The following command specifies the use of a precompiled header file named MYPCH.pch. The compiler assumes that the source code in PROG.cpp has been precompiled through MYAPP.h and that the precompiled code resides in MYPCH.pch. It uses the content of MYPCH.pch and compiles the rest of PROG.cpp to create an .obj file. The output of this example is a file named PROG.exe.

```
CL /YuMYAPP.H /FpMYPCH.PCH PROG.CPP
```

## See also

[Output-File (/F) Options](../../build/reference/output-file-f-options.md)<br/>
[Compiler Options](../../build/reference/compiler-options.md)<br/>
[Setting Compiler Options](../../build/reference/setting-compiler-options.md)<br/>
[Specifying the Pathname](../../build/reference/specifying-the-pathname.md)
