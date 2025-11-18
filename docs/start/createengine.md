# What is a cry::Engine
We were need a interface to support flexible and extensible encryption, so we come with this interface, it has a function pointer named proc as member.

# Let's Create an Engine
## One Way Encryption

First we need to define a processor function
```cpp
cry::StringPack_data proc(cry::StringPack_data text, cry::StringPack_data key) {

	int shift = 5;

	char *result = new char[ text.size() ];
	for (int i=0; i < text.size(); i++) {
		char &c = result[i];

		if(c >= 'a' || c <= 'g')
			++shift;

		result[i] = text[i] + shift;
	}

	return cry::StringPack_data(result, text.size());
}
```

Now we can create an Engine and integrate our "proc" function with it
```cpp
int main() {
	cry::Engine e;

	e.proc = proc;
}
```
