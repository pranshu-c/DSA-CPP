# DSA-CPP: Comprehensive Data Structures & Algorithms 🚀

![Build Status](https://github.com/pranshu-c/DSA-CPP/actions/workflows/build.yml/badge.svg)
![C++ Standard](https://img.shields.io/badge/C%2B%2B-17-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

A top-tier, professional repository containing implementations of various Data Structures and Algorithms in C++17. This repository is designed to demonstrate clean, standard-compliant, and production-ready C++ code.

## 🌟 Key Features

- **Modern C++17:** Uses standard containers (`std::vector`, `std::string`) instead of C-style Variable Length Arrays (VLAs).
- **Clean Architecture:** Strict avoidance of global namespace pollution (`using namespace std;`).
- **CMake Build System:** Standardized, platform-independent build configuration using CMake.
- **Continuous Integration:** Automated GitHub Actions pipeline to guarantee compilation across different platforms.

## 📂 Project Structure

- `Trees/`: Binary Trees, BSTs, Traversals, and advanced tree problems.
- `String/`: String manipulation, parsing, and algorithmic string problems.
- `dynamic_programming/`: DP implementations like Knapsack, LIS, LCS, Coin Change, and more.
- `practise(functions)/`: Mathematical utilities, number conversions, and bitwise operations.
- `questions/`: Assorted standard coding interview problems.

## 🛠️ Prerequisites

To build the projects locally, you will need:
- A C++17 compatible compiler (GCC, Clang, or MSVC)
- [CMake](https://cmake.org/download/) (v3.10 or higher)

## 🚀 Building the Code

This repository uses CMake to automatically build all standalone `.cpp` files into individual executables.

```bash
# 1. Clone the repository
git clone https://github.com/pranshu-c/DSA-CPP.git
cd DSA-CPP

# 2. Configure the project
cmake -B build

# 3. Compile the code
cmake --build build
```

The executables will be located inside the `build/` directory (or `build/Debug/` on Windows MSVC).

## 🧑‍💻 Contributing

When contributing to this repository, please ensure that:
1. You do not use `using namespace std;` in the global scope.
2. You prefer standard C++ containers (`std::vector`, `std::array`) over raw C-arrays or VLAs.
3. Your code is formatted according to the provided `.clang-format` (Google Style Guide).
