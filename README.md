# vtkm-example-compiation

## Enviroment
 - OS: Linux den 4.19.14-1-MANJARO #1 SMP PREEMPT Wed Jan 9 17:17:37 UTC 2019 x86_64 GNU/Linux
 - gcc=8.2.1
 - cmake=3.12.2

## Compilation
 - git clone https://gitlab.kitware.com/vtk/vtk-m.git vtkm
 - cd vtkm
 - mkdir build
 - cd build
 - cmake-gui .. # on official site there seem to be mistake
 - make # you can use -j[NUMBER OF CORES] to increase compile time, however 10G ram is not enough for multiple cores
 - make test
 - make install # optional

## cmake-gui options and flags
 1. pick Unix Makefiles
 2. press Configure
 3. set flags:
 
 - BUILD_SHARED_LIBS      true
 - VTKm_ENABLE_CPACK      true
 - VTKm_ENABLE_EXAMPLES   true
 - VTKm_ENABLE_RENDERING  true
 - VTKm_ENABLE_TESTING    true
 - VTKm_USE_64BIT_IDS     true
 - VTKm_Vectorization     none
 
 4. press Generate and quit
 
 ## Run examples
 Binary:
 - cd vtkm
 - ./build/examples/hello_world/HelloWorld
 - ./build/examples/game_of_life/GameOfLife
 - ./build/examples/multi_backend/MultiBackend

Source:
 - ./examples/hello_world/HelloWorld.cxx
 - ./examples/game_of_life/GameOfLife.cxx
 - ./examples/multi_backend/MultiBackend.cxx
