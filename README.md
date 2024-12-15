# aznoqmous/vcpkg-boilerplate

a boilerplate cpp + vcpkg project

https://learn.microsoft.com/en-us/vcpkg/get_started/get-started-vscode?pivots=shell-cmd

## Setup

1. `git clone https://aznoqmous/vcpkg-boilerplate <project-name>`
2. Replace <VCPKG_DIRECTORY> inside `CMakePresets.json` and `CMakeUserPresets.json`
3. Replace <PROJECT_NAME> inside `CMakeLists.txt`
4. Run visual studio `>CMake: Select Active Folder` command
5. Run visual studio `>CMake: Build` command with the "default" preset

Make sure that `CMakePresets.json` `configuration.generator` matches your Visual Studio version

## Include path
After installing vcpkg dependencies

Create a `.vscode/c_cpp_properties.json` file and add the vcpkg include folder as an include path :

```json
{
    "version": 4,
    "configurations": [
        {
            "includePath": [
                "${workspaceFolder}/vcpkg_installed/x64-windows/include"
            ]
        }
    ]
}
```