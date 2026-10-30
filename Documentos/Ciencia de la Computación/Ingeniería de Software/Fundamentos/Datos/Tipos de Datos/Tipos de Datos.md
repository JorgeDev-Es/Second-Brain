
## Ejemplos de tipos de datos
### C++
```C++
// Primitives
int my_integer = 328;
short my_short = 16;
long my_long = 1234567890;
long long my_long_long = 9876543210987654321;
char my_char = 'A';

float my_float = 3.39f;
double my_double = 3.1415926535;
long double my_long_double = 1.234567890123456L;

bool my_boolean = true;
bool another_boolean = false;

//Complex
int my_array[5] = {1, 2, 3, 4, 5};
int* my_pointer = &number;
int& my_reference = number;

// Standard Library
std::string my_string = "Hello from C++";
std::vector<int> my_vector = {1, 2, 3};
std::list<int> my_list = {10, 20, 30};
std::map<std::string, int> ages;
std::unordered_map<std::string, int> scores;
```
### C\#
```C#
// Primitives
int my_integer = 328;
short my_short = 16;
long my_long = 9007199254640991;
sbyte my_sbyte = -128;
byte my_byte = 255;

float my_float = 3.39f;
double my_double = 3.1415926535;
decimal my_decimal = 123.456m;

char my_char = 'A';
string my_string = "Hello from C#";
bool my_boolean = true;
```
### TypeScript
```TypeScript
// Primitives
let my_integer: number = 328
let my_float: number = 3.39
let my_bigint: bigint = 9007199254640991n
let my_string: string = "Hello from TypeScript"
let my_boolean: boolean = true

// Complex
let my_array: number[] = [1, 2, 3]
let my_tuple: [string, number, boolean] = ["Juan", 30, true]
```
### Python
```Python
# Primitives
my_integer: int = 328
my_float: float = 3.39
my_long: int = 9007199254640991
my_complex: complex = 1 + 2j

my_string: str = "Hello from Python"
my_boolean: bool = True

# Complex
my_list = [1, "manzana", 3.14, True]
my_tuple = (1, "manzana", 3.14, True)
my_dict = {"nombre": "Juan", "edad": 30, "ciudad": "Madrid"}
my_set = {1, 2, 3, 3, 4}

# Standard Library
my_default_dictionary = defaultdict(int)
my_deque = deque([1, 2, 3])
```