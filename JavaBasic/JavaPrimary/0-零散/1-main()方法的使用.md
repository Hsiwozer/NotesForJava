# main()方法的使用

1. #### main()方法作为<font color="red">程序的入口</font>

   ```java
   public class MainTest {
       public static void main(String[] args) {
       }
   }
   ```

2. #### main()方法也是一个<font color="red">普通的静态方法</font>

   ```java
   public class MainTest {
       public static void main(String[] args) {
           Main.main(new String[100]);
           show();
       }
   
       public static void show() {}
   }
   
   class Main {
       public static void main(String[] args) {
           for (int i = 0; i < args.length; i++) {
               args[i] = "args_" + i;
               System.out.println(args[i]);
           }
       }
   }
   ```

3. #### main()方法可以作为<font color="red">与控制台交互的方式</font>

   ```java
   public class MainDemo {
       public static void main(String[] args) {
           for (int i = 0; i < args.length; i++) {
               System.out.println("***" + args[i]);
           }
       }
   }
   ```