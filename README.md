### DOL框架
DOL即Distributed Operaton Layer，是一个用于解决现代嵌入式系统在多个应用同时运行时产生的复杂的交流问题的框架。DOL可以提供多处理器平台上的平行应用的执行效率，并且能够提供高效的性能分析和多目标映射的优化。

----------

### 安装流程
1. 首先在Ubuntu系统上安装一下必要的环境
   ![](http://i.imgur.com/UTe3x6K.png)
2. 将dolethz.zip文件解压到新建的文件夹dol中，并使用命令$	tar -zxvf systemc-2.3.1.tgz解压systemc
3. 在解压出来的system-2.3.1文件夹下新建一个objdir文件夹，进入该objdir文件夹后运行configure，最后再编译。使用命令依次如下：
   * $	cd systemc-2.3.1
   * $	mkdir objdir
   * $	cd objdir
   * $	../configure CXX=g++ --disable-async-updates
   * $	sudo make install
4. 在dol文件夹下找到并修改build_zip.xml文件
   ![](http://i.imgur.com/HXQYAVq.png)
5. 使用命令$	ant -f build_zip.xml all编译dol，然后进入build/bin/main路径下运行第一个例子$	ant -f runexample.xml -Dnumber=1。以下为运行第一个例子的结果：
   ![](http://i.imgur.com/1nIKHB5.png)


