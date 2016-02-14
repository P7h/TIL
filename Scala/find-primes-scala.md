## Finding prime numbers in Scala

```scala
//Scala method to find if a number is prime or not.
def isPrime(number: Int): Boolean = {
    if (number == 1) {
        return false;
    }
    if (number % 2 == 0 && number != 2 || number % 3 == 0 && number != 3) {
        return false;
    }
    val limit = ((Math.pow(number, 0.5) + 1) / 6.0 + 1).toInt;
    (1 until limit).foreach(i => {
        if(number % (6 * i - 1) == 0) {
            return false;
        }
        if(number % (6 * i + 1) == 0){
            return false;
        }
    })
    true
}
```

### Scala code to find primes in a given range
#### Normal execution
```scala
(1 to 100).foreach(i => println(Thread.currentThread.getName + ":" + i + "=>" + isPrime(i)))
```

#### Parallel execution
```scala
(1 to 100).par.foreach(i => println(Thread.currentThread.getName + ":" + i + "=>" + isPrime(i)))
```