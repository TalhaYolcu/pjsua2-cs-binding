# PJSUA2-cs-build

This repository provides instructions and resources for building the C# bindings of the pjsip/pjproject library on Windows platforms. It has been tested and verified to work with Visual Studio 2022.

# Overview

The pjsua2-cs-build repository aims to simplify the process of building the C# bindings for the pjsip/pjproject library on Windows. This library is a versatile and powerful multimedia communication library written in C language, and the C# bindings allow developers to use its capabilities within a C# environment.

## Prerequisites

Before proceeding with the build process, ensure you have the following tools and libraries installed on your system:

Visual Studio 2022
The pjsip/pjproject library
Building the C# Bindings

## Follow these steps to build the C# bindings using this repository:

### 1. Clone the Repository:
```bash
git clone https://github.com/TalhaYolcu/pjsua2-cs-build.git
```
### 2. Open the Solution:
Navigate to the cloned repository folder and open the solution file pjsua2-cs-build.sln in Visual Studio 2022.

### 3. Configure Preprocessor Options:
In the config_site.h file, make sure the following definitions are set correctly:
```c
#define PJ_EXPORT_SPECIFIER __declspec(dllexport)
#define PJ_IMPORT_SPECIFIER __declspec(dllimport)
#define PJ_DLL 1
#ifdef _LIB
#define PJ_EXPORTING 1
#endif
```

### 4. Build the Solution:
Build the solution using the Visual Studio build tools. Ensure that your build configuration is set to the desired platform and configuration (e.g., Debug or Release).

### 5. Verify Build Success:
After the build process completes, verify that the C# bindings have been successfully generated.


## Notes

Make sure to have the required version of Visual Studio (e.g., Visual Studio 2022) installed on your system before starting the build process.
You may need to configure additional build settings depending on your project's requirements.
Libraries such as msvcrt.lib have been removed from the build. Additionally, the preprocessor options PJ_DLL and PJ_EXPORTING need to be correctly set for the build to succeed.
License


### Acknowledgments

We would like to express our gratitude to the developers of the pjsip/pjproject library for providing such a powerful multimedia communication toolset, and to the open-source community for their contributions.
