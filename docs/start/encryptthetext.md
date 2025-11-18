# Finally Encrypting The Text
Now we know all the things to encrypt a text efficiently, let's start it.
```cpp
// auto result = "Message"_cry(&e)("pwd"_cry);
auto pack = "Message"_cry(&e);
auto result = pack("password"_cry);


for(int i=0; i < result.size(); i++)
	std::cout << std::hex << (int)result.data()[i] << std::endl;
```
