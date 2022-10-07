# libgude

Serialise and Deserialise data formats from the Gudetama Tap mobile app

## Development installation:

```sh
pip install -e .
```

## Usage Example

```python
from libgude.cdio import *

string_object = Object(String("hello"))
print(string_object)  # Object(String('hello'))
print(string_object.to_source())  # Object('hello')

serialised_string_object = string_object.serialised()
print(serialised_string_object)  # b'\x00\x06\x00\x05hello'

print(Object.parse(serialised_string_object))  # Object(String('hello'))
```
