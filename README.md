# randhex

A library for generating random hexidecimal color codes

## License

[MIT](LICENSE)

## Installation

```
$ go get github.com/frankenbeanies/randhex
```

## Usage

```go
import "github.com/frankenbeanies/randhex
```

## Methods

### New()

Generates a new random hexidecimal color code (RandHex)

```go
hex := randhex.New()
```

### String()

Provides a string representation of the RandHex prepended with '#'

```go
hexStr := randhex.New().String()
```

### Bytes()

Provides the byte representation of the RandHex

```go
hexBytes := randHex.New().Bytes()
```

### ParseString()
Parses string into a RandHex

```go
hex, _ := randhex.ParseString("#aaa")
hex, _ := randhex.ParseString("#AAAAAA")
hex, _ := randhex.ParseString("aaa")
_, err := randhex.ParseString("a") //error, bad length
_, err := randhex.ParseString("%aaa") //error, bad symbol
_, err := randhex.ParseString("#gaa") //error, not hex
```