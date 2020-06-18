###<font color="red">[函数](https://www.liwenzhou.com/posts/Go/09_function/)</font>
```go
//function 
//定义一个不需要参数也没有返回值的函数：sayhello
func sayhello(){
	fmt.Println("lalala")
}
func main(){
}
```
```go
//定义一个有参数没有返回值的函数
func sayhello2(name string){
	fmt.Println("hello",name)
}
func main(){
	n:="沙河娜扎"
	sayhello2(n)
}
```
```go
func intsum(a int,b int) int{
	ret:=a+b
	return ret
func main(){ //函数有返回值可以不接收返回值
        intsum(10,20) 
```
```go
1.func intsum(a int,b int) int{
	ret:=a+b
	return ret
2.func insum2(a int,b int) (ret int){
	ret =a+b
	return
	}
} 
```
```go
//可变参数  
func intSum2(x ...int) int {
	fmt.Println(x) //x是一个切片
	sum := 0
	for _, v := range x {
		sum = sum + v
	}
	return sum
}
func main(){
	ret1 := intSum2()
	ret2 := intSum2(10)
	ret3 := intSum2(10, 20)
	ret4 := intSum2(10, 20, 30)
	fmt.Println(ret1,ret2,ret3,ret4)
}
```
```go
 //固定参数和可变参数同时出现时，可变参数放在最后
func intSum2(x int,y...int) int {
	sum := x
	for _, v := range y {
		sum = sum + y
	}
	return sum
}
func main(){
	ret1 := intSum2(0)                 
	ret2 := intSum2(10)                //a=10,b=[]
	ret3 := intSum2(10, 20)            //a=10,b=[20]
	ret4 := intSum2(10, 20, 30)        //a=10,b=[20,30]
	fmt.Println(ret1,ret2,ret3,ret4)    
}  
```
```go
//定义具有多个返回值的函数
func calc(a,b int)(sub,sum int){
	sub=a+b
	sum=a-b
	return 
}
func main(){
	x,y:=calc(100,200)
	fmt.Println(x,y)
} 
```
```go
//defer 延迟执行
func main() {
	fmt.Println("start")
	defer fmt.Println(1)
	defer fmt.Println(2)
	defer fmt.Println(3)
	fmt.Println("end")
} 
```
```go
//可以在函数中使用变量
//1.先在自己函数中查找，找到了就用自己函数中的
//2.函数中找不到变量就往外层找全局变量
//3.外层不能访问到内层函数的内部变量
//4.想要在外部使用内层的变量，需用用return返回，通过一个变量接受返回值的形式实现
func testglobal(){
	fmt.Println("num")
}
func main(){
	abc:=  testglobal 
	fmt.Printf("%T\n",abc)
}
```
```go
//函数作为参数
func add(x,y int) int {
	return x+y
}
func calc(x,y int, op func(int,int) int) int{
	return op(x,y)
}
func main(){
	r1:=calc(100,200,add)
	fmt.Println(r1)
} 
```
```go
