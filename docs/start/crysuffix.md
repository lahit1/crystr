# Hold the Text via StringPack

## Why We Need a Suffix ?
It's because suffix make easy to make chain-processes such like ` "text"_cry(crySHA256)("key") `

## So, How to Use It Then ?
```cpp
#include <crystr/crystr>

...
{
	cry::StringPack mPack = "abcde"_cry;
}
...
```
!!! info
	As you guess, this only works on C++11+ compilers
