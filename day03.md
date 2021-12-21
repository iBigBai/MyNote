## 键盘录入
``` java
import java.util.Scanner;  
public class Main {  
    public static void main(String[] args) {  
        Scanner scanner = new Scanner(System.in);
        String s = scanner.next();  
        System.out.println(s);  
    }  
}
```
## 三元运算符
``` java
int max = (x > y) ? x : y
```
``` java
public class Main {  
    public static void main(String[] args) {  
        int x = 10;  
        int y = 2;  
        System.out.println((x > y) ? x : y);  
        int z = (x > y) ? x : y;  
        System.out.println(z);  
    }  
}
```
## if 语句
``` java
public class Main {  
    public static void main(String[] args) {  
        int num = 11;  
        if (num % 2 == 0) {  
            System.out.println(num + "是一个偶数");  
        }else {  
            System.out.println(num + "是一个奇数");  
        }  
    }  
}
```
## switch 语句
``` java
switch(表达式) {
      case 值1：
            语句体1;
      break;
      case 值2：
            语句体2;
      break;
       …
      default：
            语句体n+1;
      break;
}
```