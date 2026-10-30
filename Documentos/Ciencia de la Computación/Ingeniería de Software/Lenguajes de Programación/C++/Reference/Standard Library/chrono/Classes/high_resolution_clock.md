# `high_resolution_clock` class
Class `high_resolution_clock` represents the clock with the smallest tick period provided by the implementation.
## Member functions
`now` returns a std::chrono::time_point representing the current value of the clock.
## Examples
```C++
#include <chrono>

using namespace std;
using namespace std::chrono;

int main() {
	auto start = high_resolution_clock::now();
	
	// Code
	
	auto end = high_resolution_clock::now();
	auto duration = duration_cast<milliseconds>(end - start);
	
	cout << "Time: " << duration.count() << " ms" << endl;
}
```