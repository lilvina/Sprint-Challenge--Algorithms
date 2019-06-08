Add your answers to the Algorithms exercises here.

1. ```
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```

O(n) - The loop will continue to run no matter how much input N takes. If it didn't take any 
input, it would be 0(1), constant time.

2. ```
b)  sum = 0
    for i in range(n):
      i += 1
      for j in range(i + 1, n):
        j += 1
        for k in range(j + 1, n):
          k += 1
          for l in range(k + 1, 10 + k):
            l += 1
            sum += 1
```

This is tricky. Don't know how to answer this one but the outer loop, "i" increments twice because the loop finishes in half the time of n. As each iteration goes, it will iterate to j, which will do the same thing as i and same thing with k. As for l, it goes up by 1 but we also take in the sum and that's incremented by 1. Looking at this, I will the code could possibly explode if it is ran in the terminal or will run a long time because of how much we are looping and how much data we are taking. My guess would have to be O(n^3).

3. ```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0
      return 2 + bunnyEars(bunnies-1)
```
Okay, if bunnies were equal to zero, our code would be done but if the bunnies is whatever input you give it, the next line would be executed. With our if-statement, it's being done recursively and is checking to see if we have no bunnies. If you give the next line any number for the bunnies, 
it will return the number of bunnies. Our answer would be O(n) because even though this is recursive, the code will continue to run as long as it has input to run.

```
Suppose that you have an _n_-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get broken if dropped off a floor less than floor _f_. Devise a strategy to determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.
```
Create a while loop and then inside the loop, create a for loop, for i in range(n - 1), i represents the floor and if i is greater than or equal to break_floor, print a statement saying, "Eggs will break from this height". If i is less than break_floor, print "It is okay to drop eggs from this height". This could be done n times with each loop, so it would be linear, O(n).