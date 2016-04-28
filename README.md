# MyCPLApplet

## Description
There is an example of creating control panel applets in Windows.

## Requiremets
* [Visual Studio 2015 IDE](https://www.visualstudio.com/en-us/downloads/download-visual-studio-vs.aspx)

## How to get it
1. Download/Clone this repository.
2. Open solution file `.sln`.
3. Build the solution.

## How to create your own CPL applet
1. Open [Visual Studio 2015 IDE](https://www.visualstudio.com/en-us/downloads/download-visual-studio-vs.aspx)
2. Start project wizard

        File->New->Project
3. Select Visual C++ MFC Dll

        Visual C++->MFC->MFC DLL
4. Press `OK` and `Finish`.

## How to debug CPL applets in Visual Studio IDE
1. Open project properties.
2. In `General` tab change `Target Extension` to `.cpl`.
3. In `Debugging` tab add

        Command : <Path to Rundll32.exe>\Rundll32.exe
        Command Arguments : shell32.dll, Control_RunDLL "$(TargetPath)"
4. Press `Ok`.

### Remarks
Here you can see examples of `Command`
    
        x86 configuration : C:\Windows\System32\Rundll32.exe
        x64 configuration : C:\Windows\SysWOW64\Rundll32.exe
        