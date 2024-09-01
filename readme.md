# CodeWars repo for CodeWars things

Trying CodeWars everyday to re-remember best practices, virtual environments etc. 

## Multiples of 3 or 5
01/Sep/2024
If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.
Finish the solution so that it returns the sum of all the multiples of 3 or 5 below the number passed in. 

```
def solution(number):
    print(f'The number input is: {number}')
    list = range(1, number)
    #print(list)
    sum = 0
    for int in list:
        if int % 3 == 0 or int % 5 == 0:
            print(int)
            sum += int
    print(f'The Sum is {sum}')
    return sum
```