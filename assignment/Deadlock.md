### lab4 Deadlock
数据科学与计算机学院 14353174 林庚岳

-----------------
1. 实验结果
 * Deadlock.java代码  
 ![](https://github.com/14353174Lingengyue/ES2016_14353174/blob/lab_picture/lab4_java.png?raw=true)
 * Deadlock.bat代码  
 ![](https://github.com/14353174Lingengyue/ES2016_14353174/blob/lab_picture/lab4_bat.png?raw=true)
 * 实验运行结果，在19次处发生死锁  
 ![](https://github.com/14353174Lingengyue/ES2016_14353174/blob/lab_picture/lab4_19time.png?raw=true)
2. 死锁产生的四个条件
 * 互斥条件，每个资源每次只能被一个线程调用
 * 请求与保持条件，一个进程因请求资源而阻塞时，不释放已获得的资源
 * 不剥夺条件，进程已获得的资源在未使用完之前，不能强行剥夺
 * 循环等待条件：若干线程之间形成一种头尾相接的循环等待资源的关系
3. 实验中死锁产生原因
 * 实验中Runable会在后台不断重复执行，这样就会重复依次产生线程t，线程t需要两个资源a.methodA(b)和b.methodB(a)，a.method(b)需要调用b.last()方法，b.method(a)需要调用a.last()方法，而这四个方法都是都被定义为synchronized，因此a.methodA()与a.last()，和b.methodB()与b.last()是不能被同时调用的。当a.methodA(b)和b.methodB(a)同时执行时，a.methodA(b)会因为不能继续调用b.last()而被阻塞，而b.methodB(a)也因为不能继续调用a.last()而被阻塞，这样程序就发生死锁了