### 傳值呼叫 call by value
```
方法中的虛引數若宣告為基本資料型別，如 chat、byte、short、int、long、float、double、boolean 八種型別邊數，就表示該方法的引數傳遞方式是採傳值呼叫。 
```
```
public class CallByVal{
  public static void main(String[] args){
    int a = 10, b=15;
      system.out.println("傳值呼叫前\t a =" + a + "\t b =" + b);
      byVal(a,b);
      system.out.println("傳值呼叫後\t a =" + a + "\t b =" + b);
    }
  static void byVal(int x, int y){
    int t;
    t = x;
    x = y;
    y = t;
   system.out.println("傳值呼叫中\t x =" + x + "\t y =" + y);
   }
 }
 ```
 
 ### call by reference
 ```
 方法中的虛引數若宣告為參考資料型別，如陣列、物件...等，表示此方法的引數傳遞方式是採參考呼叫。 
 ```
 ```
 class Obj{
    int a, b;
   Obj(){
    a = 10;
    b = 15;
  }
}
public class CallByRef{
  public static void main(String[] args){
    Obj obj = new Obj;
      system.out.println("參考呼叫前\t a =" + obj.a + "\t b =" + obj.b);
    byRef(obj);
      system.out.println("參考呼叫後\t a =" + obj.a + "\t b =" + obj.b);
   }
   static void byRef(Obj p){
      int t;
      t = p.a;
      p.a = p.b;
      p.b = t;
    }
  }
 ```
### 方法多載
```
同一類別中，允許方法使用相同的名稱，但是後面所接的引數串列必須是資料型別不同、個數或順序不同。
```
```
01 void methed(){}
02 int methed(){}    //不能多載:雖然傳回值不同但引數個數相同
03 void methed(int a){}    //成功多載:比第1行的方法多一個引數
04 void methed(int b){}    //不能多載:引數名稱不同,但和第3行型別和個數相同
05 void methed(string s){} //成功多載:雖然和第3行引數個數相同但型別不同
06 void methed(int a, string s){}    //成功多載:引數個數和型別都不相同
07 void methed(string s, int a){}    //成功多載:和第6行引數個數和型別相同但順序不同
```
### 費氏數列:遞迴方法 vs iterative ==> 再算　時間複雜度
```
費氏數列值第1及第2 項皆為1，
第3項之後的公式為f(n)= f(n-1) + f(n-2)。

1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233

使用者輸入一個正整數X，計算出費氏數列的第X項並輸出。

計算費氏數列的第X項，請輸入X= 12  
==>  費氏數列的第12項= 144

(1)請使用靜態遞迴方法算出費氏數列。
(2)請使用 iterative方法算出費氏數列。
```
```
https://www.tutorialspoint.com/compile_java_online.php
```
### 遞迴方法

```
public class ex2{
    static int f(int n){
        if(n==0 || n==1) return n;
        else return f(n-1)+f(n-2);
    }
     public static void main(String []args){
        System.out.println(f(12));
     }
}
```
```
144
```

### iterative方法
```
https://magiclen.org/recursive-to-iterative/
https://emn178.pixnet.net/blog/post/91987861
```
```

```
### ???
```
import java.util.*;

public class Fibonacci {
    private List<Integer> fib = new ArrayList<>();
    {
        fib.add(0);
        fib.add(1);
    }
    
    Integer get(int n) {
        if(n >= fib.size()) for(int i = fib.size(); i <= n; i++) {
            fib.add(fib.get(i - 1) + fib.get(i - 2));
        }
        return fib.get(n);
    }
    
    public static void main(String[] args) {
        Fibonacci fibonacci = new Fibonacci();
        for(int i = 0; i < 20; i++) {
            System.out.print(fibonacci.get(i) + " ");
        }
    }
}
```
```
0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 610 987 1597 2584 4181
```
