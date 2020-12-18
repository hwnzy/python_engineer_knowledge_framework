# 脏读/幻读/不可重复读

\*\*\*\*

\*\*\*\*

**脏读:**举个例子,如果你正在读数据库内容,而我现在修改了数据库内容还没有提交,接着我修改后的内容没有提交的情况下被你读到了,就叫脏读.

**不可重复读:**举个例子,比如你正在读数据库内容,而我update数据库后提交了,你又读了一次数据库内容,这时出现两个内容不同的结果,这叫不可重复读.

**幻读**:举个例子,比如你正在读数据库内容,而我insert数据库后提交了,你又读了一次数据库内容,这时你看到内容出现了多一条数据,这叫幻读.  


**脏读：** 就是A向B 转账100块，A只填写的转账的信息，并截图发给B， 但是没有点确认转账。

 B 看到A 发过来的填写转账信息，说好的，但是此时查询账户的时候，还是原来的余 额，并没有收到A 的转账，因为A 只是填了转账信息，并没有递交或者是确认转账。

**不可重复读：** 就是 A 向B 转账100块，并点了确认转账，这个信息是提交了的，那么B 在A 通知之前和之后，执行查询自己账户的这个操作是，前后的账户余额是不一样的，第一次是原来的月，第二次是原来的余额+A转账100

**脏读和不可重复读的区别是：**A 到底有没有提交信息

**脏读和不可重复读的相同点：** 都知道收到A 要转账给B 的意图

**幻想读：**是对整个数据集进行统一的修改，例如A把所有的汽车名称从宝马改成了吉利，但是B递交了一条新数据，汽车的名称还是宝马，此时A 看到这个不同的数据时，就像是产生幻想一样，刚才我明明把所有的名称改成了吉利，为什么又出现了一个宝马，发生了什么？

**不可重复读和幻想读的区别是**，不可重复读多次读的一个数据项，比如说多次只查询银行余额这个项（针对同一行数据的修改和删除用 update 和 delete），而幻想读是针对整个数据整体，比如银行员工查询今天交易的总人数，之前查的是100个人进行交易，进行第二次查询的时候，发现有105个人进行交易（主要是用insert 操作）。

**不可重复读和幻想读的相同之处是:** 多次查询期间，另一个人都递交了新的数据，导致前后读取的数据不一样
