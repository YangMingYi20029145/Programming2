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
