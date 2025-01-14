# C++ STL Vector Implementation

This project implements a custom version of the C++ Standard Template Library (STL) vector container. The implementation provides exactly the same memory and performance characteristics as `std::vector`.

## Overview

The custom vector is a sequence container that encapsulates a dynamically allocated array. Key features include:

- Template-based implementation supporting any data type
- Customizable allocator type for memory management
- Dynamic size that grows as needed
- Direct element access via subscript operator []
- Bounds-checked access via at() method
- Iterator support for traversing elements
- Front/back element access
- Size, capacity and empty status methods

## Class Structure

### `custom::vector<T, A>`
The main vector class template with two parameters:
- T: Type of elements
- A: Allocator (default `std::allocator<T>`)

Key methods:
- `operator[]`: Direct element access
- `push_back()`: Add element to end
- `pop_back()`: Remove last element
- `front()`, `back()`: Access first/last elements
- `begin()`, `end()`: Iterator support
- `size()`, `capacity()`, `empty()`: Container info
- `reserve()`, `resize()`: Capacity management
- `clear()`: Remove all elements

### `custom::vector<T>::iterator`
Iterator class for traversing vector elements. Supports:
- Forward iteration
- Element access via dereferencing
- Comparison operations
- Prefix/postfix increment

## Usage Example

```cpp
#include "vector.h"

// Create vector of integers
custom::vector<int> v;

// Add elements
v.push_back(1);
v.push_back(2);

// Access elements
int first = v[0];
int last = v.back();

// Iterate through elements
for (auto it = v.begin(); it != v.end(); ++it) {
    // Use *it to access element
}
```

## Testing

The implementation includes comprehensive unit tests in `testVector.h` that verify:
- Element access operations
- Iterator functionality  
- Memory management
- Growth behavior
- Edge cases

Run tests by building in debug mode with the DEBUG flag defined.

## Files

- `vector.h`: Main vector implementation
- `testVector.h`: Unit tests
- `spy.h`: Helper class for testing
- `unitTest.h`: Unit testing framework

## Building

The project includes Visual Studio solution files for building on Windows. Open `LabVector.sln` and build using Visual Studio 2019 or later.

## Notes

- This is an educational implementation focused on demonstrating STL container concepts
- The implementation aims to match `std::vector`'s interface and performance
- Memory allocation is handled through a user-specified allocator type (defaults to `std::allocator<T>`)

#### Disclaimer

This README was initially generated using an AI Language Model (Claude 3.5 Sonnet) and subsequently edited by a human for accuracy and completeness. While the content accurately describes the codebase, the writing structure and initial draft were AI-assisted. The actual code implementation and testing were completed by human developers.

## License

This code is provided for educational purposes. See included license file for terms of use. [TODO: add LICENSE]

## Authors

Nathan Bird  
[nathanbirdka@gmail.com](mailto:nathanbirdka@gmail.com)

Brock Hoskins  
[]()