## Overview
This project is a C application that demonstrates basic OpenGL functionality. It uses the `AglWindow` library, which provides a cross-platform windowing system for OpenGL applications. The application sets up an OpenGL context and renders a simple triangle.

## Features
- Cross-platform support (Linux, Windows, Wine)
- Basic OpenGL rendering
- Use of `AglWindow` library

## Project Structure
```
Gui_OpenGL/
├── build/              # Build output directory for executables (.exe on Windows, .elf on Linux)
├── libs/               # Library source files (currently empty in this project)
├── src/                # Source code directory
│   ├── Main.c          # Entry point of the application
│   └── Gui_OpenGL.h    # Header file for the main window class
├── Makefile.linux      # Linux build configuration
├── Makefile.windows    # Windows build configuration
├── Makefile.wine       # Wine build configuration
└── README.md           # This file
```

### Prerequisites
- C/C++ Compiler and Debugger (GCC for Linux, Clang for other platforms)
- Make utility
- Standard development tools
- `AglWindow` library (must be installed or available in the project directory)

## Build & Run
### Linux
1. Ensure you have `AglWindow` installed.
2. Navigate to the project directory:
   ```sh
   cd Gui_OpenGL
   ```
3. Build the project using the provided Makefile:
   ```sh
   make -f Makefile.linux all
   ```
4. Run the executable:
   ```sh
   ./build/Main
   ```

### Windows
1. Ensure you have `AglWindow` installed.
2. Navigate to the project directory:
   ```sh
   cd Gui_OpenGL
   ```
3. Build the project using the provided Makefile:
   ```sh
   make -f Makefile.windows all
   ```
4. Run the executable from the build directory or use the debugger:
   ```sh
   build/Main.exe
   ```

### Wine (Cross-compilation for Windows on Linux)
1. Ensure you have `AglWindow` installed.
2. Navigate to the project directory:
   ```sh
   cd Gui_OpenGL
   ```
3. Build the project using the provided Makefile:
   ```sh
   make -f Makefile.wine all
   ```
4. Run the executable using Wine:
   ```sh
   wine build/Main.exe
   ```

### Emscripten (WebAssembly)
1. Ensure you have `AglWindow` installed.
2. Navigate to the project directory:
   ```sh
   cd Gui_OpenGL
   ```
3. Build the project using the provided Makefile:
   ```sh
   make -f Makefile.web all
   ```
4. Serve the output directory and open the `index.html` file in a web browser.

### Clean Rebuild
To clean the build directory and rebuild from scratch, use:
```sh
make -f Makefile.(os) clean
make -f Makefile.(os) all
```

This README provides a basic overview of the project structure, features, and how to build and run it on different platforms.