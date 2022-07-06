# Dusk support for Windows APIs
Long-term goals for this project:
- Provide first-class support for all Windows APIs, from old school Win32 to new school WinUI 3 and WinRT.
- All APIs should be as easy to use and idiomatic from Dusk as possible, without introducing any overhead compared to C/C++.
- Do not depend on the Windows SDK from Microsoft, in order to provide a seamless user experience for Dusk programmers as well as avoid their restrictive license terms.
- Provide a great IDE experience, with go-to-definition and easy viewing of Microsoft's [official docs](https://github.com/MicrosoftDocs/sdk-api) when hovering over API calls, for example.
- Since ~all available sample code is written in languages other than Dusk, it should be incredibly easy to port code that uses a Windows API from C, C++ or C# to Dusk. Possible solution: provide a "raw" version of each API that closely matches its original form. Provide a fix-it that translates the raw call to a idiomatic Dusk call.
- IMO, Microsoft went way overboard with their splitting of the Win32 APIs into modules in [win32metadata](https://github.com/microsoft/win32metadata). I will likely flatten this hierarchy in Dusk by a considerable amount.

Short-term goals for this project:
- Just parse Windows.Win32.winmd.
