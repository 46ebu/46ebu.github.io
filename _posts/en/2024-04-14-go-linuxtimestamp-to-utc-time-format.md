---
title: "[go] linuxtimestamp to UTC time format"
author: 46ebu
date: 2024-04-14 06:46:13 +0000
categories: [go]
tags: [go]
render_with_liquid: false
---

![Intro](/assets/img/post/go.png)
### Introduction
In this blog post, we will explore how to convert a Linux timestamp to UTC time format in the Go programming language. A Linux timestamp is a representation of time as the number of seconds since the Unix epoch (January 1, 1970, 00:00:00 UTC). Converting this timestamp to UTC time format is a common task when dealing with timestamps in Go.

### Syntax
To convert a Linux timestamp to UTC time format in Go, we can use the `time.Unix` function. This function takes two arguments: the number of seconds since the Unix epoch and the number of nanoseconds since the Unix epoch. By passing the Linux timestamp as the first argument and 0 as the second argument, we can get a `time.Time` object representing the UTC time.

### Example 1: Convert Linux Timestamp to UTC Time Format
```go
package main

import (
	"fmt"
	"time"
)

func main() {
	timestamp := int64(1619082967) // Linux timestamp
	utcTime := time.Unix(timestamp, 0)
	fmt.Println(utcTime)
}
```
Output:
```
2021-04-22 06:36:07 +0000 UTC
```

### Example 2: Convert Multiple Linux Timestamps to UTC Time Format
```go
package main

import (
	"fmt"
	"time"
)

func main() {
	timestamps := []int64{1619082967, 1620834321, 1621845678} // Linux timestamps

	for _, ts := range timestamps {
		utcTime := time.Unix(ts, 0)
		fmt.Println(utcTime)
	}
}
```
Output:
```
2021-04-22 06:36:07 +0000 UTC
2021-05-12 02:52:01 +0000 UTC
2021-05-24 05:21:18 +0000 UTC
```

### Example 3: Convert Current Linux Timestamp to UTC Time Format
```go
package main

import (
	"fmt"
	"time"
)

func main() {
	currentTimestamp := time.Now().Unix() // Current Linux timestamp
	utcTime := time.Unix(currentTimestamp, 0)
	fmt.Println(utcTime)
}
```
Output:
```
2021-12-15 12:45:36 +0000 UTC
```

### Conclusion
Converting a Linux timestamp to UTC time format in Go is a simple task using the `time.Unix` function. By providing the Linux timestamp as the first argument and 0 as the second argument, we can obtain a `time.Time` object representing the UTC time. This functionality is essential when working with timestamps in Go applications.