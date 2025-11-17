# Hold the Text via StringPack

## Why Wee Need [StringPack](/api/stringpack)

Since std::string isn't compatible with constexpr functions we were need another struct to hold both string pointer and string length so we got ' cry::StringPack' / ' cryStringPack '.
!!! note
	Notice that [cry::StringPack](/api/stringpack) / [cryStringPack](/api/stringpack) is defined to [std::string_view](https://en.cppreference.com/w/cpp/string/basic_string_view.html)
	for C++17 and newer

## So, How to Use It Then ?


### C implementation
```c
#include <crystr/crystr>

...
{
	cryStringPack mPack("abcde", 5);
}
...
```

### C++ implementation
```cpp
#include <crystr/crystr>

...
{
	cry::StringPack mPack = "abcdef";
}
...
```
!!! warning
	Since C++ < 17 implementation uses std::string ( which a class that doesn't compatible with constexpr ) as parameter, the function can break the project's whole point ( compile-time encryption )

### C++ implementation
```cpp
#include <crystr/crystr>

...
{
	cry::StringPack mPack("abcde", 5);
}
...
```
