# SimpleCom

Console app for serial connection.

# How to use

1. Conenct serial adaptor to your PC
2. Start `SimpleCom.exe`
3. Setup serial console via setup dialog
4. Operate target device via the console
5. Press F1 to leave its serial session and to finish SimpleCom

# Start with command-line arguments

You can pass serial port and baud rate to SimpleCom, for example: `SimpleCom.exe COM1 115200`

# How to build

Use [SimpleCom.sln](https://github.com/YaSuenag/SimpleCom/blob/master/SimpleCom.sln) on your Visual Studio.  
I confirmed x64 build on VS 2019.

# How to use on [Windows Terminal](https://github.com/microsoft/terminal)

You can integrate SimpleCom to Windows Terminal if you add following JSON values to `settings.json`.

```
{

 ...

  "profiles": [

 ...

    {
      "closeOnExit" : true,
      "commandline": "C:\\path\\to\\SimpleCom.exe",
      "cursorColor": "#FFFFFF",
      "cursorShape": "filledBox",
      "guid": "{a3177c2a-f5f4-4c95-b877-0d12d6413363}",
      "name": "SimpleCom"
    }

 ...

```

See [Windows Terminal official document](https://github.com/microsoft/terminal/blob/master/doc/user-docs/UsingJsonSettings.md) for more details.

# Notes

* SimpleCom sends / receives VT100 escape sequences. So the serial device to connect via SimpleCom needs to support VT100 or compatible shell.
* SimpleCom supports ANSI chars only, so it would not work if multibyte chars (e.g. CJK chars) are given.

# License

GNU General Public License v2.0
