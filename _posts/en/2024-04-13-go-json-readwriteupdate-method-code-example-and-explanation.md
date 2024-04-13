---
title: "[go] json read/write/update method (code example and explanation)"
author: 46ebu
date: 2024-04-13 00:43:20 +0000
categories: [go]
tags: [go]
render_with_liquid: false
---

![Intro](/assets/img/post/go.png)
### Introduction
JSON (JavaScript Object Notation) is a lightweight data interchange format that is easy for humans to read and write and easy for machines to parse and generate. In Go, handling JSON data involves reading, writing, and updating JSON content. In this blog post, we will explore how to perform these operations using code examples and explanations.

### Reading JSON Data
To read JSON data in Go, we can use the 'encoding/json' package. The 'Unmarshal' function is used to decode JSON data into a Go structure. Here is an example code snippet to demonstrate how to read JSON data:

```go
package main

import (
	"encoding/json"
	"fmt"
)

type Person struct {
	Name string `json:"name"`
	Age  int    `json:"age"`
}

func main() {
	jsonData := []byte(`{"name": "Alice", "age": 30}`)
	var person Person
	err := json.Unmarshal(jsonData, &person)
	if err != nil {
		fmt.Println("Error:", err)
		return
	}
	fmt.Println("Name:", person.Name)
	fmt.Println("Age:", person.Age)
}
```

Output:
```
Name: Alice
Age: 30
```

### Writing JSON Data
To write JSON data in Go, we can use the 'encoding/json' package as well. The 'Marshal' function is used to encode a Go structure into JSON data. Here is an example code snippet to demonstrate how to write JSON data:

```go
package main

import (
	"encoding/json"
	"fmt"
)

type Person struct {
	Name string `json:"name"`
	Age  int    `json:"age"`
}

func main() {
	person := Person{Name: "Bob", Age: 25}
	jsonData, err := json.Marshal(person)
	if err != nil {
		fmt.Println("Error:", err)
		return
	}
	fmt.Println(string(jsonData))
}
```

Output:
```
{"name":"Bob","age":25}
```

### Updating JSON Data
To update JSON data in Go, we can first read the JSON content, make the necessary changes to the corresponding Go structure, and then write the updated content back to a JSON format. Here is an example code snippet to demonstrate how to update JSON data:

```go
package main

import (
	"encoding/json"
	"fmt"
)

type Person struct {
	Name string `json:"name"`
	Age  int    `json:"age"`
}

func main() {
	jsonData := []byte(`{"name": "Alice", "age": 30}`)
	var person Person
	err := json.Unmarshal(jsonData, &person)
	if err != nil {
		fmt.Println("Error:", err)
		return
	}
	person.Age = 40
	updatedData, err := json.Marshal(person)
	if err != nil {
		fmt.Println("Error:", err)
		return
	}
	fmt.Println(string(updatedData))
}
```

Output:
```
{"name":"Alice","age":40}
```

### Conclusion
In this blog post, we have explored how to read, write, and update JSON data in Go using code examples and explanations. By leveraging the 'encoding/json' package, developers can easily work with JSON data in their Go applications, allowing for seamless integration with external APIs and data sources. This knowledge is essential for anyone working with JSON data in Go projects.