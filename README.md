# C++ STL Array Implementation

This project implements a custom version of the C++ Standard Template Library (STL) array container. The implementation provides similar functionality to `std::array` while serving as an educational example.

## Overview

The custom array is a fixed-size sequence container that encapsulates a statically allocated array. Key features include:

- Template-based implementation supporting any data type and size
- Fixed size specified at compile time
- Direct element access via subscript operator []
- Bounds-checked access via at() method
- Iterator support for traversing elements
- Front/back element access
- Size and empty status methods

## Class Structure

### `custom::array<T,N>`
The main array class template with two parameters:
- T: Type of elements
- N: Fixed size of array

Key methods:
- `operator[]`: Direct element access
- `at()`: Bounds-checked element access
- `front()`, `back()`: Access first/last elements
- `begin()`, `end()`: Iterator support
- `size()`, `empty()`: Container info

### `custom::array<T,N>::iterator`
Iterator class for traversing array elements. Supports:
- Forward iteration
- Element access via dereferencing
- Comparison operations
- Prefix/postfix increment

## Usage Example

```cpp
#include "array.h"

// Create array of 5 integers
custom::array<int, 5> arr;

// Access elements
arr[0] = 1;
arr.at(1) = 2;

// Iterate through elements
for (auto it = arr.begin(); it != arr.end(); ++it) {
    // Use *it to access element
}
```

## Testing

The implementation includes comprehensive unit tests in `testArray.h` that verify:
- Element access operations
- Iterator functionality  
- Bounds checking
- Memory management
- Edge cases

Run tests by building in debug mode with the DEBUG flag defined.

## Files

- `array.h`: Main array implementation
- `testArray.h`: Unit tests
- `spy.h`: Helper class for testing
- `unitTest.h`: Unit testing framework

## Building

The project includes Visual Studio solution files for building on Windows. Open `LabArray.sln` and build using Visual Studio 2019 or later.

## Notes

- This is an educational implementation focused on demonstrating STL container concepts
- The implementation aims to match `std::array`'s performance
- Error checking is included via bounds checking in at()
- Memory is statically allocated at compile time

#### Disclaimer

This README was initially generated using an AI Language Model (Claude 3.5 Sonnet) and subsequently edited by a human for accuracy and completeness. While the content accurately describes the codebase, the writing structure and initial draft were AI-assisted. The actual code implementation and testing were completed by a human developer.

## License

This code is provided for educational purposes. See included license file for terms of use. [TODO: add LICENSE]

## Author

Nathan Bird  
[nathanbirdka@gmail.com](mailto:nathanbirdka@gmail.com)