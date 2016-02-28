## Factorial of a number in Scala

```scala
//Normal recursion paradigm.
```

```scala
//With tail recursion.
import scala.annotation.tailrec

object Factorial extends App {
    override def main(args: Array[String]): Unit = {
      val n = 10
      @tailrec def factorialImpl(accumulo: Int, n: Int): Int = {
        if (n <= 1) accumulo
        else factorialImpl(n * accumulo, n - 1)
      }
    println(factorialImpl(1, n))
  }
}
```
