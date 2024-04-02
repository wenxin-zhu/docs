# vscode json文件配置

> c_cpp_properties.json

```json
{
    "configurations": [
        {
            "name": "Win32",
            "includePath": [
                "${workspaceFolder}/**" // 头文件目录
            ],
            "defines": [
                "_DEBUG",
                "UNICODE",
                "_UNICODE"
            ],
            "cStandard": "c17",
            "cppStandard": "gnu++14",
            "intelliSenseMode": "windows-gcc-x64",
            "compilerPath": "C:/Users/ZWX/AppData/Local/Programs/mingw64/bin/g++.exe" // 自定义路径
        }
    ],
    "version": 4
}
```

> launch.json

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "gcc - Build and debug active file",
            "type": "cppdbg",
            "request": "launch",
            "program": "${fileDirname}/${fileBasenameNoExtension}",
            "args": [],
            "stopAtEntry": false,
            "cwd": "${workspaceFolder}",
            "environment": [],
            "externalConsole": false,
            "MIMode": "gdb",
            "setupCommands": [
                {
                    "description": "Enable pretty-printing for gdb",
                    "text": "-enable-pretty-printing",
                    "ignoreFailures": true
                }
            ],
            "preLaunchTask": "C/C++: gcc build active file",
            "miDebuggerPath": "C:/Users/ZWX/AppData/Local/Programs/mingw64/bin/gdb.exe" //gbd路径
        }
    ]
}
```

> settings.json

```json
{
    "files.associations": {
        "iostream": "cpp",
        "initializer_list": "cpp",
        "ostream": "cpp"
    }
}
```

> tasks.json

```json
{
    "tasks": [
        {
            "type": "cppbuild",
            "label": "C/C++: gcc build active file",
            "command": "C:/Users/ZWX/AppData/Local/Programs/mingw64/bin/g++.exe", // g++路径
            "args": [
                "-fdiagnostics-color=always",
                "-g",
                "${file}",
                "-o",
                "${fileDirname}\\${fileBasenameNoExtension}.exe"
            ],
            "options": {
                "cwd": "C:/Users/ZWX/AppData/Local/Programs/mingw64/bin" // mingw/bin路径
            },
            "problemMatcher": [
                "$gcc"
            ],
            "group": {
                "kind": "build",
                "isDefault": true
            },
            "detail": "调试器生成的任务。"
        }
    ],
    "version": "2.0.0"
}
```

