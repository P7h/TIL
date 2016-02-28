## Factorial of a number in Scala

```scala
//Normal recursion paradigm.
object FactorialRec {
    def main(args: Array[String]): Unit = {
      val n = 10
      def factorialImpl(n: Int): Int = {
        if (n <= 1) 1
        else n * factorialImpl(n - 1)
      }
    println(factorialImpl(n))
  }
}
```

```scala
//With tail recursion.
import scala.annotation.tailrec

object FactorialTailRec {
    def main(args: Array[String]): Unit = {
      val n = 10
      @tailrec def factorialImpl(accumulo: Int, n: Int): Int = {
        if (n <= 1) accumulo
        else factorialImpl(n * accumulo, n - 1)
      }
    println(factorialImpl(1, n))
  }
}
```
