# VS Code Extensions

Here are some VS Code extensions that are useful:

- Color Highlight
- Debug Controls in Titlebar
- Error Lens
- indent-rainbow
- markdownlint
- Markdown Preview Enhancedd
- One Dark Pro theme
- Todo Tree
- Trailing Spaces

Here are some helpful extensions for C/C++:

- C/C++ Extension Pack
- Code Runner
- Doxygen Documentation Generator
- CMake (disable for now)
- CMake Tools (disable for now)

## Project Configuration Topics

Here are some topics for discussion when configuring C++ projects in VS Code:

- Tasks: Configure Default Build Task (task.json)
- C/C++: Select Intellisense Configuration
- C/C++: Add Debug Configuration (launch.json)
- Settings > Code Runner: Run in Terminal (Workspace Settings)
- Run Code (Code Runner)

- Workspace settings override user settings
- Language specific editor settings

----------

## Windows Setup

[Using GCC with MinGW](https://code.visualstudio.com/docs/cpp/config-mingw)

- Install the VS Code Extensions given above
- Installing the MinGW-w64 toolchain
- Check your MinGW installation
- Create a Hello World app
- Explore the debugger
- Customize debugging with launch.json

## Linux Setup

```zsh
    # update and upgrade the system
    sudo apt update && sudo apt-get upgrade --fix-missing

    # install essential GCC dev tools
    sudo apt install build-essential gdb
```

```zsh
    # Force any missing install, autoremove unused package,
    # autoclean, clean update, and reboot system
    sudo apt -f install
    sudo apt autoremove
    sudo apt -y autoclean
    sudo apt -y clean
    sudo apt update
    sudo reboot
```

## macOS Setup

The default Xcode clang++ compiler should work, but we can also make use of clang++ from the Linux llvm toolchain.

Install llvm using Homebrew.

```zsh
    brew install llvm
```

Add the following to `.zshrc` to use llvm and clang++.

```zsh
    # Add Homebrew executable directory, coreutils, and usr folders to path
    PATH=/usr/local/opt/coreutils/libexec/gnubin:/usr/local/opt:/usr/local/bin:/usr/local/sbin:$PATH

    # Add Homebrew llvm toolchain
    export PATH="/usr/local/opt/llvm/bin:$PATH"
```

## References

[Using GCC with MinGW](https://code.visualstudio.com/docs/cpp/config-mingw)

[CMake Tools for Visual Studio Code](https://github.com/microsoft/vscode-cmake-tools/blob/main/docs/README.md)

----------

[C++ with Visual Studio Code on macOS](https://medium.com/@sagads80/c-with-visual-studio-code-on-macos-85b2e9e84cc2)

[Build and Debug C++ on Visual Studio Code for Mac](https://medium.com/gdplabs/build-and-debug-c-on-visual-studio-code-for-mac-77e05537105e)

[Using Clang in Visual Studio Code](https://code.visualstudio.com/docs/cpp/config-clang-mac)

[User and Workspace Settings](https://code.visualstudio.com/docs/getstarted/settings)

----------

[Debugging with LLDB-MI on macOS](https://code.visualstudio.com/docs/cpp/lldb-mi)
