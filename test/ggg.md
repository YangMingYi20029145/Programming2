### call by value
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
 class Obj{
    int a, b;
   Obj(){
    a = 10;
    b = 15;
  }
}
public class CallByRef{
  public static void main(String[] args){
    Obj obj = new Obj
      system.out.println("參考呼叫前\t a =" + obj.a + "\t b =" + obj.b);
    byRef(obj)
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
1.void methed(){}
2.int methed(){}    //不能多載:雖然傳回值不同但引數個數相同
3.void methed(int a){}    //成功載入:比第一行的方法多一個引數
4.void methed(int b){}    //不能載入:引數名稱不同,但和第3行型別和個數相同
5.void methed(string s){} //成功載入:雖然和第3行引數個數相同但型別不同
6.void methed(int a, string s){}    //成功載入:引數個數和型別都不相同
7.void methed(string s, int a){}    //成功載入:和第6行引數個數和型別相同但順序不同
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
