# JSON file structure

JSON file structure can be a bit confisuing

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
