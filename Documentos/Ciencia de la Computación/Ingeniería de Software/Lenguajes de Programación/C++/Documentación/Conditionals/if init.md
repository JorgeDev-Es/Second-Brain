# `if-init` statement
```C++
if (init-statement; condition) {
	// Code to execute if condition is true
} else {
	// Code to execute if condition is false
}
```
## Key points
## Examples
```C++
for (int i = 0; i < nums.size(); i++) {
	if (int complement = target - nums[i]; seenNumbers.contains(complement)) {
		return {seenNumbers[complement], i};
	} else {
		seenNumbers.insert({nums[i], i});
	}
}
```