```GO
package main
import (
	"fmt"
	"time"
)
func main(){
	
	fmt.Println("the time is",time.Now())
}
```
```go
package main
import (
	"fmt"
	"math/rand"
)
func main(){
	fmt.Println("my favorite number is",rand.Intn(10))
}
```
```go
package main

import (
	"fmt"
	"math"
)

func main() {
	fmt.Printf("Now you have %g problems.\n", math.Sqrt(9))
}
```
```go
package main

import "fmt"

func add(x int, y int) int {
	return x + y
}
// (x int ,y int)可以简写为（x,y int）
func main() {
	fmt.Println(add(42, 13))
}
```
``` go
package main

import "fmt"

func swap(x, y string) (string, string) {
	return y, x
}

func main() {
	a, b := swap("hello", "world")
	fmt.Println(a, b)
}
```
```go
s1:="hello"
	s2:="world"
	fmt.Println(s1+s2)
	s3:=fmt.Sprintf("%s-%s",s1,s2)
    fmt.Println(s3)
```

###<font color="red">[运算符](https://www.liwenzhou.com/posts/Go/03_operators/)</font>
```go
    1.算术运算符
	a:=10
	b:=10
	fmt.println(a+b)
	fmt.Println(a-b)
	fmt.Println(a*b)
	fmt.Println(5/2)
	fmt.Println(5%2)
	a++
	fmt.println(a)
	b--
	fmt.println(b)
```
```go
	2.关系运算符
	c:=10>2
	var c bool =10>2
	fmt.prntln(10>2)
```
```go
	3.逻辑运算符
	fmt.Println(10 >5 && 1==1)
	fmt.Println(! (10>5))
	fmt.Println(1>5||1==1)
```
```go
	4.位运算符
	a:=1  //001
	b:=5  //101
	fmt.Println(a&b)//1
	fmt.Println(a|b)//5
	fmt.Println(a^b)//4
	fmt.Println(a<<2)//4
	fmt.Println(a<<b)//32
	fmt.Println(a>>2)//0  不会到小数了
```
```go	
	5.赋值运算符
	a:=5
	a+=5//a=a+5   
	var b int
	b=a//b=5
	a*=5//a=25
	a%=2//a=1
	a<<=2//a=20
	a&=1//a=1
```
