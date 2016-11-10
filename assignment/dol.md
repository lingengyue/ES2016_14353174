### lab3 DOL实例分析
数据科学与计算机学院 14353174 林庚岳

----------

1. 修改example2，让3个square模块变成2个
   * 我们找到dol/examples/example2文件夹中的example2.xml文件，将N（即迭代次数）由3改为2，这样square模块只会迭代两次
   ![](https://github.com/14353174Lingengyue/ES2016_14353174/blob/master/x2.png?raw=true)
   * 使用指令sudo -f runexample.xml -Dnumber=2编译运行example2结果如下图所示:
   ![](https://github.com/14353174Lingengyue/ES2016_14353174/blob/master/e2.png?raw=true)
2. 修改example1，使其输出3次方数
   * 我们找到dol/examples/example1/src文件夹下的square.c函数，将i = i * i改为i = i * i * i，这样输出就从2次方变成3次方
   ![](https://github.com/14353174Lingengyue/ES2016_14353174/blob/master/x1.png?raw=true)
   * 重新编译运行example1，结果如下图所示
   ![](https://github.com/14353174Lingengyue/ES2016_14353174/blob/master/e1.png?raw=true)

----------
### 实验感想
本次实验初次对dol中的example进行分析和修改，一开始无从下手，不知道该怎么看，但经过TA的仔细讲解，对example框架有了一个初步认识，加上本次实验不是很难，所以没什么问题


