Notiz
==========

**1.** 继承于Thread类  
    start()运行的是多线程，run()运行的是单线程  
**2.** 优先级区间是1-10  
**3.** yield()相当于变道交警，让其他线程先跑。实现了“你一个，我一个”  
**4.** 加入了一个Random变量以及一个for循环，实现了和yield()一样的效果，机制不同，执行时间过久导致了线程的切换。  
**5.** nextInt(10)的取值范围是0-9，同时写入产生脏数据  
**6.** A.join()是A去加入了其他，先执行A  
**7.** sleep(t,单位是毫秒)，如果只想要一个sleep，加入if(Haupt.p==this)代码，则只有当P运行的时候会sleep  
**8.** InterruptedException 打断睡眠,通过interrupt()  
**9.1.** 在方法中加入synchronized，避免了5中产生的脏数据  
**9.2.** 在Haupt中创建一个Object如s，在Prozess中的run()中插入synchronized(s)，实现另一种方式的锁  
**10.** 生产者消费者模型，锁需要在一个类中，在生产者类中是synchronized erzeuge()和synchronized nimm()方法
**11.** notify()不放锁，是运行完erzeuge()后自然放锁。wait()会暂时放锁;wait()和sleep()都可以抛出Exception;wait()会放锁，sleep()不放锁  
**12.** 用notifyAll()去唤醒所有，让大家来抢一个锁
**16.** 谁调用锁谁，Thread.currentThread()来调用当前的线程  
**18.** Reentrantlock公平锁，在原有方法的基础上用了Concurret类的方法，如await()等。先进先出，后进后出。
