ENAS



ENAS通过共享参数来减少模型搜索的计算量



搜索空间的容量：

RNN包含N个节点，4个激活函数（tanh, ReLU,identity, sigmoid），最终一共可以生成4N × N! 种网络结构。每一个节点有4种激活方式，N个节点相互独立，生成4N种激活方式，第一个节点只能和输入进行连接，第二个节点可以和输入和第一个节点2个里面选一个连接，第三个节点可以和输入和第1,2共3个节点里面选一个连接，依次类推，最终产生N!种连接方式。所以最终生成4N × N!种有向图DAG。
————————————————
版权声明：本文为CSDN博主「watersink」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/qq_14845119/article/details/84070640



cnn网络：

每个节点相互对立，每一个节点都有6种操作可能，L个节点就会有6L种操作可能。

有L个节点的有向图一共有L(L-1)/2条连接线，每个连接线有连接，不连接，2种可能，整个图就会产生2 L(L-1)/2种连接结构。最终就会产生6L × 2 L(L-1)/2种网络结构。



