###<font color="red">[循环语句](https://www.liwenzhou.com/posts/Go/04_basic/)</font>
```go
	//if 判断
	1.var score =65
	if score >=90{
		fmt.Println("excellent")	
	}else if score >=70 {
		fmt.Println("good")
	}else {
		fmt.Println("terrible")
```
```go
	2.if score:=65; score >=90{
		fmt.Println("excellent")	
	}else if score >=70 {
		fmt.Println("good")
	}else {
		fmt.Println("terrible")
	}//score 这个变量只在一个代码块里生效
	//判断可以只要if语句
```
```go
	//for 循环
	1.for i:=0;i<10;i++{
		fmt.Println(i)
	}	
	//省略初始语句，但是必须保留初始语句后面的分号
	2.var i int=0
	for ;i<10;i++{
	fmt.Println(i)
	}
	//省略初始语句和结束语句
	3.var i =0
	for i<10{
		fmt.Println(i)
		i++
	}
	//无限循环
	for{
		fmt.Println("hello")
	}
	//break跳出循环
	for i:=0;i<5;i++{
		fmt.Println(i)
		if i==3{
			break
		}
	}
	 //continue继续下一次循环
	for i:=0;i<5;i++{
		if i==3{
			continue//跳过本次for循环，继续下一次循环
		}
		fmt.Println(i)
    }	
``` 
```go
	// switch	
	finger :=3
	switch finger{
	case 1:
		fmt.Println("大拇指")
	case 2:
		fmt.Println("食指")
	case 3:
		fmt.Println("中指")
	case 4:
		fmt.Println("无名指")
	case 5:
		fmt.Println("小拇指")
	default:
		fmt.Println("无效的输入！")
    }
```
```go
//case 一次判断多个值
num :=3
switch num{  //可以写为switch num:=3;num{ }
case 1,3,5,7,9: 
	fmt.Println("奇数")
case 2,4,6,8,10:
	fmt.Println("偶数")
}
```
```go
//分支还可以使用表达式，这时switch语句后面不需要再跟判断变量，跟了就错了 
age := 30
	switch {
	case age < 25:
		fmt.Println("好好学习吧")
	case age > 25 && age < 35:
		fmt.Println("好好工作吧")
	case age > 60:
		fmt.Println("好好享受吧")
	default:
		fmt.Println("活着真好")
	}
```
###<font color="red">[数组](https://www.liwenzhou.com/posts/Go/05_array/)</font>
```go
 	var a [3]int//默认为初始值 数组为0值
	var b=[4]int{1,2}
	var cityarray = [4]string{"北京","上海", "深圳"}
	var boolarray =[...]bool{false,true,true}
	fmt.Println(a,b,cityarray,boolarray)
	fmt.Printf("%T\n",boolarray)//自动推导类型
	fmt.Println(boolarray[1])
	//指定索引值的方式初始化数组
	c:=[...]int{1:1,3:5}
	fmt.Println(c)
	fmt.Printf("type of c:%T\n",c)
```
```go
	 //数组的遍历
	  var a = [...]string{"北京", "上海", "深圳"}
	 for i := 0; i < len(a); i++ {
		 fmt.Println(a[i])
     }  
```
```go
	 var a = [...]string{"北京", "上海", "深圳"}
	for index:= range a {
        fmt.Println(index) 
```
```go
	 var a = [...]string{"北京", "上海", "深圳"}
 	for _.value:=range a{
		fmt.Println(value)
    }  
```
```go
	//多维数组  多多维数组不能让编译器推导元素个数
	a:=[3][2]string{
		{"北京", "上海"},
		{"广州", "深圳"},
		{"成都", "重庆"},
	}
	for _, v1 := range a {
		for _, v2 := range v1 {
			fmt.Printf("%s\t", v2)
		}
		fmt.Println()
    }
```
###<font color="red">[切片](https://www.liwenzhou.com/posts/Go/05_array/)</font>
