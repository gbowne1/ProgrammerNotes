# JSON file structure

JSON code structure can be a bit confusing. This is commonly used in API's and is a great way to struture data.

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
