# enchanting_scala_0

###Hello Scala!


+ 如果让我用两个字来形容scala，我会用“妖娆”。
+ 让我们从零开始领略她的“妖娆”。
+ 博主也是从零开始学习scala，也是第一次写博客。
+ 整个系列肯定会存在很多错误，请大家指出。
+ 在后续的学习过程中发现之前的文章有错误会立即更正。
+ Hello Scala!

_____

以下是我的环境

+ OS X Yosemite 10.10.2
+ java version "1.8.0_45"
+ scala version 2.11.6
+ Intellij IDEA Community Edition 14.1.2
+ Scala plugin 1.5

省略环境的安装过程，来个``Hello World!``吧，oh，是``Hello Scala!``

```scala
package org.scala.study.grammer.hello

/**
 * Created by coder on 15/5/23.
 */
object Hello {

  def main(args: Array[String]) {
    println("Hello Scala!")
  }

}
```

虽然是个短短的``Hello Scala!``，但也包含了很多东西。下面我们一分析下，着重与  **java** 对比。

####package
+ 与java不同，包名与文件夹不存在完全的对应关系。
+ 下面写法也支持

```scala
package org.scala.study.grammer.hello {
  object Hello {
    def main(args: Array[String]) {
      	println("Hello Scala!")
    }
  }
}
```
