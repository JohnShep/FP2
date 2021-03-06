
## My Library: Math Library
My name: JT Shepple

## What I did:
I messed around with the Math Library and checked out how to use different functions with matrices. First I made two 3x3 matrixes and did basic math to them like added, subtracted and multiplied them. I also did a factor which could multiple or divide each element in the matrix. 


```racket
#lang racket

(require math)

;Makes a 3x3 matrix filled in with 5's
(define filledMatrix (make-matrix 3 3 5))

;Makes a custom matrix of 3x3
(define customMatrix (matrix [[1 2 3] [2 3 4] [3 4 5]]))

;Adds the two matixes together and prints to screen.
;This would add 5 to each element and is printed to the screen.
(matrix+ filledMatrix customMatrix)

;Subtracts the custom matrix from the filled in matrix so each element starts at 5 and subtracts
;the value in the cooresponding spot from the custom matrix and is printed to the screen.
(matrix- filledMatrix customMatrix)

;Scale multiplies each element by 2 and then by 3 so in my filledMatrix each element would be 30
(define thirdMatrix (matrix-scale (matrix-scale filledMatrix 2) 3))

;From this thirdMatrix I subtracted the custom matrix so now each
;element is 25 which is printed to the screen.
(matrix- thirdMatrix filledMatrix)
```


I also messed around with a few other Math functions. One was the random number generator which could be useful in creating games having a random probability of an outcome in say picking a number out of a hat or rolling an equal sided die. This was pretty easy to use because all you had to do was callthe random integer function and a min and max (a range) and it would spit out a random number. I also tried the divisor function which would take in a number and print out all of the factors including 1 and itself. You can also give this a negitive number and the output would be the same. The last fuction is the map fibonacci which would print out the next x amount of fibonacci numbers. 

```racket
;Pick a random integer from 1 to 50
(random-integer 1 50)

;Prints out all factors of a given number.
(divisors 75)

;Prints out the next x amount of fibonacci numbers.
(map fibonacci (range 7))
```



![Image 1](https://github.com/JohnShep/FP2/blob/master/RacketOutput.png?raw=true)
