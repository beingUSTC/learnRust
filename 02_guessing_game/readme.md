猜数游戏

我们将完成一个经典的初学者编程挑战：猜数游戏，
它会首先生成一个1到100之间的随机整数，并紧接
着请求玩家对这个数字进行猜测。
假如玩家输入的数字与随机数不同，那么程序将给出
数字偏大或偏小的提示。而假如玩家猜中了我们准备的数字，
那么程序就会打印出一段祝贺信息并随之退出。

在Rust中，变量都是默认不可改变的，使用mut来申明一个变量是可变的
let foo = 5;//foo是不可变的
let mut bar = 5; // bar是可变的

使用Result类型来处理可能失败的情况 result是一个枚举类型
  read_line会将用户输入的内容存储到我们传入的字符串中，
它还会返回一个io::Result值。对于Result而言，它拥有Ok和Err两个变体。
其中的Ok变体表明当前的操作执行成功，并附带代码产生的结果值。相应地，Err变体则表明当前的操作执行失败，并附带引发失败的具体原因。

使用rand生成随机数字
Rust中的包（crate）代表了一系列源代码文件的集合。我们s当前正在构建的项目是一个用于生成可执行程序的二进制包 （binary crate），
而我们引用的rand包则是一个用于复用功能的库包 （library crate，代码包）。

关于包的版本问题
Cargo会一直使用某个特定版本的依赖直到你手动指定了其他版本，通过Cargo.lock 实现
如果要忽略lock强制升级包则使用 cargo update。

Rust允许使用同名的新变量guess来隐藏 （shadow）旧变量的值。比如程序中的两个guess

加入循环实现多次猜测
loop关键字实现循环