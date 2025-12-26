# Lightweight System Monitor

A lightweight desktop application to monitor system resources (CPU, RAM, GPU) and manage running processes, built in C++ with Qt Widgets. Designed to be fast, minimal, and efficient.

## Features

### Core Features
- CPU monitoring (total and per-core usage)
- RAM usage monitoring (used, free, cached)
- Process listing with:
  - PID, name
  - CPU and RAM usage
  - Ability to terminate processes safely
- Minimal memory and CPU footprint
- Background monitoring thread for efficiency

### Optional Features
- GPU monitoring (NVIDIA/AMD)
- Alerts for high usage
- Logging to CSV/JSON

## Tech Stack

- **Language:** C++17
- **UI Framework:** Qt Widgets
- **OS APIs:** Windows API (`Windows.h`, `Toolhelp32Snapshot`, `GetSystemTimes`, `GlobalMemoryStatusEx`)
- **Build System:** CMake
- **Threading:** `std::thread`, `std::mutex`
- **Memory Management:** RAII, stack allocation, `std::unique_ptr`

## Development Guidelines

- **No dynamic memory allocations in hot loops**
- **Separate core logic from UI**
- **Polling interval:** 1 second recommended
- **Handle Windows errors gracefully**
- **RAII for all HANDLEs**

## Collaboration

I am open to collaborating! If you’re interested in contributing to this project, feel free to reach out or open a pull request. Contributions to features, performance improvements, or UI enhancements are welcome.

## License
MIT License
