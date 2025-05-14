
```bash
mkdir build
cd build
cmake .. -G "Visual Studio 17 2022" -A x64
cmake --build . --config Release  -- /p:WarningLevel=0
.\\release\\capture_data.exe
```
