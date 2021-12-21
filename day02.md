## 常量
1. 字面值常量
> * 字符常量：使用单引号''的内容 
> * 字符串常量：使用双引号""的内容
> * 整数常量：所有整数
> * 小数常量：所有小数
> * 布尔常量：`true`&`false`
> * 空常量：`null`
``` java
public class Main {  
    public static void main(String[] args) {  
        System.out.println("zbc");  //字符串常量  
 		System.out.println(123);    //常数常量  
 		System.out.println(12.3);   //小数常量  
 		//System.out.println('10');   //Error：''中必须放单个字符 
 		//System.out.println('');     //Error：''中不能什么都不放 
 		System.out.println(' ');    //带空格字符  
 		System.out.println(true);   //boolean 中只有两个值true&false  
 		System.out.println(false);  
    }  
}
```
2. 自定义常量
>* 接口常量
>* 枚举
>* `final static`
>* 定义方法获得
## 原码反码补码（原反补）
1.  原码
2. 反码
* 正数：反码与原码相同
* 负数：除符号位外，原码逐位取反
3. 补码「参与运算」
* 正数：补码与原码相同 
* 负数：在反码的末尾+1
``` java
public class Main {  
    public static void main(String[] args) {  
        System.out.println(0b100);  //0b 表示二进制   4  
 		System.out.println(0100);   //0  表示八进制   64  
 		System.out.println(100);    //默认十进制      100  
		System.out.println(0x100);  //0x 表示十六进制 256  
 	}  
}
```
## 基本数据类型「4类8种」
> 1. 整数型
>* `byte` 一字节8位「-128～127」
>* `short`二字节16位「-32768～32767」
>* `int`四字节32位「-2147483648～2147483647」二十一亿
>* `long`八字节64位「-2^63~2^63-1」
> 2. 浮点型
> * `float`四字节32位「-3.403E38~3.403E38」
> * `double`八字节64位「-1.798E308~1.798E308」
> 3. 字符型
>* `char`两个字节16位「0～65535」
> 4. 布尔型
> * `boolean`「理论上八分之一个字节」
``` java
public class Main {  
    public static void main(String[] args) {  
        //整数类型  
 		byte b = 10;  
        short s = 20;  
        int i = 30;  
        long l = 88888888;  //整数默认数据类型int,可以直接转换为long  
 		long l2 = 88888888L;//过大的整数会超过int取值范围，必须加L声明数据类型  
 		System.out.println(b);//10  
 		System.out.println(s);//20  
 		System.out.println(i);//30  
 		System.out.println(l);//88888888  
 		//浮点类型 
		float f = 12.3F; //小数默认数据类型double,无法转换为float必须强制添加F标识  
 		double d = 12.34;  
        System.out.println(f);//12.3  
 		System.out.println(d);//12.34  
 		//字符类型 
		char c = 'a';  
        char c1 = 97;  
        //char c2 = '97' //Error:char必须放单个字符  
 		System.out.println(c);	//a  
 		System.out.println(c1);	//a  
 	}  
}
```
## 运算符
> `/`除法：整数运算只能是整数。
> `%`取模「取余」符号与被模数相同
> * 被模数绝对值<模数绝对值,结果是被除数
> * 被模数绝对值 = 模数或是倍数,结果是0
> * 被模数绝对值>模数绝对值,结果是余数
``` java
public class Main {  
    public static void main(String[] args) {  
        byte b = 3 + 4;  
		//编译器常量优化机制，在编译过程中就将结果计算出来了
        byte b1 = 3;  
        byte b2 = 4;  
        //byte b3 = b1 + b2;  
 		//Error:byte与byte(short,char)运算会提升为int 
		//b1,b2是两个变量，变量存储的值是变化的，编译过程中无法判断具体的值，运算可能会超出取值范围 
	}  
}
```