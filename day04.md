## for循环语句
``` java
for (int i = 0; i < 10; i++) {  
    System.out.println("hello world");  
}
```
## 增强for循环语句
``` java
```
## while语句
``` java
int i = 1;  
while (i < 10) {  
    System.out.println("hello world");  
    i++;  
}
```
## do{ } while语句
``` java
int i = 11;  
do {  
	//先执行再判断,至少执行一次
    System.out.println(i);  
    i++;  
} while (i < 10);
```
## 关键字break continue
* `break:`结束循环
* `continue:`结束本次循环，继续下次循环
* `return:`结束方法体
``` java
for (int i = 0; i < 4; i++) {  
    if (i == 2) {  
        break;  //结果：0，1  
 		continue; //结果：0，1，3  
 	}  
    System.out.println("i = " \+ i);  
}
```
## 方法重载
* 方法名相同，参数列表不同，与返回值类型无关
``` java
//1.参数个数不同  
//2.参数类型不同  
//3.参数顺序不同（开发中不用）  
public double add(int a, double d){  
    return a + d;  
}
public int add(int a, int d){  
    return a +d ;  
}
```