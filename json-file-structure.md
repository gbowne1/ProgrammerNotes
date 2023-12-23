# JSON file structure

JSON code structure can be a bit confusing. This is commonly used in API's and is a great way to struture data.

JSON (JavaScript Object Notation) is a text-based data exchange format derived from the JavaScript object syntax. It is a collection of key-value pairs where the key must be a string type, and the value can be a number, string, boolean, array, object, or null.

The structure of JSON is similar to JavaScript object literal format, and it allows the construction of a data hierarchy using various data types. JSON is language-independent and can be used in many programming languages. It is commonly used for transmitting data in web applications and can be easily converted to and from JavaScript objects using the JSON.parse() and JSON.stringify() methods

The basic structure of a JSON object is defined by key-value pairs enclosed in curly braces, while arrays are enclosed in square brackets. Each key and value must be separated by a colon, and multiple key-value pairs are separated by a comma. JSON is widely used for sending data between computers due to its simplicity and readability for both humans and machines

This is a JSON object file:

```json
{
 "name": "John",
 "age": 30,
 "city": "New York"
}
```

This is a JSON array:

```json
[
 "apple",
 "banana",
 "cherry"
]
```

This is a JSON array with objects

```jsonc
[
 {
  "name": "John",
  "age": 30,
  "city": "New York"
 },
 {
  "name": "Jane",
  "age": 25,
  "city": "Seattle"
 }
]
```

This is JSONC but includes comments

```jsonc
{
 "name": "John", // This is a comment
 "age": 30,
 "city": "New York",
 "hobbies": [
  "programming", // This is a comment,
  "reading",
  "traveling" /* This is a multi-line comment. */
 ]
}
```
