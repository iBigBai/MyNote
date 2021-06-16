## 面向对象
### 匿名对象
* `匿名对象:`没有名字的对象，仅调用一次
``` java
//new 对象名.方法名
new Car().run();
```
### 关键字static
`static:`
>1. 随着类的加载而加载
>2. 优先于对象的存在（随着字节码文件加载时还没有对象）
>3. 被类的所有对象共享（共性用静态，特性用非静态）
>4. 可以通过类名调用

`注意事项:`
* 静态方法中没有`this`关键字
* 静态只能访问静态
### 关键字this&spuer
`this:`	代表所在方法所属对象的引用（哪个对象调用了this所在的函数，this就代表这个对象）
``` java
public static void main(String[] args) {
    Phone p1 = new Phone();
    p1.setBrand("三星");
    p1.setPrice(5288);
    System.out.println(p1.getBrand() + "..." + p1.getPrice());
}
class Phone {								//java bean
	private String brand;					//品牌
	private int price;						//价格
			
	public void setBrand(String brand) {	//设置品牌
		this.brand = brand;
	}
			
	public String getBrand() {				//获取品牌
		return this.brand;					//this.可以省略,你不加系统会默认给你加
	}
			
	public void setPrice(int price) {		//设置价格
		this.price = price;
	}
			
	public int getPrice() {					//获取价格
	    return price;
	}
}
```
### 构造方法 Constructor
* 构造方法定义
> 1. 方法名与类名相同（大小写也要与类名一致）
> 2. 没有返回值类型，连void也没有；
> 3. 没有具体的返回值return；
```java
class Person {
	private String name;
	private int age;
	//构造方法
	public Person() {
		name = "张三";
		age = 23;
        //return;//构造方法也是有return语句的,格式是return;
	}
	public void show() {
		System.out.println(name + "..." + age);
	}
}
```
###### 构造方法重载
**注意：没有写构造方法，系统自动提供构造方法；写了构造方法，系统不再提供构造方法**
**建议：永远自己写无参构造犯法**
## 继承
