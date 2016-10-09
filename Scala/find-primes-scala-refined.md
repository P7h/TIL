## Finding prime numbers in Scala [refined version]

```scala
// Scala method to find if a number is prime or not.
// https://en.wikipedia.org/wiki/Twin_prime
def isPrime(number: Int): Boolean = {
    number match {
        case 1 => false
        case twoOrThree if (twoOrThree == 2 || twoOrThree == 3) => true
        case twoOrThreeMultiplier if (twoOrThreeMultiplier % 2 == 0 || twoOrThreeMultiplier % 3 == 0) => false
        case sixTest if((sixTest + 1) % 6 == 0 || (sixTest - 1) % 6 == 0) => {
            val limit = ((Math.pow(sixTest, 0.5) + 1) / 6.0 + 1).toInt
            (3 until limit by 2).filter(i => (sixTest % i == 0)).size == 0
        }
        case _ => false
    }
}
```


```scala
// Scala method to find if a number is prime or not.
// https://en.wikipedia.org/wiki/Primality_test
def naivePrimalityTest(n: Int): Boolean = {
  def primeEvalRecursion(i: Int, n2: Int): Boolean = {
      n2 match {
        case iSquared if (i*i > n2) => true
        case nModi if (n2 % i == 0 || n2 % (i + 2) == 0) => false
        case _ => primeEvalRecursion((i + 6), n2)
      }
  }
  n match {
    case lessThanOrEqualTo1 if (n <= 1) => false
    case lessThanOrEqualTo3 if (n <= 3) => true
    case multipleOf2Or3 if (n % 2 == 0 || n % 3 == 0) => false
    case _ => primeEvalRecursion(5, n)
  }
}
```

### Scala code to find primes in a given range
#### Normal execution
```scala
(1 to 100).map(i => ((i, isPrime(i)))).filter(_._2 == true).foreach(i => print(i._1 + "\t"))
(1 to 100).map(i => ((i, naivePrimalityTest(i)))).filter(_._2 == true).foreach(i => print(i._1 + "\t"))
```

#### Parallel execution
```scala
(1 to 100).par.map(i => ((Thread.currentThread.getName, i, isPrime(i)))).toList.filter(_._3 == true).sortBy(_._2).foreach(i => println(i._1 + "\t" + i._2))
```