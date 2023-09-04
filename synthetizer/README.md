# Windows instructions

1. Install CMake and MS Build Tools
2. Set these env vars in $profile if using PowerShell

```ps1
$env:path += ";C:\Program Files\CMake\bin"
$env:path += ";C:\Users\juanc\Desktop\facultad\TESIS\model_explorer\external\libtorch\lib" # change this to this folder synthetizer\external\libtorch\lib
$env:CUDA_PATH = "C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v12.2"
$env:CudaToolkitDir = "C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v12.2"
$env:NVTOOLSEXT_PATH = "C:\Program Files\NVIDIA Corporation\NvToolsExt"
$env:path += ";$CUDA_PATH;$CudaToolkitDir;$NVTOOLSEXT_PATH"
```

3. Compile with:

```sh
cmake -B cmake-build
cmake --build cmake-build
```

4. Run using terminal

```
.\cmake-build\model_explorer_artefacts\Debug\model_explorer.exe
```

5. Load `json` file of trained model
