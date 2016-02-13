## Finding prime numbers in Scala [refined version]

```
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

### Scala code to find primes in a given range
#### Normal execution
```
(1 to 100).map(i => ((i, isPrime(i)))).filter(_._2 == true).foreach(i => println(i._1))
```

#### Parallel execution
```
(1 to 100).par.map(i => ((Thread.currentThread.getName, i, isPrime(i)))).toList.filter(_._3 == true).sortBy(_._2).foreach(i => println(i._1 + "\t" + i._2))
```