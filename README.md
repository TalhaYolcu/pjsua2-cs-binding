# pjsua2-cs-build
This repository shows how to build C# binding of the pjsip/pjproject on Windows platforms. Tested with Visual Studio 2022

ignore libraries : msvcrt.lib removed
PJ_DLL and PJ_EXPORTING should be added as preprocessor options

config_site.h 

#define PJ_EXPORT_SPECIFIER  __declspec(dllexport)
#define PJ_IMPORT_SPECIFIER  __declspec(dllimport)
#define PJ_DLL  1
#ifdef _LIB
#define PJ_EXPORTING 1
#endif
