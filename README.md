Just grab the code (and the Spike submodule).

Then run `cmake .` followed by `make`.
This will build Spike and the CPUTest executable.
You'll need to have CUDA installed.

Generally, I recommend having a separate 'build' directory
(If you want to do this, then do `cd build; cmake ..; make`).
(Otherwise, CMake will leave lots of clutter around in the top-level
source tree!)

Then just run `./CPUTest` to make sure it functions!

Have a look in CMakeLists.txt to see how the build works.

