# CERA

CERA is a C++20 game engine built from the ground up. Each commit is an episode in the video series that goes with it.

CERA starts from an empty folder and spends time on the parts of an engine that usually stay hidden: how the project is built, how memory and ownership work, how the codebase is structured and why each architectural decision was made. The engine grows one small, working step at a time, and every step is a commit you can check out and build yourself.

## Requirements

- CMake 3.24 or newer
- A C++20 compiler: MSVC, Clang or GCC
- Windows, Linux or macOS

## Building

```bash
git clone https://github.com/Dyronix/cera.git
cd cera

cmake -S . -B build
cmake --build build
```

The first command configures the project. It reads `CMakeLists.txt` from the current folder (`-S .`) and writes every generated file into `build/` (`-B build`). The second command compiles whatever was configured.

Because all build output lives in `build/`, the source tree stays clean. If the build ever gets into a strange state, delete `build/` and run both commands again.

The executable ends up in `build/`. With multi-config generators such as Visual Studio, it goes in a subfolder per configuration, for example `build/Debug/`. To build a specific configuration:

```bash
cmake --build build --config Release
```

## Following along

Each commit matches one episode. To see the code as it was at the end of an episode, find its commit and check it out:

```bash
git log --oneline
git checkout <commit>
```

`git checkout main` brings you back to the latest version.

## License

CERA is released under the [MIT License](LICENSE).
